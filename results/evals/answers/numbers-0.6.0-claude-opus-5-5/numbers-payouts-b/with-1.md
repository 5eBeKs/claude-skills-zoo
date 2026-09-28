<!-- numbers-0.6.0-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 1: passed -->

Nothing is missing. August card sales were $4,185.63 and $3,713.86 reached the bank, so the gap is **$471.77**. Every dollar of that is accounted for. The biggest parts are two chargebacks, fees, and money that was still on its way to the bank on August 31.

# August 2026 payout reconciliation

**The gap: $471.77.** Card orders placed in August came to $4,185.63; the bank received $3,713.86 from Shopify Payments in August. The bridge below closes to $0.00: nothing is missing. The biggest pieces are two disputes ($195.17 including fees), money still in transit at month end ($271.90) and card fees ($141.44).

## The bridge

| | USD |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| minus Refunds processed in August | 58.06 |
| minus Card fees | 141.44 |
| minus Disputes: amount and fees | 165.17 + 30.00 |
| plus Other transactions (adjustment, dispute_won) | 99.01 |
| minus Still in transit at month end | 271.90 |
| **equals Paid out for August's card transactions** | **3,618.07** |
| plus Paid out in August for earlier months' transactions | 95.79 |
| **equals Paid out to the bank in August** | **3,713.86** |

The last line is the figure to check against your bank statement.

## Disputes

- Order #2015: $83.66 disputed, plus a $15.00 dispute fee
- Order #2027: $81.51 disputed, plus a $15.00 dispute fee

Together: $195.17. The "Other transactions" line is a dispute you won (money returned to you) and an adjustment.

## Still in transit at month end

These August sales were paid out in the first days of September, so they will be on September's bank statement:

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

## July orders paid out in August

These July 31 orders landed in the bank on August 3, so August's payouts include them:

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

## Paid outside Shopify Payments

One order was paid partly by gift card and partly by card. Only the card part goes through payouts, so the gift card part won't appear in the payout report:

#2051 (Gift card, Shopify Payments)

## Unmatched items

None: every counted card order has a matching charge, every charge has a counted order, and all amounts match.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.6.0, scripts 2ba057087965

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer would change them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
