I rewrote the checked report in my own words, so my previous reply didn't pass the plugin's number check. That check requires the report exactly as the scripts produced it. The figures are the same; here is the checked report word for word:

---

# August 2026: card sales vs. payouts

**The gap: $471.77** between card orders placed in August and what was paid out to the bank in August. The bridge below closes to zero: every dollar of the gap is explained by refunds, card fees, disputes and money still in transit.

- The bank figure is not checked: the payouts export was not given, so what reached the bank is taken from the transactions export alone.

## The bridge

| | Amount |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| − Refunds processed in August | 58.06 |
| − Card fees | 141.44 |
| − Disputes: amount and fees | 165.17 + 30.00 |
| + Disputes won back | 83.66 |
| + Dispute fees returned | 15.00 |
| Reserve held (-) or released (+) by Shopify | 0.00 |
| Failed payout paid again | 0.00 |
| Shopify adjustments | 0.35 |
| − Still in transit at month end | 271.90 |
| **= Paid out for August's card transactions** | **3,618.07** |
| + Paid out in August for earlier months' transactions | 95.79 |
| **= Paid out to the bank in August** | **3,713.86** |

The last line is the figure to check against your bank statement.

## What's behind the gap

**Disputes.** Two chargebacks; their net cost is 96.51.
- #2015: amount 83.66, fee 15.00
- #2027: amount 81.51, fee 15.00

**Still in transit at month end** (already earned, lands in the first September payouts):
#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

**July orders paid out in August** (these raise August's payouts):
#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

**Split payment.** #2051 (Gift card, Shopify Payments) totalled 120.12: only the card part, 100.12, goes through payouts; the other 20.00 was paid by gift card and never reaches the bank.

**Unmatched items:** none. Every card order has a matching charge at the same amount, and no orders were paid entirely outside Shopify Payments. There were no failed payouts. The payouts export was not provided, so the bank figure comes from the transactions alone.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.11.6, scripts 6e9e71a410d0

## Questions for you

The figures above use the usual answer to each question below until you confirm it; a different answer would change them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by payout-reconciliation v0.11.6 · seal 9182120165ab

---

This report is also saved as `files/reconciliation.md`.
