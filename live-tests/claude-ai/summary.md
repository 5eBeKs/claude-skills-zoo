**Asked:** How did August go? I need the numbers for my accountant. Our Shopify orders export is attached.
(attached: orders_export.csv) · **Skill used:** shopify-monthly-summary · **Model:** Opus 5.5 · **Build:** earlier than 0.10.1 (seal v0.9.0)

---

I'll run the August month-end summary from your orders export.

*(Created a file, shared a file, ran 6 commands)*

Sales summary, 2026-08

In 2026-08 the store charged €2,918.82 and had €2,848.32 left after refunds. The total charged includes €466.00 of VAT and €151.90 of shipping; the net after refunds still holds most of both (refunds gave some back), so neither figure is profit.

Figure Amount
Total charged €2,918.82
Refunds €70.50
Net after refunds €2,848.32
Orders counted 58
Average order value €50.32
Refund rate 2.4%
Units sold 134
VAT inside the total €466.00
Shipping charged €151.90
Discounts given €20.28

Revenue as the store defines it: €2,918.82 (VAT included, shipping included, partial refunds as amount). 6 orders had a discount. Refunded orders: #1030, #1042.

Top products
By line price x quantity, before order discounts, VAT included when prices include it:
Product Units Revenue
Gift Set 17 €833.00
Glass Teapot 600ml 19 €646.00
Black Tea 100g 27 €310.50
Oolong 50g 16 €256.00
Ceramic Cup 14 €252.00

What was left out
2 orders were left out: test order: #1013; cancelled: #1021. Orders are placed in the month by order Created at, as written in the export, and refunds are counted in the month of their order.

How this was counted
These are the usual definitions, used until you confirm them:
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

What the figures were computed from:
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- Subtotal in this export is before discounts (6 orders)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- computed by shopify-month-end vunknown, scripts b47bf500c7d0

Questions for you
The figures above use the usual answers until you confirm them:
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-month-end v0.9.0 · seal 809a5fe40239

*(Output offered for download: Summary 2026 08, MD)*
