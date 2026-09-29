# NOTES

Every place where I was not sure how Amazon writes a field, a line or a report. For each one I give what the
files contain, how confident I am that real Seller Central output looks like that (as of Jul-Oct 2026), and
why. "Mine" means a modelling choice with no Amazon source behind it.

Sources I used: my own knowledge of Seller Central reports; the SP-API report-type page for
`GET_V2_SETTLEMENT_REPORT_DATA_FLAT_FILE_V2`; SP-API GitHub issue #5391 (27 Sep 2026, a CAD V2 file that writes
`FBAFees | FBA Inventory Storage Fee | Base fee`); the SP-API changelog, which removes the legacy flat file and
XML settlement reports on 2026-11-11; A2X articles on reserves (`Current Reserve Amount`,
`Previous Reserve Amount Balance`) and on DD+7 ("deferred transactions don't appear in the settlement file
until the cash actually moves"); a Seller Forums thread on coupon fees (after 15 Jul 2025 the Date Range
report writes type `Amazon Fees`, description `Coupon Performance Based Fee` / `Coupon Participation Fee`);
several articles on the June 2025 coupon fee change ($5 per coupon + 2.5% of coupon sales); and a Feedvisor
note that in early 2026 the Date Range transaction report switched to posting date instead of payout date.

## 1. Which date puts each item in a month

The seller keeps books by calendar month in America/Los_Angeles. truth.json uses these rules:

| item | date that decides the month | why |
|---|---|---|
| order charges (principal, shipping, gift wrap, promotions, tax, referral, FBA fee, shipping chargeback) | `posted-date-time` converted to Pacific time. For FBA and MFN alike this is the shipment time, **not** purchase-date, DD+7 release, settlement end or deposit date | the settlement file and the Date Range report both carry it; it is when Amazon charges the buyer |
| refunds, A-to-z debits, chargeback debits | posted date-time (Pacific) of the refund/debit line | same reason; the sale stays in its own month |
| storage, aged-inventory, removal, placement, coupon fees, subscription, labels | posted date-time (Pacific), even though storage is for the month before | this is the posted-date rule the task asks for; accrual is left to the seller (see TRAPS) |
| advertising | posted date-time of each invoice charged to the account | ad spend by day would need the Ads console; not in these files |
| reimbursements | posted date-time (Pacific) | |
| tax collected / remitted | posted date-time of the line (Pacific) | nets to zero every month |
| deposits | the bank posting date (`bank/disbursements.csv`) | cash is in the bank on that date; the settlement `deposit-date` and the Date Range `Transfer` row are when Amazon *started* the transfer |
| failed disbursement | the Pacific date of the attempted deposit (`deposit-date` of that settlement) | listed under `disbursements.failed` of that month |
| orders count / units / cancelled | purchase-date converted to Pacific time | "orders placed in the month" |
| owed_by_amazon_at_month_end | the instant 00:00 Pacific on the 1st of the next month; `reserve_held` = `Current Reserve Amount` of the last settlement closed before that instant | |
| claims open at month end | filed before that instant and not decided by it | outcome shown as known on Oct 6 |
| orders refunded in a later month | sale month = Pacific month of the order's posted date; refund month = Pacific month of the refund's posted date | Oct 1-6 refunds are listed and flagged `in_a_settlement_file: false` |

Sign convention: the settlement file's own sign (money to the seller positive). Month "activity" =
net_product_sales + amazon_fees.total + advertising.total + reimbursements.total + tax collected + tax remitted.
The lines `Previous Reserve Amount Balance`, `Current Reserve Amount`, `Payable to Amazon`,
`Failed disbursement` and the Date Range `Transfer` rows move money within Amazon or to the bank. They are never activity.

## 2. Settlement report, Flat File V2

