<!-- numbers-0.6.0-claude-opus-5-5 / numbers-payouts / with the plugin / run 2: passed -->

I reworded my first answer, so it wasn't the text that passed the figure check. Here is the checked version, unchanged. All the figures are the same as before.

## Where August's money went

In August you took **€371.08 more in card orders than reached the bank**. There is no missing money: refunds, card fees, one dispute and payouts still on their way to the bank account for the whole gap. The bridge closes to 0.00.

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees (19.30 + 15.00) | 34.30 |
| − Still in transit at month end | 209.69 |
| **= Paid out for August's card transactions** | **2,448.74** |
| **= Paid out to the bank in August** | **2,448.74** |

The last line is the figure your bank statement should show for August. Please check it against the bank.

**Dispute:** order #1060 was disputed. You lost the 19.30 charge plus a 15.00 dispute fee.

**Still in transit on 31 August.** This money is paid out in early September:
#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)

**Paid outside Shopify Payments.** These orders never appear in payouts, so the money is in PayPal and not in the bank transfer (€99.00):
#1055 (PayPal Express Checkout)

**Unmatched items:** none. Every card order has a matching charge and every amount agrees.

### How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.6.0, scripts 2ba057087965

### Questions for you
The figures above use the usual answer to each question until you confirm it. A different answer changes them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
