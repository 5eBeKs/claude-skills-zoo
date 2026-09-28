<!-- numbers-0.6.0-claude-opus-5-5 / numbers-payouts / with the plugin / run 3: passed -->

I reconciled both exports. The figures below have passed the number check, and a copy is saved as `files/reconciliation_2026-08.md`.

# August 2026: card sales vs. money in the bank

**The gap is €371.08.** That's card orders placed in August minus what Shopify Payments paid out to the bank in August. The bridge closes to zero (unexplained difference: €0.00), so every euro of it is accounted for below.

## The bridge

| | | EUR |
|---|---|---:|
| | Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − | Refunds processed in August | 70.50 |
| − | Card fees | 56.59 |
| − | Disputes: amount and fees (19.30 + 15.00) | 34.30 |
| − | Still in transit at month end | 209.69 |
| = | Paid out for August's card transactions | 2,448.74 |
| = | **Paid out to the bank in August** | **2,448.74** |

The last line is what your bank statement should show from Shopify for August. Check it against the statement.

## Where the gap went

- **Money still on its way:** €209.69 from late-August orders was in transit on 31 August and lands in early September:
#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)
- **Refunds:** €70.50, all on August orders.
- **Card fees:** €56.59 deducted by Shopify Payments.
- **Dispute:** order #1060 was charged back. €19.30 was taken back, plus a €15.00 dispute fee.

## Not in the payouts at all

Orders paid outside Shopify Payments (€99.00) go to that provider, not to your Shopify payouts. Look for this money in PayPal:
#1055 (PayPal Express Checkout)

## Unmatched items

None. Every counted card order has a matching charge, every charge matches a counted order, and no charge amount differs from its order.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

Computed from:
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.6.0, scripts 2ba057087965

## Questions for you

The figures above use the usual answer until you confirm. A different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

<!-- the report this run saved next to the exports: reconciliation_2026-08.md -->

# August 2026: card sales vs. money in the bank

**The gap is €371.08** — card orders placed in August against what Shopify Payments paid out to the bank in August. The bridge closes to zero (unexplained difference: €0.00), so every euro of it is accounted for below.

## The bridge

| | | EUR |
|---|---|---:|
| | Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − | Refunds processed in August | 70.50 |
| − | Card fees | 56.59 |
| − | Disputes: amount and fees (19.30 + 15.00) | 34.30 |
| − | Still in transit at month end | 209.69 |
| = | Paid out for August's card transactions | 2,448.74 |
| = | **Paid out to the bank in August** | **2,448.74** |

The last line is the figure your bank statement should show from Shopify for August — worth checking against it.

## Where the gap went

- **Money still on its way:** €209.69 from late-August orders was in transit on 31 August and lands in early September:
#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)
- **Refunds:** €70.50, all on August orders.
- **Card fees:** €56.59 deducted by Shopify Payments.
- **Dispute:** order #1060 was charged back — €19.30 taken back plus a €15.00 dispute fee.

## Not in the payouts at all

Orders paid outside Shopify Payments (€99.00) go to that provider, not to your Shopify payouts — look for this money in PayPal:
#1055 (PayPal Express Checkout)

## Unmatched items

None: every counted card order has a matching charge, every charge matches a counted order, and no charge amount differs from its order.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

Computed from:
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.6.0, scripts 2ba057087965

## Questions for you

The figures above use the usual answer until you confirm; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

