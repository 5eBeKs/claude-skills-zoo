# NOTES: where I was unsure how Stripe writes things

Everything here comes from Stripe's public documentation as I remember it (knowledge up to mid-2026) plus my own decisions. Nothing was checked against a live account. Confidence: **High**, meaning I would be surprised to be wrong; **Medium**, meaning probably right but details may differ; **Low**, meaning a reasonable guess.

## Global decisions

| # | Point | What the generator does | Confidence |
|---|---|---|---|
| G1 | Report timezone | Truth months are **UTC** calendar months. The Dashboard payments export writes `Created date (UTC)`, and Stripe's financial reports are anchored on `*_utc` columns. The balance file also has local `created` / `available_on` columns in America/Chicago, because a report run with `timezone=America/Chicago` adds them. | Medium |
| G2 | Account timezone in the Dashboard | The payments export was filtered "Jul 1 to Sep 30" in the **account timezone**, so its UTC window is 2026-07-01 05:00 to 2026-10-01 05:00. That is why the first July charges in UTC (Jun 30 evening in Chicago) are missing from it and some October-UTC charges are in it (TRAPS.md #4, #5). | Low to Medium |
| G3 | Chicago offset | Stdlib only and no tzdata, so the generator uses fixed CDT (UTC-5) rules for 2026 (DST Mar 8 to Nov 1). The whole window is in CDT. | High |
| G4 | Money in truth | USD. A charge uses its own exchange rate. A refund, dispute or dispute reversal uses the rate of the day it happened (the USD that actually left or entered the balance), not the charge's rate. | Decision |
| G5 | Which month a payout belongs to | The month its balance transaction was created (the money left Stripe), not its arrival date. `in_transit_at_month_end` lists the difference. | Decision |
| G6 | "disputes_lost" | The amount withdrawn at dispute creation in that month, whatever the later outcome. This matches the balance report's `dispute` category and makes the balance equation close. The `disputes_won_back` value adds money back when a dispute is won. The per-status lists are in TRAPS.md. | Decision |
| G7 | Test mode | A live export never contains test data (modes are fully separate). I simulate the common human error: a test-mode payments export glued under the live one, with `Mode=Test`. Test data appears nowhere else. | Decision. Medium that a `Mode` column exists in payments exports. |
| G8 | Balance excludes reserve | "Balance" = available + pending. Funds moved into the rolling reserve leave it (category `risk_reserved_funds`), and truth reports them separately. | Medium |
| G9 | Balance file covers all categories | Stripe splits this into *Balance change from activity – itemized* (no payouts) and *Payouts – itemized*. As requested, one file has every category, including `payout` and `payout_reversal`, with the Reports API column names. | Decision |
| G10 | Report data end | Taken at 2026-10-04 15:42 UTC, the balance report has data up to 2026-10-04 00:00 UTC (reports lag up to a day). | Low to Medium |
| G11 | CSV encoding | UTF-8 without BOM, LF line endings, minimal quoting (Python `csv`). Stripe may use CRLF or a BOM. | Low to Medium |
| G12 | MRR | Active + past_due subscriptions (not trialing, unpaid or canceled). Annual plans count as 1/12. Forever and still-running repeating coupons are applied, once-coupons are not. VAT is removed from inclusive EUR/GBP prices. Converted at the last day's rate. Stripe's own Billing analytics may differ in edge cases (past_due, FX timing). | Decision |

## unified_payments.csv (Dashboard > Payments > Export)

| # | Point | Choice | Confidence |
|---|---|---|---|
| P1 | Header spelling | `Created date (UTC)`. Older exports say `Created (UTC)`. | Low to Medium |
| P2 | Column set | The classic "all columns" set (id, Description, Seller Message, Amount, Amount Refunded, Currency, Converted Amount, Converted Amount Refunded, Fee, Taxes On Fee, Converted Currency, Mode, Status, card fields, dispute fields, Invoice ID, PaymentIntent ID), plus `Decline Reason`. | Medium |
| P3 | Status values | `Paid` / `Refunded` (fully refunded) / `Failed`. A partially refunded or disputed payment stays `Paid`, and the dispute shows in its own columns. | Low to Medium |
| P4 | Card brand labels | `Visa`, `MasterCard`, `American Express`, `Discover` here. Lowercase API values (`visa`, `amex`) in the balance file. | Medium |
| P5 | Booleans | `true` / `false`. | Low to Medium |
| P6 | Amounts | Major units, 2 decimals, `-` for negatives, no thousands separator. Converted columns are in USD. `Fee` is in USD. Failed rows have empty Converted Amount and `Fee 0.00`. | Medium to High |
| P7 | Metadata | Written as `key (metadata)` columns. The keys order_id, skus, tax_amount, tax_country and promo_code are set by the shop's own Checkout integration. Stripe's payments export has **no tax column**, so one-time tax is only in this metadata (presentment currency) and subscription tax only in invoices.csv. | Medium (column naming), Decision (keys) |
| P8 | Amount Refunded after a refund failure | A failed refund is not counted, so the charge shows 0.00 again. | Medium |
| P9 | Converted Amount Refunded | The sum of the refunds' own USD amounts (the refund-day rate), so a full refund can differ from Converted Amount. | Medium |
| P10 | Dispute status values | API values: needs_response, under_review, won, lost, warning_needs_response, warning_under_review, warning_closed. | High (values), Medium (that the export prints them raw) |
| P11 | Evidence due time | 23:59:59 UTC, 7 to 18 days after the dispute. | Low |
| P12 | Descriptions | One-time: `Order GL-nnnnnn` (set by the shop). Invoices: `Subscription creation`, `Subscription update` (renewals too), `Payment for Invoice` (manual and late hosted-page payments). | Low to Medium |
| P13 | Statement descriptor | `GRIDLOFT* ASSETS` / `GRIDLOFT* PRO` (prefix + suffix). ACH uses `GRIDLOFT`. | Medium |
| P14 | Id shapes | Modern ids: `<prefix>_<1 or 3><5 time chars><last 10 chars of acct id><8 chars>`. pi_/ch_/txn_ of one payment share the first 16 characters. Refunds get their own base. `py_` for ACH. Customers are `cus_` + 14. | Medium (structure), Low (exact character semantics) |
| P15 | Taxes On Fee | 0.00 (no tax on Stripe fees for a US account). | Medium |

## balance_transactions_itemized.csv (Reports: itemized balance)

| # | Point | Choice | Confidence |
|---|---|---|---|
| B1 | Column names | balance_transaction_id, created_utc, created, available_on_utc, available_on, currency, gross, fee, net, reporting_category, source_id, description, customer_facing_amount, customer_facing_currency, automatic_payout_id, automatic_payout_effective_at_utc, customer_*, charge_id, payment_intent_id, charge_created_utc, invoice_id, subscription_id, payment_method_type, card_brand, card_funding, card_country, dispute_reason, payment_metadata[order_id]. | Medium to High (names), Medium (payment_metadata[key]) |
| B2 | No `type` column | The itemized reports group by reporting_category. Balance-transaction types are in the model (`charge`, `payment`, `refund`, `payment_refund`, `refund_failure`, `adjustment`, `stripe_fee`, `tax_fee`, `reserved_funds`, `payout`, `payout_failure`) but not written. | Medium |
| B3 | available_on | Card charges: 00:00 UTC, 2 business days after the UTC charge date (US holidays skipped). ACH: 4 business days. Refunds, disputes, fees, reserve, adjustments, payouts: available immediately (= created). | Medium to Low |
| B4 | Refund rows | Category `refund`, fee 0.00 (Stripe keeps the original processing fee), description `REFUND FOR CHARGE (<charge description>)`. | Medium (fee), Low to Medium (description) |
| B5 | Refund failure | Category `refund_failure`, +amount at the refund's USD value, description `REFUND FAILURE`, source = the refund id. | Medium (category), Low (description) |
| B6 | Dispute rows | Type adjustment, category `dispute`, gross = -disputed amount, fee = 15.00, net = -(amount+15). Won: category `dispute_reversal`, gross +amount (reversal-day FX), fee -15.00. Descriptions `Chargeback withdrawal for ch_…` / `Chargeback reversal for ch_…`, source = du_ id. | Medium to High |
| B7 | Dispute fee returned on a win | Yes (US). Stripe's newer separate "dispute countering fee" (announced 2025, as I recall) is **not** modelled. | Medium |
| B8 | Inquiries | No balance transaction and no fee. | Medium to High |
| B9 | Billing / Tax usage fees | One row per product per UTC day, posted the next day around 02:xx UTC. Category `fee`, the amount is in **gross** (fee column 0.00), empty source_id, descriptions `Billing - Usage Fee (YYYY-MM-DD)` / `Tax - Usage Fee (YYYY-MM-DD)`. Billing is 0.7% of recurring and invoice volume, Tax 0.5% of charges where tax was calculated. Stripe may bill these monthly or with other wording. | **Low** |
| B10 | Rolling reserve | Category `risk_reserved_funds`, a daily hold of 5% of the previous UTC day's volume at 04:11 UTC, released 30 days later. Empty source_id, my own descriptions. | **Low** |
| B11 | Manual adjustment | Category `other_adjustment`, empty source_id, description `Credit for duplicate Billing usage fee (2026-08-10)`. | Low |
| B12 | Payout rows | Category `payout`, gross = -amount, description `STRIPE PAYOUT`, source = po_ id, empty automatic_payout_id. | Medium to High (description), Medium (empty payout id) |
| B13 | Payout failure | Type `payout_failure`, category `payout_reversal`, +amount, source = the failed po_ id, description `STRIPE PAYOUT FAILURE`, swept into the next payout. | Medium (category), Low (description) |
| B14 | automatic_payout_effective_at_utc | The payout's arrival date at 00:00:00. | Low |
| B15 | Currency | Always `usd` (a US account settles only in USD). The customer's currency is in customer_facing_*. | High |

## payouts.csv (Dashboard > Balances > Payouts > Export)

| # | Point | Choice | Confidence |
|---|---|---|---|
| O1 | Columns | id, Amount, Currency, Arrival Date (UTC), Created (UTC), Status, Type, Method, Source Type, Automatic, Description, Destination, Statement Descriptor, Failure Code, Failure Message, Failed At (UTC), Balance Transaction, Failure Balance Transaction. | Low to Medium |
| O2 | Timing | Daily automatic payouts. A payout is created on the business day **before** its arrival date, around 21:xx UTC, and sweeps every balance transaction available by 00:00 UTC of the arrival date. | Low to Medium |
| O3 | Arrival Date format | `YYYY-MM-DD 00:00:00`. | Low |
| O4 | Failed payout | failure_code `invalid_account_number` (the owner mistyped a new bank account on Aug 12). Payouts are paused until the account is fixed on Aug 18. The money comes back as `payout_reversal` and leaves in the next payout, which gets a new id, because Stripe has no "retry" of the same payout id. | Medium |
| O5 | Filter | Arrival date on or after 2026-07-01, so it includes a payout created on June 30. One payout is `in_transit` at the export. | Decision |

## invoices.csv / subscriptions.csv (Dashboard exports)

| # | Point | Choice | Confidence |
|---|---|---|---|
| I1 | Invoice columns | id, Number, Customer (+name/email/country), Subscription, Billing Reason, Collection Method, Status, Currency, Date (UTC), Finalized At, Due Date, Period Start/End, Subtotal, Discount, Coupon, Tax, Total, Starting/Ending Balance, Amount Due/Paid/Remaining, Attempt Count, Attempted, Paid At, Voided At, Next Payment Attempt, Charge, Description. | Low to Medium |
| I2 | Period Start/End | The line-item service period (the period being paid for). The API's `invoice.period_*` for renewals refers to the previous period. | Medium |
| I3 | Draft window | Renewal invoices stay draft for 1 hour and get their Number when finalized. subscription_create invoices finalize immediately. | High |
| I4 | Trial conversion | The first paid invoice after a trial has billing_reason `subscription_cycle`. | Medium to High |
| I5 | Dunning settings (merchant's choice) | Retries 2/5/9/14 days after the first failure. Afterwards the subscription is marked `unpaid` and the invoice is left open. Every Monday the owner cancels unpaid subscriptions and voids their open invoice. | Decision |
| I6 | incomplete → incomplete_expired | After 23 hours, with the first invoice voided. | High |
| I7 | Amount Remaining on void | 0.00. | Low |
| I8 | Credit balance | A negative starting balance reduces Amount Due. If it covers the whole total, the invoice is paid with no charge (Attempt Count 0, empty Charge). | High (semantics), Medium (export columns) |
| I9 | Coupons | LAUNCH20 counts its 3 months from signup (the trial eats part of it). WELCOME5 (once, USD only) is given only to non-trial signups. | High (repeating semantics) |
| I10 | Proration | Monthly → annual upgrade: annual price minus a time-proportional credit, tax on the net. Two lines in the model, one net Subtotal in the export. | Medium |
| I11 | Subscription columns | id, Customer ID/Name/Email, Plan (price id), Product (prod id), Quantity, Interval, Amount, Currency, Status, Created, Start, Current Period Start/End, Trial Start/End, Canceled At, Cancel At Period End, Ended At, Coupon (only if still active). | Low to Medium |
| I12 | canceled_at for cancel_at_period_end | The time of the request, not the end of the period. | High |
| I13 | Stripe Tax | USD/CAD prices exclusive, EUR/GBP inclusive. The merchant is registered in TX, WA, PA, OH, NJ, UT, TN, EU OSS, UK and Canada GST/HST/QST. B2B customers are in Oregon (no sales tax). | Decision |
| I14 | Manual B2B invoices | send_invoice, net 15, paid by ACH Direct Debit (`py_`). The balance transaction is created when the debit starts and becomes available 4 business days later. The invoice is `paid` when the debit succeeds. | Low to Medium |

## Fee schedule used (Stripe US standard, as I know it)

Card: 2.9% + $0.30, plus 1.5% for cards issued outside the US and 1% when the presentment currency is not USD. The percentage is computed on the converted USD amount and rounded half-up to the cent. ACH Direct Debit: 0.8%, capped at $5.00. Dispute fee: $15.00. Billing: 0.7%. Tax: 0.5%. Confidence: High for the rates, Medium for rounding (Stripe may round each component separately).

## The three format points I am least sure of

1. **Billing/Tax usage-fee rows (B9)**: daily rows posted the next day, with the amount in `gross`, an empty source and my own description wording.
2. **Rolling-reserve rows (B10)**: category `risk_reserved_funds` is right, but the row granularity (daily), empty source_id and descriptions are guesses.
3. **Payments-export labels (P1, P3, G7)**: the `Created date (UTC)` header, `Paid/Refunded/Failed` status words and the `Mode` column.
