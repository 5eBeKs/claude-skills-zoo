**Asked:** We sold more in August than reached the bank. Where did the money go? The orders export and the Shopify Payments payout transactions are attached.
(attached: orders_export.csv, payout_transactions.csv) · **Skill used:** payout-reconciliation · **Model:** Opus 5.5 · **Build:** earlier than 0.10.1 (seal v0.9.0)

---

I'll reconcile August's orders against the Shopify Payments payouts and build a bridge showing where the difference went.

*(Created a file, shared a file, ran 6 commands)*

August: card sales vs. money in the bank

The gap is €371.08: card orders placed in August against what Shopify paid out to the bank in August. Nothing is missing: the bridge below closes with an unexplained difference of €0.00.

Before the figures:

The bank figure is not checked: the transactions export starts on 2026-08-01 and the payouts export was not given.

In short, the gap is refunds, card fees, one lost dispute, and the last days of August still on their way to the bank.

The bridge
Line Amount
Card orders placed in August (Shopify Payments, shipped yet or not) €2,819.82
Refunds processed in August −€70.50
Card fees −€56.59
Disputes: amount and fees −€19.30 and −€15.00
Reserve held (-) or released (+) by Shopify €0.00
Failed payout paid again €0.00
Shopify adjustments €0.00
Still in transit at month end −€209.69
Paid out for August's card transactions €2,448.74
Paid out to the bank in August €2,448.74

The last line is the figure to look for on your bank statement for August.

What's behind each line

The dispute. Order #1060 was disputed by the customer: Shopify took back the order amount of €19.30 plus a dispute fee of €15.00, so the dispute's total cost was €34.30. If it can still be contested in Shopify, winning it would return the amount.

Still in transit at month end. These card sales were paid out in the first days of September, so they will be on September's bank statement, not August's:
#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)

Paid outside Shopify Payments. This order was paid by PayPal, so its money went to your PayPal account and never appears in Shopify payouts. It is not part of the card figures above:
#1055 (PayPal Express Checkout)

Unmatched items. Every counted card order has a matching charge at the same amount, and every charge matches a counted order. There were no failed payouts, reserves, adjustments or split payments.

How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- the transactions export starts on 2026-08-01: payouts early in August 2026 may carry earlier transactions it does not have, so the bank figure is not checked; add the payouts export (Finances > Payouts > Export)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end vunknown, scripts d5907b24d784

Questions for you
The figures above use the usual answer to each of these until you confirm it; a different answer changes them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
- The transactions export starts on 2026-08-01, so the payouts of the first days of August 2026 may be short of what the bank received. Can you add the payouts export (Finances > Payouts > Export) to check the bank figure?

Checked by shopify-month-end v0.9.0 · seal 3e907d2cc678

*(Output offered for download: Reconciliation 2026 08, MD)*
