<!-- numbers-0.5.1-claude-opus-5-5 / numbers-payouts / with the plugin / run 2: passed -->

Card orders in August were €371.08 more than what reached your bank that month. Nothing is missing: refunds, card fees, one chargeback and money still on its way at month end account for every cent. Here's the full breakdown:

---

# August 2026: where the card money went

**The gap: €371.08** between card orders placed in August and what Shopify Payments paid out to the bank in August. The bridge below closes to zero: every euro of it is accounted for by refunds, card fees, a dispute, and money still on its way to the bank at month end.

Two things the figures below rest on, which I need you to confirm (see "Questions for you" at the end): test orders are left out of sales, and the export's payment methods, statuses and tags are as expected. The figures use the usual answer until you confirm; a different answer changes them.

## The bridge

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees (19.30 + 15.00) | 34.30 |
| − Still in transit at month end | 209.69 |
| **= Paid out for August's card transactions** | **2,448.74** |
| **= Paid out to the bank in August** | **2,448.74** |

The last line is the figure your bank statement should show from Shopify Payments for August: please check it against the bank. No August payouts were for earlier months' sales, and every refund was on an August order.

## Where it went

- **Refunds:** €70.50 given back to customers.
- **Card fees:** €56.59 kept by Shopify Payments on 57 card orders.
- **Dispute:** order #1060 was charged back: €19.30 taken back plus a €15.00 dispute fee.
- **In transit:** €209.69 was on its way at 31 August and lands in September:
#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)

## Not in the payouts at all

Orders paid outside Shopify Payments never appear in the payout report, so don't look for this money there; it went to that provider's account (€99.00):
#1055 (PayPal Express Checkout)

## Unmatched items

None: every counted card order has its charge, every charge belongs to a counted order, and all amounts match.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.5.1, scripts 32efef0622a7

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

If you confirm the two answers above, I'll save them so next month's run points out anything new in the exports.
