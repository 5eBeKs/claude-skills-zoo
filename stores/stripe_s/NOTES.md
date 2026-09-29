# NOTES - how Stripe writes things, and what we had to guess

Stripe documentation was read in September 2026 (docs.stripe.com, support.stripe.com). Where the docs did not settle a
point we chose, and the choice is listed here with a confidence level: **high** (documented), **medium** (consistent with
docs and common knowledge, not verified field by field), **low** (our best guess).

## Time stamps: which are UTC and which are New York time

| file | columns | zone |
|---|---|---|
| customers, subscriptions, invoices, invoice_line_items, credit_notes, payments, payouts, disputes, coupons, promotion_codes, prices | every column whose header ends in `(UTC)` | UTC, `YYYY-MM-DD HH:MM:SS` |
| balance_change_from_activity_itemized | `created_utc`, `available_on_utc`, `automatic_payout_effective_at_utc`, `charge_created_utc` | UTC |
| balance_change_from_activity_itemized | `created`, `available_on`, `automatic_payout_effective_at`, `charge_created` | America/New_York (report run with `timezone=America/New_York`) |
| payouts_itemized | `effective_at_utc` UTC, `effective_at` New York; `payout_expected_arrival_date` is a plain date | |
| balance_summary_* | the dates inside the descriptions are New York calendar dates | |

- Dashboard exports write UTC and say so in the header: **medium-high**. Report columns with and without `_utc` and their
  meaning are documented for the payout-reconciliation itemized report: **high**; that the same optional columns
  (`automatic_payout_id`, `automatic_payout_effective_at*`, customer and card columns) can be selected on the
  balance-change-from-activity itemized report: **medium**.
- `available_on` for card payments = 00:00 UTC two business days after the charge (US holidays skipped): **medium**.
- Automatic payouts are deducted from the Stripe balance at `automatic_payout_effective_at`, "the date we expect this
  automatic payout to arrive" (documented: **high**). We stamp it at **00:00 UTC** of the arrival date, which is 20:00 New
  York time on the previous day - so in a New York balance report a payout arriving on the 1st counts in the previous
  month: **low-medium** (time of day is our choice).

## File formats

- **Invoice line items**: we found no general Dashboard export of invoice line items (the Invoices page exports invoices;
  the Tax Rates page offers an "invoice line item tax export"; Sigma has an `invoice_line_items` table). The file is written
  in Dashboard style (Title Case headers, `(UTC)` stamps, major units) with Invoice-line-item API fields. Existence of such a
  file in this exact form: **low**. `Unit Amount` is the price's unit amount, so on proration and trial lines
  `Quantity x Unit Amount` does not equal `Amount` - that matches the API (`price.unit_amount` vs prorated `amount`): **medium**.
- **Credit notes**: no documented Dashboard CSV export found; Dashboard-style file with Credit Note API fields: **low**.
- **Unified payments export** column names (`Created date (UTC)`, `Converted Amount`, `Converted Amount Refunded`,
  `Seller Message`, `Taxes On Fee`, `Payment Source Type`, `Mode` ...): **medium**. `Status` values `Paid` / `Refunded`
  (fully refunded) / `Failed`, partial refunds stay `Paid`: **medium-low**. Failed rows show `Converted Amount` 0.00: **low**.
  Bank-transfer rows show `Payment Source Type` = `customer_balance`: **low-medium**.
- **Subscriptions export**: one row per subscription item (the Business plan has a base item and a seat item, so two rows
  share one `id`): **low-medium**. `Amount` = unit amount of the item's price; `Canceled At (UTC)` is filled as soon as
  cancel_at_period_end is set, while status is still active (API behaviour: **high**; export column: **medium**).
  Metadata column written as `migrated_from (metadata)`: **medium**. `pause_collection` is not in the export: **medium**.
- **Invoices export**: column set is a mix of the classic export (`Billing` = collection method, `Attempt Count`,
  `Starting Balance`, `Ending Balance`, `Period Start/End (UTC)`) and newer fields (`Paid At`, `Voided At`,
  `Marked Uncollectible At`, `Customer Name/Email`): **medium-low**. Customer name/e-mail are the snapshot on the invoice.
