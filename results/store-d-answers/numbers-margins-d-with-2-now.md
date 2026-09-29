**No product with a known cost lost money in July 2026. The margin is unknown for 42 products because the products export has no cost for them.**

These are gross margins on each product: revenue without VAT minus cost per item. Not spread over products: 27,308.20 in discounts, 83,060.38 in refunds and 9,121.94 in tips and gift cards sold (not products).

**Made money:** every other product. Margin % runs from 62.0 (Slim Chino - Navy / 28) to 79.5 (Canvas Cap - Black). Canvas Tote Bag made the largest margin: 8,656.78.

**Lost money (sold below cost):** none.

**Can't tell (42 products, margin unknown, not zero):**
- **Possibly renamed (30 Classic Crew Tee SKUs such as CT-BLK-L).** The products export has the same product name under another SKU, such as HP-TEE-CLS-BLK-L at 7.40. Are they the same product? I haven't used that cost until you confirm.
- **No cost in the products export:** Linen Bucket Hat - Natural, Linen Bucket Hat - Olive, and Heavyweight Hoodie - Forest (HP-HWH-FOR-S to HP-HWH-FOR-XXL).
- **Sold without a SKU:** Custom embroidery (initials) (90.00 revenue), Enamel Pin Set (2,870.52 revenue), Gift Wrap (793.00 revenue), Silk Bandana - Navy Dot (3,334.92 revenue), Silk Bandana - Paisley (3,812.79 revenue).

All of them: (no SKU) Custom embroidery (initials), (no SKU) Enamel Pin Set, (no SKU) Gift Wrap, (no SKU) Silk Bandana - Navy Dot, (no SKU) Silk Bandana - Paisley, CT-BLK-L, CT-BLK-M, CT-BLK-S, CT-BLK-XL, CT-BLK-XS, CT-BLK-XXL, CT-HGR-L, CT-HGR-M, CT-HGR-S, CT-HGR-XL, CT-HGR-XS, CT-HGR-XXL, CT-NVY-L, CT-NVY-M, CT-NVY-S, CT-NVY-XL, CT-NVY-XS, CT-NVY-XXL, CT-OLV-L, CT-OLV-M, CT-OLV-S, CT-OLV-XL, CT-OLV-XS, CT-OLV-XXL, CT-WHT-L, CT-WHT-M, CT-WHT-S, CT-WHT-XL, CT-WHT-XS, CT-WHT-XXL, HP-ACC-BKT-NAT, HP-ACC-BKT-OLV, HP-HWH-FOR-L, HP-HWH-FOR-M, HP-HWH-FOR-S, HP-HWH-FOR-XL, HP-HWH-FOR-XXL

**What's counted:** 7875 orders. 152 orders were left out (cancelled, partly paid, test or payment pending), each listed with its reason in the report. 1420 orders had VAT inside their prices (the store adds tax on top, selling abroad), and their own tax was taken out of their lines. VAT removed: each order's own tax, where its prices include it.

**How this was counted**

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- no VAT rate given: each order's own tax is taken out of its lines where its prices include it (from the export)

- the orders export has records on 31 of 31 days of July 2026
- the orders export's shape is not recorded yet (financial status: authorized, expired, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: USD; payment method: (for testing) Bogus Gateway, Bank Deposit, Cash, Cash on Delivery (COD), Gift Card, PayPal Express Checkout, Shopify Payments, manual; tags: Net 15, Net 30, Subscription, Subscription First Order, Subscription Recurring Order, replacement, test, wholesale)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 58,166 rows, SHA-256 4c14bc07ab3d150c
- products_export.csv: 278 rows, SHA-256 9bfaf73f89f87d36
- computed by shopify-month-end v0.10.1, scripts 632933f9ff3a

**Open questions.** The figures use the usual answers until you confirm them; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

The full checked report, with every product's units, revenue, cost and margin and every excluded order, is saved as `files/margins_2026-07.md`.
