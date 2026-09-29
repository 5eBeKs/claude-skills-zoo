Short answer: no money is missing. The payout is $471.77 below August card sales because of four things: money still on its way to your bank on Aug 31, two chargebacks (one was won back), card fees and refunds. Some July sales paid out in August make up part of the difference. Each line below is accounted for, with nothing left unexplained.

This isn't checked against your bank yet, because I only had the orders and transactions exports. If you export Finances > Payouts > Export, I can check the $3,713.86 payout by payout.

# August 2026 payout reconciliation

- The bank figure is not checked: the payouts export was not given, so what reached the bank is taken from the transactions export alone.

**The gap:** card sales placed in August exceed what reached the bank in August by **$471.77**. Nothing is missing: the bridge below closes, with an unexplained difference of 0.00. The gap is mostly money still on its way to the bank at month end, disputes, card fees and refunds.

## Bridge: card sales to the bank

| | Amount |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| − Refunds processed in August | 58.06 |
| − Card fees | 141.44 |
| − Disputes: amount and fees | 165.17 and 30.00 |
| + Disputes won back | 83.66 |
| + Dispute fees returned | 15.00 |
| Reserve held (-) or released (+) by Shopify | 0.00 |
| Failed payout paid again | 0.00 |
| Shopify adjustments | 0.35 |
| − Still in transit at month end | 271.90 |
| **= Paid out for August's card transactions** | **3,618.07** |
| + Paid out in August for earlier months' transactions | 95.79 |
| **= Paid out to the bank in August** | **3,713.86** |

The last line is the figure to find on your bank statement. The disputes' net cost for the month is 96.51.

## Disputes

- Order #2015: amount 83.66, fee 15.00
- Order #2027: amount 81.51, fee 15.00

## Still in transit at month end (arrives in September)

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

## July orders paid out in August

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

## Split payments

Order #2051 (Gift card, Shopify Payments) totalled 120.12: the card part 100.12 went through Shopify Payments, the rest 20.00 was paid by gift card and never reaches a payout.

## Unmatched items

None: every counted card order has a matching charge at the right amount, and every charge matches a counted order. No orders were paid entirely outside Shopify Payments, and no payouts failed. No payouts export was given, so the bank figure comes from the transactions alone.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.11.0, scripts a07884a2bdbf

## Questions for you

The figures above use the usual answer to each question until you confirm it; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by payout-reconciliation v0.11.0 · seal f0d6dbcca401
