Here's the checked answer. It's also saved as `files/reconciliation.md`.

---

# August 2026: card sales vs. money in the bank

**Before the figures:**

- The bank figure is not checked: the transactions export starts on 2026-08-01 and the payouts export was not given.

**The gap: €371.08** between card orders placed in August and what Shopify Payments paid out to the bank in August. The bridge below closes to zero: every euro of that gap is explained by refunds, card fees, one dispute and money still in transit on 31 August.

## The bridge

| | Line | EUR |
|---|---|---:|
| | Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − | Refunds processed in August | 70.50 |
| − | Card fees | 56.59 |
| − | Disputes: amount and fees | 19.30 and 15.00 |
| − | Still in transit at month end | 209.69 |
| = | Paid out for August's card transactions | 2,448.74 |
| = | Paid out to the bank in August | 2,448.74 |

No reserve, adjustments, failed payouts or earlier months' transactions appear in the export. Paid out to the bank in August is the figure to check against your bank statement.

## Where the money went

- **Refunds:** 70.50, all on August orders.
- **Card fees:** 56.59 charged by Shopify Payments on the card orders.
- **Dispute (chargeback):** order #1060, amount 19.30 plus a dispute fee of 15.00; the disputes' net cost is 34.30. Nothing has been won back yet.
- **Still in transit at month end** (reaches the bank in early September):

#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)

## Not in the payouts at all

This order was paid with PayPal, so its money goes to your PayPal account, not the Shopify payouts. It is not part of the gap above (99.00 in total):

#1055 (PayPal Express Checkout)

## Unmatched items

None: every card order has a matching charge at the same amount, there are no split payments and no failed payouts. Because the payouts export was not given, the bank figure comes from the transactions alone (not checked against the payouts list).

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

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
- The transactions export starts on 2026-08-01, so the payouts of the first days of August 2026 may be short of what the bank received. Can you add the payouts export (Finances > Payouts > Export) to check the bank figure?

Checked by payout-reconciliation v0.11.0 · seal c094c2a03d5a
