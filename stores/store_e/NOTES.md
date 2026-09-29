# NOTES

Decisions made where Shopify's behaviour or file format was not certain, each with my confidence
(high / medium / low). Sources: Shopify Help Center pages read on [a day in September 2026] ("Exporting orders",
"Shopify Payments payout details", "Payout timing", "Reserves") and my own knowledge. Nothing was taken
from any other store or project.

## 1. The store and the model

- Synthetic store "Kade & Klei Wonen" (fictional), Utrecht, NL. Shop currency EUR, prices include VAT,
  "dynamic tax-inclusive pricing" on: an EU customer pays the same gross price, and the VAT inside it depends
  on the destination country (OSS). Rates: NL/BE/ES 21, DE 19, FR/AT 20, IT 22, IE/PL 23, DK/SE 25, FI 25.5,
  LU 17. GB 20 (store is UK VAT registered), CH 8.1 (import VAT collected at checkout), US no tax.
- Presentment currencies GBP, USD, CHF: EUR price converted at the day's rate and rounded up to x.95.
  For US the NL VAT is removed first. Duties are collected at checkout: US 15 % of goods value (EU-US
  tariff), CH 2.6 %. The rates move a little every day (random walk, fixed seed).
- B2B customers in DE/BE with a VAT ID are tax exempt (reverse charge): prices without NL VAT, no tax line.
- The event model runs from 1 May 2026 to the export moment, Sunday 4 Oct 2026 10:15 Europe/Amsterdam.
  May-June exist so that July has an opening balance, June orders can be refunded or disputed in July and
  June gift cards can be redeemed. Nothing happens after the export moment (checked).
- Store time is Europe/Amsterdam; every moment in the model is in CEST (UTC+02:00). Only Net 30 due dates
  can reach winter time; they are written with +0100.
- Money is integer cents; every conversion or tax extraction rounds once, half away from zero.
- Orders created per day follow a weekday/hour profile with a July linen sale and a September newsletter
  week. 20,537 orders are created in Jul-Sep (12 test orders and 3 deleted real orders among them);
  20,522 are counted.

## 2. Export scopes (what the merchant exported)

| File | Scope | Confidence it is a normal choice |
|---|---|---|
| orders_export.csv | Created at on/after 1 Jul 2026 00:00, no end date, so 1-4 Oct orders are inside | high |
| payment_transactions_export.csv | Transaction Date on/after 26 May 2026 00:00 | high |
| payouts_export.csv | Payout Date on/after 1 Jun 2026 | high |
| products_export.csv | all products, old CSV template (as asked) | high |

Test orders are in the orders export (Shopify lists them in the admin); deleted orders are not.

## 3. orders_export.csv

- Column set and order: the 79-column layout I know from real exports (Name ... Payment References).
  The Help Center table lists the same fields in a slightly different order (it puts Phone second and the
  Province Name columns next to Province); I kept the file order I remember. Confidence medium.
- Header spelling "Cancelled at" and "Lineitem compare at price", "Lineitem sku": as in real files; the
  Help Center writes "Canceled at" / "compare-at". Confidence medium.
- **Amounts are in shop currency (EUR) and Currency is always EUR.** The Help Center says the Currency
  column is "Your store's base currency at the time of the order". So a GBP order shows EUR line prices such
  as 50.29; the customer's currency and amount appear only in the payments export (Presentment Amount /
  Presentment Currency) and in truth.json. Each EUR field is converted separately, so Subtotal + Shipping +
  Duties can miss Total by a cent. Confidence medium (community reports disagree).
- Multi-line orders: order-level fields only on the first row. Name, Email, Created at, all Lineitem columns,
  Vendor and Lineitem discount repeat on every row. Tax columns are written on the first row only.
  Confidence medium (tax columns: medium-low).
- Dates: `2026-07-01 00:12:34 +0200` (format quoted in the Help Center for the payments export). High.
- Tax-inclusive store: Subtotal = line prices minus all product discounts, VAT included; Total = Subtotal +
  Shipping + Duties + tip. Taxes shows the VAT already inside those amounts. Medium.
