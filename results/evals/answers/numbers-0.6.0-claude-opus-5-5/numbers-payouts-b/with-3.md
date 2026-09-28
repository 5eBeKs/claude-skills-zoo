<!-- numbers-0.6.0-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 3: passed -->

Nothing is missing. Of the $471.77 gap, $271.90 is money still on its way: three orders were paid out in early September. The rest went to fees, chargebacks and refunds. Every dollar is accounted for, with $0.00 left unexplained.

# August 2026 payout reconciliation

**The gap: $471.77.** Card orders placed in August came to $4,185.63, and $3,713.86 reached the bank in August. The bridge below closes to $0.00 unexplained. The biggest pieces are two chargebacks, card fees, and three orders whose payouts landed in early September.

Two open questions at the end (test orders, and confirming the export's shape) could change these figures. Until you answer, the figures use the usual answer.

## Bridge

| | | USD |
|---|---|---:|
| | Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| − | Refunds processed in August | 58.06 |
| − | Card fees | 141.44 |
| − | Disputes: amount and fees | 165.17 + 30.00 = 195.17 |
| + | Other transactions (adjustment, dispute_won) | 99.01 |
| − | Still in transit at month end | 271.90 |
| = | Paid out for August's card transactions | 3,618.07 |
| + | Paid out in August for earlier months' transactions | 95.79 |
| = | **Paid out to the bank in August** | **3,713.86** |

**Paid out to the bank in August** is the figure to check against your bank statement.

## Disputes (chargebacks)

- Order #2015: $83.66 disputed, plus a $15.00 fee
- Order #2027: $81.51 disputed, plus a $15.00 fee

The export also has "dispute_won" and "adjustment" transactions. Together they add back $99.01, which is the "Other transactions" line above.

## Still in transit at month end

These are August sales. Their payouts reach the bank in September:

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

## Earlier sales paid out in August

These are July orders that were paid out in August:

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

## Paid outside Shopify Payments

$20.00 was paid by gift card, so it will never appear in a payout. This was the gift card part of split-payment order #2051: order total $120.12, of which $100.12 was paid by card and $20.00 by gift card.

## Unmatched items

None. Every counted card order has a matching charge, every charge matches a counted order, and no charge amounts differ from their orders.

## How this was counted

Definitions:

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

Export:

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Files:

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.6.0, scripts 2ba057087965

## Questions for you

The figures above use the usual answer to each question below until you confirm it. A different answer changes the figures.

1. Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
2. The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
