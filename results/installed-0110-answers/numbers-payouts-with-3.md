No money is missing. Card orders came to €2,819.82 and €2,448.74 reached the bank in August, a gap of €371.08. Refunds, card fees, one chargeback and payouts that hadn't landed by 31 August account for all of it, down to the cent. The biggest part, €209.69, arrives in the first days of September. The bank figure hasn't been checked yet (see the warning at the top). Here is the checked reconciliation, also saved as `reconciliation.md`:

---

# August 2026: card sales vs. what reached the bank

**Warning, read first:**

- The bank figure is not checked: the transactions export starts on 2026-08-01 and the payouts export was not given.

**The gap: €371.08** between card orders placed in August and what Shopify paid out to the bank in August. The bridge below explains all of it; the unexplained difference is 0.00. Nothing went missing. The money went to refunds, card fees, one dispute, and payouts that were still on their way at month end.

## The bridge

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees | 19.30 + 15.00 |
| − Still in transit at month end | 209.69 |
| **= Paid out for August's card transactions** | **2,448.74** |
| **= Paid out to the bank in August** | **2,448.74** |

The last line is the figure to find on your bank statement. No reserve, adjustments or failed payouts showed up this month.

## Where the gap went

- **Money still on its way (209.69).** This is the largest part. These orders were paid in the last days of August and land in early September:
#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)
- **Refunds (70.50).** All of them were on August orders.
- **Card fees (56.59).** Shopify Payments' processing fees. These figures are consistent with each other, but this check does not compare the rates against your contract.
- **One dispute (chargeback).** Order #1060: 19.30 was taken back plus a 15.00 dispute fee. Its net cost is 34.30. If you win it, the amount and possibly the fee come back.

## Not in the payouts at all

Orders paid through PayPal never show up in Shopify Payments payouts. That money lands in your PayPal account, so don't look for it in the payout report. These orders (99.00) are **not** part of the gap above:
#1055 (PayPal Express Checkout)

Every card order matched a charge, and every charge matched an order. There were no split payments, no failed payouts, and no orders from earlier months paid out in August. `bank_checked` is false, so the bank figure comes from the transactions export alone.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- the transactions export starts on 2026-08-01: payouts early in August 2026 may carry earlier transactions it does not have, so the bank figure is not checked; add the payouts export (Finances > Payouts > Export)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.11.0, scripts a07884a2bdbf

## Questions for you

The figures above use the usual answer to each of these questions until you confirm it. A different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
- The transactions export starts on 2026-08-01, so the payouts of the first days of August 2026 may be short of what the bank received. Can you add the payouts export (Finances > Payouts > Export) to check the bank figure?

Checked by payout-reconciliation v0.11.0 · seal 59e5511c87ec