| point | what the files contain | confidence | basis |
|---|---|---|---|
| column list and order | the 24 columns from the brief | 90% | brief; SP-API page confirms the three-column amount layout |
| summary row | first data row: settlement-id, start, end, deposit-date, total-amount, currency, then 18 empty fields; detail rows leave those five empty | 75% | memory of real files |
| date format | `2026-08-31 23:42:09 UTC` for start/end/deposit/posted-date-time | 60% | memory for US; a Japanese V2 parser (2026) shows `2026/09/15 08:03:13 UTC`, and EU files use `DD.MM.YYYY`, so the separator may differ |
| posted-date | the **UTC** calendar date of posted-date-time | 55% | follows from the UTC time stamp; this is what makes last-evening Pacific lines look like the next month |
| amounts | `-12.34`, point decimal, no thousands separator, never blank | 75% | SP-API page: local formats (EU `95,00`); US uses a point |
| currency on detail rows | empty (only on the summary row) | 55% | memory |
| encoding / line ends / quoting | ASCII, LF, no quoting | 55% | flat files are unquoted TSV; line ending not sure |
| row order | by posted date-time | 40% | real files seem grouped by order but are not strictly sorted |
| file name | `settlements/settlement_<settlement-id>.txt` | mine | real downloads carry a report id as the name |
| settlement-id | 11 digits, rising about 40 million per period | 70% | issue #5391 shows `26827395211` for July 2026 |
| order lines | transaction-type `Order`; amount-type `ItemPrice` (Principal, Shipping, GiftWrap, Tax, ShippingTax, GiftWrapTax), `ItemFees` (FBAPerUnitFulfillmentFee, Commission, ShippingChargeback, GiftwrapChargeback), `ItemWithheldTax` (MarketplaceFacilitatorTax-Principal, -Shipping), `Promotion` (Principal, Shipping) | 80% | long-standing names |
| gift wrap tax withheld | `MarketplaceFacilitatorTax-Other` | 35% | could be `-Giftwrap` |
| refunds | transaction-type `Refund`, same amount types; referral returned as `ItemFees/Commission` (+) and `ItemFees/RefundCommission` (-) | 80% | |
| A-to-z | transaction-type `A-to-z Guarantee Refund` | 40% | may be written `A-to-z Guarantee Claim` as in the Date Range report |
| chargeback | transaction-type `Chargeback Refund` | 60% | |
| quantity-purchased | repeated on every row of an order item; empty on refund rows | 40% | memory of pivot problems; not sure about refunds |
| shipment-id | FBA: `D` + 8 letters/digits; MFN: empty | 40% | |
| adjustment-id / merchant-adjustment-item-id | 14 digits / 9 letters-digits on refund rows | 35% | format is a guess; that they exist on refunds is 75% |
| order-item-code | 14 digits | 70% | |
| marketplace-name | `Amazon.com` on rows tied to a customer order, empty on account-level rows | 50% | |
| fulfillment-id | `AFN` / `MFN` on order-related rows, empty elsewhere | 65% | |
| reserve | `other-transaction / other-transaction / Previous Reserve Amount Balance` (+) posted at the period start, `... / Current Reserve Amount` (-) posted at the period end | 80% names, 55% posting dates | A2X naming |
| FBA inventory fees (2026 layout) | transaction-type `FBAFees`, amount-type = fee name (`FBA Inventory Storage Fee`, `FBA Long-Term Storage Fee`, `FBA Removal Order: Return Fee`, `FBA Removal Order: Disposal Fee`, `FBA Inbound Placement Service Fee`), amount-description `Base fee`; US has no `Tax on fee` rows | storage 50%, others 35% | issue #5391 writes storage this way in 2026. Which column holds `FBAFees` and which holds the fee name is 45%. Older US files wrote `other-transaction / other-transaction / Storage Fee`, `StorageRenewalBilling`, `RemovalComplete`, `DisposalComplete`; a parser should accept both |
| aged-inventory surcharge label | `FBA Long-Term Storage Fee` | 40% | Amazon renamed the fee; the report label may now say "Aged Inventory Surcharge" |
| coupon fees | transaction-type `AmazonFees`, amount-type `Coupon Participation Fee` or `Coupon Performance Based Fee`, description `Base fee`; performance fee one row per redeemed order with the customer order-id, posted about 1.5 minutes after shipment, not deferred; participation fee $5 at coupon start with a 12-character fee id as order-id | names 70%, V2 layout 35%, timing 40% | forum thread (Date Range names), fee change articles |
| coupon discount | `Promotion / Principal` with promotion-id `PLM_<uuid>` | promotion row 75%, id format 30% | |
| seller promotion ids | `Percentage Off 2026/07/08 10-22-41-517`, `Free Shipping 2026/02/11 9-40-18-226` | 55% | default internal description style of Amazon promotions |
| advertising | `ServiceFee / Cost of Advertising / TransactionTotalAmount`; $500 threshold invoices plus a month-end invoice at 02:31:05 UTC on the 1st | names 70%, timing mine | |
| subscription | `other-transaction / other-transaction / Subscription Fee`, -39.99 at 00:12:37 UTC on the 1st | names 50%, time mine | |
| reimbursements | `other-transaction / FBA Inventory Reimbursement / WAREHOUSE_LOST` (DAMAGE, MISSING_FROM_INBOUND, REVERSAL_REIMBURSEMENT, CUSTOMER_RETURN), sku + quantity, order-id only for CUSTOMER_RETURN | 65% names, 50% order-id rule | amounts are 62% of list price per unit (mine) |
| removal fees | order-id holds the removal order id; sku, quantity filled | 45% | |
| inbound placement | shipment-id holds the FBA shipment id, quantity = units | 30% | |
| Buy Shipping labels | `other-transaction / other-transaction / Shipping label purchase`, order-id of the MFN order, 3 minutes before ship confirmation | 35% | Date Range writes type `Shipping Services` (60%) |
| negative balance | settlement total negative, no deposit; the next settlement starts with `other-transaction / other-transaction / Payable to Amazon` equal to that negative total | name 55%, mechanics 45% | A2X/accounting write-ups name `Payable to Amazon` and `Successful charge` (card charge); I carry it forward, no card charge |
| failed disbursement | the settlement file keeps its deposit-date; the returned money comes back as `other-transaction / other-transaction / Failed disbursement` (+) in the next settlement and is paid with it | 25% name, 45% mechanics | Amazon says the money goes back to the account and out again after the bank details are fixed; the exact line label is a guess |
| Request Transfer | closes the open settlement at the click (end = deposit-date, 16:42 PDT), the next period runs only to the original scheduled close | 40% | if Amazon restarts a 14-day cycle instead, the 3.5-hour negative stub would not exist |
| deposit-date | settlement end + 1 day, same clock time (request transfer: at the end time) | 45% | |
| DD+7 | an order's lines sit in the settlement in which funds are released (delivery date + 7 days, daily batch 10:00-14:00 UTC) and keep their original posted-date, so every file has lines dated before its own start date | 55% | A2X quote above; batch time mine |