- Discount Amount = line-level + order-level product discounts + shipping discounts (VAT included).
  Lineitem discount = only discounts applied to that line (automatic "3 voor 2 kaarsen", "Zomer Sale
  Linnen -20%"); per Help Center it excludes order-level product discounts. Discount Code lists codes only,
  joined with ", "; automatic and manual draft discounts leave it empty (Help Center: excludes automatic).
  Medium / low for the ", " join.
- Free shipping code: Shipping column shows 0.00 and the saved shipping is in Discount Amount. Medium-low.
- Tax 1 Name is written as `<country code> <local VAT name> <rate>%`, e.g. `NL BTW 21%`, `FI ALV 25.5%`,
  `CH MWST 8.1%`. Only one tax line per order (one destination rate). Low-medium.
- Payment Method labels: "Shopify Payments", "PayPal Express Checkout", "Klarna", "Bank Deposit",
  "gift_card", "Cash", "manual" (B2B marked as paid), "bogus"; several joined with " + " (separator from the
  Help Center). Labels: medium.
- Payment ID / Payment Reference / Payment References: `c<checkout id>.<n>` for checkout orders,
  `r<11 digits>.<n>` for draft/POS orders; Payment References also counts captures and refunds (Help Center
  semantics). Format: low.
- Financial Status values: pending, authorized, partially_paid, paid, partially_refunded, refunded, voided.
  A cancelled order that never captured money is "voided". Zero-total orders are "paid". Medium.
- Paid at = first capture (Klarna: at fulfilment; bank transfer: when marked paid). Medium.
- Fulfillment Status fulfilled / partial / unfulfilled; Lineitem fulfillment status fulfilled / pending.
  Medium-low.
- Order edits: an added item is a new row; a removed item stays as a row with Lineitem quantity 0 (current
  quantity) and Subtotal/Total drop. Low.
- Exchanges: the new item is an extra row, the returned line keeps its quantity, and Total includes the new
  item (returns never reduce Total; Refunded Amount and Outstanding Balance carry the rest). So an exchange
  at equal price has Total above what was charged. Low.
- Outstanding Balance (Help Center: shown because the POS channel is installed) = Total − value returned −
  (captured − refunded), never below 0. Medium.
- Refunded Amount = money refunded, in EUR at the refund-day rate. Medium.
- Source: web, pos, shopify_draft_order, and `3890849` for the Shop app channel (numeric channel id). The
  numeric id is invented. Low.
- Tips: in Total only, no column of their own. Low-medium.
- Walk-in POS sales have no customer: Email and billing fields empty. Pickup, gift-card-only and POS
  orders have no shipping address. Medium.
- Emails use example.com/.net/.org; B2B and staff use `.example` domains. No real person or company.

## 4. payment_transactions_export.csv (Shopify Payments)

- Columns: the 11 the Help Center lists (Transaction Date, Type, Order, Card Brand, Card Source, Payout
  Status, Payout Date, Available On, Amount, Fee, Net) plus Checkout, Payment Method Name, Presentment
  Amount, Presentment Currency, Currency, which current exports carry. The extra five: medium.
- Type values `charge`, `refund`, `dispute`, `reserve`. A chargeback is a negative `dispute` row with Fee
  15.00; a won chargeback is a positive `dispute` row with Fee -15.00 (amount and fee returned). A lost
  chargeback has no second row. Labels: low. Fee return on a win: medium-low.
- Card Source: empty for online payments, `contactless` for POS (Help Center example is "swiped"). Low.
- Payment Method Name: card / ideal / apple_pay. Card Brand: visa, master, american_express, maestro;
  empty for iDEAL. Medium-low.
- Payout Status: paid, scheduled, failed, pending (API spelling; the admin shows "Deposited"). Medium-low.
- Amount and Net in EUR (payout currency). Charges on GBP/USD/CHF orders are converted at the rate of the
  charge day; refunds and chargebacks at their own day's rate.
- Fees (my assumption for a NL store): EEA cards 1.9 % + 0.25, non-EEA cards and Amex 2.9 % + 0.25,
  iDEAL 0.29, POS 1.5 %, plus 1.5 % currency conversion for non-EUR payments. Refunds do not return the
  processing fee (high). Chargeback fee 15.00 (medium).
- Test-mode and Bogus orders create no rows; live tests with a real card do.

## 5. payouts_export.csv

- Columns: Payout Date, Status, Charges, Refunds, Adjustments, Reserved Funds, Fees, Retried Amount, Total,
  Currency. Medium. Fees are written negative so the columns add up to Total. Low-medium.
- Adjustments = chargebacks and their reversals (amounts only); chargeback fees are in Fees.
- Grouping (Help Center, Netherlands): settlement 3 business days, counted from the **UTC** capture date;
  Friday-Sunday captures are paid together on Wednesday. So a charge at 00:30 store time on the 1st is
  grouped with the previous UTC day. Public holidays in model: 14 and 25 May. Medium-high.
- Reserve: fixed EUR 7,500 held on 10 Aug (negative reserve row in that day's payout), EUR 5,000 released
  on 21 Sep (positive row), EUR 2,500 still held at export. Help Center confirms negative/positive reserve
  transactions; the label "reserve" is my choice. Medium / low.
- Failed payout on Fri 28 Aug: its transactions stay linked to it (Payout Status failed). Payouts due
  31 Aug and 1 Sep were held while the bank account was re-verified (their Available On dates stay, Payout
  Date becomes 2 Sep), and the 2 Sep payout carries the failed total in Retried Amount. Low-medium.
- The 5 Oct payout exists at export as `scheduled`; later transactions are `pending` with no Payout Date.

## 6. products_export.csv

- Old template (Variant SKU ... Cost per item, Variant Inventory Qty present), plus Included / Price /
  Compare At Price columns for the markets United Kingdom, United States, Switzerland (prices empty =
  converted automatically) and Status. Medium.
- Gallery image rows (Handle + Image Src + Image Position only) for products with 6+ variants.
- Shows the state at export: renamed SKUs, new mug costs, the renamed tablecloth title; the deleted picnic
  blanket is missing; an archived product (beach towel, sold only in May-June) and a draft product are
  included. Barcodes use the restricted 2x prefix so they can never be a real GTIN.

## 7. truth.json - Analytics definitions I followed

Figures are in EUR, "reversals on their own day", store-time months.

- Gross sales = price x quantity **without VAT** (tax-inclusive store); discounts and returns also without
  VAT. Returns = value of returned units after their discounts. Medium-high.
- Gift card sales are not in gross sales (breakdown `gift_card_sales_not_in_gross_sales`); tips are not in
  total sales (`tips_not_in_total_sales`). High.
- Shipping = shipping charged without VAT minus shipping refunded; free-shipping discounts reduce shipping
  and are not in discounts (breakdown `shipping_discounts_not_in_discounts`). Medium.
- Duties = duties charged minus duties refunded. `additional_fees` is 0 (the store charges none). Medium.
- Order edits: an added item is gross sales on the edit day, a removed item a return on the edit day.
  Medium-low.
- Exchanges: the returned unit is a return and the new item is a sale, both on the exchange day. Medium.
- Cancellation reverses every remaining item, shipping, duties and tip as returns/negatives on the cancel
  day, even when no money was ever captured. Medium.
- Refund without items (goodwill) is a return with no tax reversal. Medium-low.
- Chargebacks do not change sales. Medium-high.
- Currency: order amounts at the order's rate; reversals at the rate of their own day, so a fully cancelled
  GBP order need not net to exactly 0.00. Medium-low.
- `count` = orders created in the month (store time), including cancelled, POS, draft and zero-total
  replacement orders, excluding test and deleted orders. `cancelled_later_or_same_month` = those of them
  cancelled by the export moment.
- Test orders: Shopify itself only excludes orders with its test flag (Bogus, test mode). I also exclude
  the staff STAFF100 orders and the two live-card tests, all tagged `test`, because they are tests; Shopify
  Analytics would count them. The live tests' money stays in `shopify_payments`. Decision.
- Deleted orders are excluded from sales and count; their Shopify Payments rows stay in `shopify_payments`.
  Medium.
- "Refunds after the export" is read as refunds dated 1-4 Oct (after the period, before the export): they
  are visible in the export and must not reach Q3. A refund after the export moment cannot exist in the
  files, so the model has none.

## 8. truth.json - money definitions

- `shopify_payments`: Shopify Payments rows by store-time month of Transaction Date. Charges +, refunds −,
  chargebacks −, chargeback_reversals +, reserve_movements (hold −, release +), fees_processing −,
  fees_chargeback_net − (15.00 per chargeback minus fees returned on wins). net_activity = sum of Net.
- `payouts.deposited` = payouts with Status paid and Payout Date in the month; `failed` = failed ones.
- `money_in_transit` = Net of all Shopify Payments rows up to the month end minus deposited payouts up to
  the month end. It excludes the reserve (shown in `reserve_held_closing`) and includes a failed payout until
  its retry is deposited. closing = opening + net_activity − deposited_total (checked).
- `other_payment_methods`: PayPal, Klarna, bank transfer, B2B marked-as-paid, cash, gift card, by event
  month, EUR at the event-day rate. Gift card: redeemed, refunded back to cards, issued by sale, issued
  manually (no sale), outstanding balance.
- `receivables_closing` at the last second of the month: orders not cancelled with Outstanding Balance > 0:
  bank transfer pending, B2B payment terms, partially paid, Klarna authorised but not captured (money due
  from Klarna after capture, listed separately).
- `margin`: rows grouped by variant, keyed by current SKU (or `no-sku:<handle>:<variant>`); cost is the unit
  cost stored on the line at the time of sale (units returned reverse their own recorded cost). A variant
  with no cost gets `cost_recorded: null`. Goodwill refunds cannot be tied to a SKU and are in
  `returns_not_attributable_to_sku`.

## 9. Things deliberately left out

Shopify Balance, Shop Pay Installments, Markets Pro / Managed Markets, marketplace channels, inventory
adjustments, taxes on B2B shipping to exempt customers other than removal of VAT, US state sales tax,
refund failures and payout adjustments other than those listed.
