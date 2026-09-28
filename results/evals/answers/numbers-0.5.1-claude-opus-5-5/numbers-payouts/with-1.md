<!-- numbers-0.5.1-claude-opus-5-5 / numbers-payouts / with the plugin / run 1: passed -->

Nothing is missing. The whole gap between August's card sales and what reached your bank is explained: €0.00 is left over. The money went to refunds, card fees, one dispute, and payouts that were still on their way on 31 August.

## August 2026: where the card money went

Card orders in August came to €2,819.82, and €2,448.74 reached the bank. The gap is **€371.08**, and all of it is accounted for (unexplained difference: €0.00).

**Before you rely on these figures:** they assume test orders (tagged "test" or paid through Shopify's test gateway) are left out of sales. That's the usual choice, but you haven't confirmed it yet. If you want them counted, the figures change. The questions are at the end.

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees | 19.30 + 15.00 = 34.30 |
| − Still in transit at month end | 209.69 |
| **= Paid out for August's card transactions** | **2,448.74** |
| **= Paid out to the bank in August** | **2,448.74** |

The last line is the total your bank statement should show from Shopify for August. None of the money paid out in August was for sales from earlier months.

In short, the money went to:
- **Refunds:** €70.50, all on August orders.
- **Card fees:** €56.59.
- **One dispute:** order #1060. You lost the €19.30 sale plus a €15.00 dispute fee.
- **Money still on its way:** €209.69 was not in the bank by 31 August. It is from orders at the end of the month and arrives in early September: #1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02).

**Not in the payouts at all:** #1055 (PayPal Express Checkout). It was paid by PayPal, so that money goes to your PayPal balance and never appears in the Shopify Payments payouts. It is not included in the card orders figure above.

**Unmatched items:** none. Every counted card order has a matching charge, every charge has a counted order, and all the amounts agree.

### How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.5.1, scripts 32efef0622a7

### Questions for you
The figures above use the usual answer to each question until you confirm it. A different answer changes them.
1. Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
2. The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
