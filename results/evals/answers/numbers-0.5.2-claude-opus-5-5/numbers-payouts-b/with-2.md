<!-- numbers-0.5.2-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 2: passed -->

Nothing is missing. The gap is fully explained and the bridge closes to $0.00. Here's the reconciliation, generated from both exports and checked against them:

---

# August 2026 payout reconciliation

**The gap: $471.77** between card orders placed in August ($4,185.63) and what reached the bank in August ($3,713.86). The bridge below closes with $0.00 unexplained, so nothing is missing: the gap is refunds, card fees, two disputes and money still on its way, partly offset by a dispute won, an adjustment and late-July sales paid out in August.

Money still in transit ($271.90) is not lost — it lands in early September. The real costs are the two disputes ($195.17 with fees), card fees and refunds.

## Bridge

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

The last line is the figure to check against your bank statement.

## Disputes

- Order #2015: $83.66 plus a $15.00 dispute fee
- Order #2027: $81.51 plus a $15.00 dispute fee

## Still in transit at month end (arrives in September)

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

## July orders paid out in August

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

## Other notes

- Order #2051 was split: $100.12 on card (counted above) and $20.00 by gift card, which never goes through payouts — don't look for that $20.00 in the payout report.
- Unmatched items: none. Every counted card order has a matching charge, every charge matches a counted order, and all amounts agree.

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

The figures above use the usual answer to each of these until you confirm it; a different answer would change them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

If you confirm the two answers above, I'll save the export shape so next month's run flags any new payment method, status or payout type.
