<!-- numbers-0.5.2-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 1: passed -->

# August 2026 payout reconciliation

**The gap is $471.77, and none of it is missing.** Card orders placed in August came to $4,185.63, and $3,713.86 reached your bank in August. The bridge below accounts for every dollar: the unexplained difference is $0.00. In order of size, the gap comes from money still on its way on 31 August, two disputes, card fees, and refunds.

| | USD |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | $4,185.63 |
| − Refunds processed in August | $58.06 |
| − Card fees | $141.44 |
| − Disputes: amount and fees | $195.17 |
| &nbsp;&nbsp;&nbsp;disputed amount | $165.17 |
| &nbsp;&nbsp;&nbsp;dispute fees | $30.00 |
| + Other payout transactions (adjustment, dispute_won) | $99.01 |
| − Still in transit at month end | $271.90 |
| **= Paid out for August's card transactions** | **$3,618.07** |
| + Paid out in August for earlier months' transactions | $95.79 |
| **= Paid out to the bank in August** | **$3,713.86** |

Check the last line against your bank statement.

## Disputes (chargebacks)
- #2015: $83.66 disputed, plus a $15.00 dispute fee
- #2027: $81.51 disputed, plus a $15.00 dispute fee

Together these cost $195.17. The payout export also has `dispute_won` and `adjustment` rows, which add back $99.01 net ("Other payout transactions" in the table).

## Still in transit on 31 August
This money has been paid out but reaches your bank in September: #2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02). Total: $271.90.

## July orders paid out in August
#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03). Total: $95.79. These are part of the August bank figure but aren't August sales.

## Paid outside Shopify Payments
Order #2051 was paid partly by gift card. Only the $100.12 card part goes through payouts. The $20.00 gift-card part will never show up in a payout, so there's no need to look for it there.

## Unmatched items
Every order matched its charge. No order is missing a charge, no charge is missing an order, and no amounts disagree.

## How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.5.2, scripts 05e46938ecfc

## Questions for you
The figures above use the usual answer to each question until you confirm it. A different answer would change them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
