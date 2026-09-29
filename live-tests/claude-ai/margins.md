**Asked:** Which of our products lose money? The Shopify orders export for August and our cost sheet are attached.
(attached: orders_export.csv, cogs.csv) · **Skill used:** sku-margin-check · **Model:** Opus 5.5

---

I'll work out August margin per product from the orders export and your cost sheet, and flag anything sold below cost or missing a cost.

*(Created a file, shared a file, ran 3 commands)*

One product lost money in August: the Steel Strainer. The Gift Set can't be judged yet because it has no cost in your sheet. The full answer is below and attached as a file.

Product margins, August 2026

Warnings: none.

Sold below cost
Steel Strainer (STR-STL-001): 20 units, revenue without VAT 109.24 against cost 142.00, margin -32.76 (-30.0%). It sells for less than its unit cost of 7.10.

Cost unknown
SET-GFT-001 has no cost in the cost sheet, so its margin is unknown, not zero. Gift Set sold 17 units for 700.01 without VAT. What does one set cost you?

Orders left out
test order: #1013; cancelled: #1021

All products
Product SKU Units Revenue ex VAT Cost Margin Margin %
Ceramic Cup CUP-CER-001 14 211.76 105.00 106.76 50.4%
Glass Teapot 600ml POT-GLS-600 19 542.85 302.10 240.75 44.3%
Gift Set SET-GFT-001 17 700.01 unknown unknown unknown
Steel Strainer STR-STL-001 20 109.24 142.00 -32.76 -30.0%
Black Tea 100g TEA-BLK-100 27 260.94 102.60 158.34 60.7%
Green Tea 100g TEA-GRN-100 13 140.93 53.30 87.63 62.2%
Matcha 30g TEA-MAT-030 8 161.35 77.60 83.75 51.9%
Oolong 50g TEA-OOL-050 16 215.13 99.20 115.93 53.9%

Not spread over products: 20.28 in discounts, 70.50 in refunds and 0.00 in tips and gift cards sold.

58 orders had VAT inside their prices, and each order's own tax was taken out of its lines. VAT removed: each order's own tax, where its prices include it. The figures cover 58 orders.

How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- no VAT rate given: each order's own tax is taken out of its lines where its prices include it (from the export)
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- cogs.csv: 7 rows, SHA-256 af53eff44895fecd
- computed by shopify-month-end v0.10.1, scripts 632933f9ff3a

Open questions
The figures use the usual answers below until you confirm them; a different answer changes them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-month-end v0.10.1 · seal 687869e2b04d

*(Output offered for download: Margins, MD)*