## 3. Date Range reports (monthly transaction report)

I judged this report realistic and necessary. It is the only file that shows lines of the still-open
settlement and DD+7 deferred orders not yet released. Without it, September cannot be closed from the files.

| point | what the files contain | confidence | basis |
|---|---|---|---|
| file name | `2026JulMonthlyTransaction.csv` | 50% | custom ranges download as `2026Jul1-2026Jul31CustomTransaction.csv` |
| preamble | 7 quoted lines before the header (USD note and column definitions) | 75% that such lines exist | **the wording is mine**; parsers should search for the `date/time` header row |
| header | `date/time, settlement id, type, order id, sku, description, quantity, marketplace, account type, fulfillment, order city, order state, order postal, tax collection model, product sales, product sales tax, shipping credits, shipping credits tax, gift wrap credits, giftwrap credits tax, Regulatory Fee, Tax On Regulatory Fee, promotional rebates, promotional rebates tax, marketplace withheld tax, selling fees, fba fees, other transaction fees, other, total` | 60% | memory of 2023-2025 files |
| date/time | `Aug 31, 2026 4:42:09 PM PDT`, Pacific, the file covers the Pacific calendar month | 70% format, 55% month boundary | |
| numbers | all fields quoted; zero written `0`; others two decimals; thousands separator comma (`-46,421.19`) | 50% | |
| encoding | UTF-8, LF | 40% | |
| type/description | `Order`; `Refund`; `A-to-z Guarantee Claim`; `Chargeback Refund`; `Service Fee` (`Cost of Advertising`, `Subscription`); `FBA Inventory Fee` (`FBA storage fee`, `FBA Long-Term Storage Fee`, `FBA Removal Order: Return Fee`, `FBA Removal Order: Disposal Fee`, `FBA Inbound Placement Service Fee`); `Adjustment` (`FBA Inventory Reimbursement - Lost:Warehouse`, `- Damaged:Warehouse`, `- Lost:Inbound`, `- Reversal`, `- Customer Return`); `Amazon Fees` (coupon fees); `Shipping Services` (`Shipping label purchase`); `Transfer` (`To account ending in 4417`, `Failed disbursement`) | 55% overall; `Failed disbursement` 25% | |
| where non-order amounts go | the `other` column (ads, subscription, storage, reimbursements, transfers) | 55% | |
| rows per order | one row per order item per transaction | 65% | |
| reserve and `Payable to Amazon` | not shown in this report | 50% | |
| DD+7 | rows dated at posted date (early-2026 change); settlement id = the settlement the money is released in; **blank** while not yet released on the report date | 60% posting date, 30% blank id | |
| Transfer rows | dated when Amazon starts the transfer (the settlement deposit-date), failed one included, amount negative | 55% | |
| description | product title at the time the line posted | 50% | |

