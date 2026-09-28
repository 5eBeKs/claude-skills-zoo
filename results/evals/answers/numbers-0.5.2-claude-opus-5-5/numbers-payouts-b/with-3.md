<!-- numbers-0.5.2-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 3: passed -->

## August 2026: why the payout is lower than sales

**Card orders placed in August came to $4,185.63. The bank received $3,713.86 in August. That is a gap of $471.77.** The bridge closes to the cent, with an unexplained difference of $0.00. The biggest causes are the two disputes, money still in transit at month end, and card fees.

| | USD |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| − Refunds processed in August | 58.06 |
| − Card fees | 141.44 |
| − Disputes: amount and fees | 165.17 + 30.00 = 195.17 |
| + Other payout transactions (adjustment, dispute_won) | 99.01 |
| − Still in transit at month end | 271.90 |
| **= Paid out for August's card transactions** | **3,618.07** |
| + Paid out in August for earlier months' transactions | 95.79 |
| **= Paid out to the bank in August** | **3,713.86** |

Check that last line against your bank statement.

**Disputes (chargebacks).** Each dispute takes back the order amount and adds a fee:
- #2015: $83.66 plus a $15.00 fee
- #2027: $81.51 plus a $15.00 fee

The payout export also has adjustment and dispute_won lines, which add money back. They are in the "+ Other" row.

**Still in transit at month end.** You have not lost this money. It lands in September: #2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02).

**July orders paid out in August.** These increase August's bank total: #1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03).

**Not paid through Shopify Payments.** Order #2051 was split between a gift card and a card. Only its card part of $100.12 is in the payouts. The gift-card part of $20.00 never goes through payouts, so don't look for it there.

**Unmatched items:** none. Every counted order has a matching charge, and every charge amount matches its order.

### Questions for you
The figures above use the usual answers below until you confirm them. A different answer would change the figures.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them? The export has orders paid through "Bogus Gateway (for testing)", and these are currently left out.
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

### How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.5.2, scripts 05e46938ecfc