- **Invoice period**: on subscription_cycle invoices `Period Start/End` is the previous period (the "usage period during
  which invoice items were added"), not the service period; the service period is on the lines: **high**. On create,
  update and manual invoices both are the creation time: **medium**.
- **Customers export**: `Balance` uses the API sign (negative = credit the customer can spend): **medium-low**.
  `Currency` blank for customers never invoiced: **medium**. `Total Spend` (net of refunds), `Payment Count`,
  `Refunded Volume`, `Dispute Losses` in the customer's currency: **low**.
- **Balance summary** (`balance.summary`): categories `starting_balance`, `activity`, `payouts`, `ending_balance` and the
  descriptions `Starting balance (date)`, `Activity`, `Total payouts`, `Ending balance (date)` are documented: **high**.
  Row order and using the exclusive end date in `Ending balance (YYYY-MM-DD)`: **low**.
- **Payouts itemized**: payout rows carry the balance-transaction sign (negative gross/net), reversals positive: **low-medium**.
  `payout_reconciliation_status` values: **low**. Dashboard payouts export column set: **low-medium**.
- **Disputes, coupons, promotion codes, prices exports**: column sets **low-medium**.
- File names are descriptive; Stripe's own downloads are named differently (for example `unified_payments.csv`,
  `Itemized_balance_change_from_activity_USD_<from>_to_<to>_America-New_York.csv`): **medium** for those names.
- Amounts: major units with 2 decimals, `-` for negatives, no thousands separators; currency codes lower case: **high**.
- CSV: UTF-8 without BOM, LF line ends, minimal quoting: **medium**. Line descriptions use `×` and currency symbols.
- Ids: real prefixes (`cus_`, `sub_`, `si_`, `in_`, `il_`, `ii_`, `ch_`, `py_`, `pi_`, `re_`, `dp_`, `cn_`, `txn_`, `po_`,
  `pm_`, `price_`, `prod_`, `promo_`, `ba_`); payment-intent families share a stem (`pi_3...`, `ch_3...`, `re_3...`,
  `txn_3...`) like real ids: **medium**. Invoice numbers `PREFIX-0001` per customer, credit notes `<invoice number>-CN-01`:
  **medium-high**.

## Billing behaviour

- Trial start creates a paid 0.00 invoice (`subscription_create`, line "Trial period for ..."): **high**. The first real
  invoice after a trial has billing_reason `subscription_cycle`: **medium-low**.
- Renewal invoices are created at the period boundary and finalized/charged about an hour later (so an invoice can be dated
  in one month and paid in the next): **high**.
