<!-- numbers-0.5.1-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 3: passed -->

None of the money is missing. The difference comes from disputes, card fees, refunds and payouts that hadn't landed by 31 August, and it's fully accounted for.

# August 2026 payout reconciliation

**The gap: $471.77.** Card orders placed in August came to $4,185.63; the bank received $3,713.86 from Shopify Payments in August. Nothing is missing: the bridge below closes to $0.00. The biggest pieces are two disputes ($195.17), money still in transit on 31 August ($271.90) and card fees ($141.44).

## The bridge

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

Check the last line against your bank statement.

## Disputes

- Order #2015: $83.66 disputed, plus a $15.00 dispute fee
- Order #2027: $81.51 disputed, plus a $15.00 dispute fee

The "dispute_won" and "adjustment" transactions in the payout report (together $99.01 in your favour) are counted on their own line above.

## Still in transit on 31 August (arrives in September)

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

## July orders paid out in August

These July 31 charges landed in the bank on 3 August, so they are in August's bank total but not in August's sales:

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

## Money that never goes through payouts

Order #2051 ($120.12) was paid partly by gift card: only the $100.12 card part is in payouts; the $20.00 gift-card part will never appear there. Test orders (Bogus Gateway) are left out of sales entirely.

## Unmatched items

None: every counted card order has a matching charge, every charge matches a counted order, and no charge amount differs from its order.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

Computed from:

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.5.1, scripts 32efef0622a7

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

1. Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
2. The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
