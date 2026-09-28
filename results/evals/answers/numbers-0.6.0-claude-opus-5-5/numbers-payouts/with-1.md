<!-- numbers-0.6.0-claude-opus-5-5 / numbers-payouts / with the plugin / run 1: passed -->

I've reconciled the two exports and the figures pass the number check. The answer is below.

# August 2026: card sales vs. what reached the bank

**The gap: €371.08** between card orders placed in August and what Shopify Payments paid out to the bank in August. Every euro of the gap is accounted for (unexplained difference: €0.00). It went to refunds, card fees, one dispute, and payouts that were still on their way to the bank at month end.

## The bridge

| | | EUR |
|---|---|---:|
| | Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − | Refunds processed in August | 70.50 |
| − | Card fees | 56.59 |
| − | Disputes: amount and fees | 19.30 + 15.00 = 34.30 |
| − | Still in transit at month end | 209.69 |
| = | Paid out for August's card transactions | 2,448.74 |
| = | **Paid out to the bank in August** | **2,448.74** |

The last line should match the Shopify Payments payouts on your bank statement for August. It's worth checking.

## Where the gap went

- **Dispute:** order #1060 was disputed for €19.30, plus a €15.00 dispute fee.
- **In transit at month end:** €209.69. This money isn't lost; it was paid out in early September:
  #1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)
- **Refunds and card fees** make up the rest, as shown in the table.

## Not in the payout report at all

Orders paid outside Shopify Payments never show up in payouts, so don't look for this money there. It goes to your PayPal account (€99.00):
#1055 (PayPal Express Checkout)

## Unmatched items

None. Every counted card order has a matching charge, every charge matches a counted order, and every charge amount matches its order.

## Open questions: the figures above use the usual answer until you confirm

A different answer would change the figures above.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.6.0, scripts 2ba057087965