## 4. All Orders report

| point | what the file contains | confidence |
|---|---|---|
| columns | the 32 in the file (no `url`, `is-iba`, `order-invoice-type` etc.) | 60% |
| scope | orders with purchase-date from 2026-07-01 00:00 PDT to 2026-09-30 23:59:59 PDT, requested Oct 6 | mine |
| dates | UTC, `2026-08+00:00` | 65% |
| item-price | line total (unit price x quantity), tax in item-tax | 60% |
| promotion discounts | written negative (`-7.50`), blank when none | 45% |
| zero shipping / gift wrap | blank | 40% |
| cancelled | order-status `Cancelled`, item-status `Cancelled`, quantity `0`, all money blank | 40% |
| partial cancellation | order `Shipped`, one line item-status `Cancelled`, quantity 0 | 45% |
| ship-city | as typed by the buyer (mixed case, some upper, some lower) | 70% |
| encoding | Windows-1252 (curly apostrophe 0x92, en dash 0x96, degree 0xB0), LF, unquoted | 55% |
| product-name | title at purchase time | 70% |

## 5. Bank disbursements list

My own simple CSV (`deposit_date, settlement_id, amount, account, bank_description`, CRLF), holding the
bank posting dates from Jul 1 to the report date. A real bank export would not carry a clean settlement-id
column; I kept it because the brief asks for it. The failed ACH does not appear, because the old account was
closed and never showed the credit. The last deposit (Oct 1) is after September's month end.

## 6. Money and fee assumptions (mine unless noted)

- Referral 15% (Home & Kitchen, 85%) of price + shipping + gift wrap minus promotions, minimum $0.30 per item (70%).
- Refund administration fee = min($5.00, 20% of the referral fee returned) (80%). Refunds return the ShippingChargeback when shipping is refunded (60%).
- FBA per-unit fees are per SKU at plausible 2026 levels, not Amazon's rate card. MFN label costs are by weight.
- Tax: one combined rate per state and a simplified shipping-taxability flag. Business buyers are tax-exempt half the time. OR/MT/NH/DE/AK are 0%.
- Storage fee posted on the 8th-10th for the previous month (70%); aged-inventory surcharge on the 15th-17th (60%). Amounts are mine.
- Reserve = max($1,500, 4% of order principal posted in the trailing 30 days), recomputed at each close; $2,850 held when the simulation starts on 2026-04-28. The formula is mine, but Amazon's reserve does vary settlement to settlement.
- A-to-z claims and chargebacks only on MFN orders. A granted claim refunds principal, shipping and tax, returns the referral fee and takes the refund administration fee (50%).
- DD+7 release at delivery date + 7 days. Bank credit on the next business day after the UTC deposit-date. US bank holidays: May 25, Jun 19, Sep 7, Oct 12.
- The whole period is in PDT; the code applies the US DST rule in general.

## 7. Deliberately not modelled

The low-inventory-level fee, the returns processing fee, Colorado and Minnesota retail delivery fees (the
`Regulatory Fee` columns stay 0), deal/Lightning Deal and Prime Exclusive Discount fees, Vine,
carrier adjustments on Buy Shipping labels, liquidations, SAFE-T claims, pay-by-invoice business orders,
a card charge for a negative balance (`Successful charge`), and orders placed after Sep 30. Without October
orders, the October part of the open settlement holds only refunds, fees and DD+7 releases of earlier orders;
no file shows it anyway. Also not modelled: the limit on how far back the Statements page offers settlement
downloads. I assume all eight files were downloaded.