- Smart Retries modelled as 4 retries about 3, 7, 12 and 18 days after the first failure: **medium** (configurable in Stripe).
- `unpaid` subscriptions keep generating invoices that are finalized but never attempted: **medium** (docs: "invoices continue
  to be generated, but payments aren't attempted").
- pause_collection `void`: renewal invoice finalized (gets a number) and voided at once; `keep_as_draft`: stays draft;
  `mark_uncollectible`: finalized and marked uncollectible. Status stays `active`: **medium** for status, **low-medium**
  for numbering.
- Trials ending without a payment method: cancel (before 2026-07-15) or `paused` (after): **high** that both settings exist.
- `incomplete` -> `incomplete_expired` after 23 hours with the first invoice voided: **high**.
- Prorations: per-second fraction of the current period, one credit line for the old price/quantity and one charge line for
  the new, each rounded to the cent (half away from zero); descriptions `Unused time on N x Product after D Mon YYYY` /
  `Remaining time on ...`: **medium**. Interval change resets the billing anchor and invoices immediately: **high**.
- Discounts: a subscription coupon applies to every line of the invoice (subscription lines, proration lines, one-off
  items added to that invoice); a fixed-amount coupon is capped at the positive subtotal and spread over positive lines:
  **medium-low**. `once` coupons are consumed by the first invoice with a positive amount, not by the 0.00 trial invoice: **low-medium**.
  `repeating` coupons run N months from the moment they are applied (trial days included): **high**.
- Negative invoice totals go to the customer credit balance; the balance is applied at finalization of later invoices
  (`Starting Balance` / `Ending Balance`): **high**.
- Pre-payment credit notes reduce `Amount Due` / `Amount Remaining`, not `Total`: **medium-high**.
- Paying an invoice out of band sets it paid and fills `Amount Paid` with the amount that was due: **medium-low**.
- The final invoice of an immediate cancel with prorate + invoice_now has billing_reason `subscription_update`: **low**.
  Resuming a paused subscription invoices at once with billing_reason `subscription_update`: **low**.
- Deleting a customer removes it from the customers export but its invoices, payments and canceled subscriptions keep the
  `cus_` id (customer e-mail/name blank where Stripe reads the live customer): **medium-low**.

## Money

- Card fee 2.9% + 0.30 USD; +1.5% for non-US cards; +1% when the charge currency is not USD, all included in the `fee`
  of the charge: **medium** for the rates, **low-medium** for folding the conversion 1% into the fee.
- Bank-transfer payments (`py_`, customer_balance): fee 0.5% capped at 5.00 USD (+1% conversion for EUR/GBP): **low**.
- Refunds do not return the processing fee: **high**. EUR/GBP refunds are converted at the refund-date rate: **medium**.
- Disputes: one balance transaction (`reporting_category=dispute`) with the amount and a 15.00 dispute fee (never
  returned); a separate 15.00 "dispute countered fee" when evidence is submitted, returned if won (both documented in the
  Stripe support FAQ): **medium**. Our countered-fee rows use `reporting_category=fee` and wording "Dispute countered fee for
  dp_...": **low**. Won disputes reverse the same USD amount that was withdrawn: **low-medium**. Descriptions "Chargeback
  withdrawal for ch_..." / "Chargeback reversal for ch_...": **medium**.
- Refund balance transactions described `REFUND FOR CHARGE (<charge description>)`: **medium**. Failed refund:
  `reporting_category=refund_failure`, positive: **high** for the category, **low** for the wording.
- Stripe Billing (0.7%) and Stripe Tax (0.5%) usage fees posted as separate `fee` rows once a month (on the 2nd) with
  negative gross and 0.00 in the fee column: **low** for timing and wording (Stripe may bill them daily), **medium** for
  their being separate rows.
- Charge descriptions `Subscription creation` (first invoice), `Subscription update` (renewals and updates),
  `Payment for Invoice` (manual invoices): **medium**.
- Payout failure: `payout_failure` balance transaction (`reporting_category=payout_reversal`) returns the money; the next
  payout sweeps it: **high** for the category. The swept transactions keep the failed payout's id: **low-medium**.
- Daily payouts (2-business-day rolling), created ~13:00-13:45 UTC and arriving the next business day; weekly on
  Wednesdays from 2026-08-19: our choice, **medium** that it looks realistic.
- FX: one daily EUR/USD and GBP/USD rate, applied at the charge date (no separate markup): our model.

## Definitions (answer key)

- Primary MRR follows Stripe Billing analytics as documented (September 2026): active + past_due subscriptions, unpaid =
  churn, trials excluded, taxes and one-off items excluded, FX adjustment line in the roll-forward: **high**. Stripe drops a
  subscription from MRR as soon as cancel_at_period_end is set - we keep it until it ends in the primary figure and give
  Stripe's convention as `stripe_billing_convention`. Discounts: recurring (repeating/forever) coupons subtracted, one-time
  not (Stripe lets you configure both).
- Sales-tax rates per city are rough synthetic approximations, not authoritative rates.
- Not included on purpose: Stripe's own "MRR per subscriber" and "Subscription metrics" downloads (they would hand over
  the answer and their exact format is not documented), Sigma output, Revenue Recognition reports.
