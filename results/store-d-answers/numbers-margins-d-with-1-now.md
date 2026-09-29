I got two figures wrong in my last message: the Canvas Weekender Bag's margin and the count of cancelled orders. The corrected answer is below, filled in directly from the calculation.

Here are July 2026's product margins (USD, revenue without VAT, 7875 orders).

**Lost money (sold below cost): 0 products.** Every product with a cost on file had a positive gross margin. The thinnest was Slim Chino - Navy / 28 (HP-CHN-NVY-28): 62.0% margin, 30 units, 1,655.77 revenue, 1,025.77 gross margin. The biggest earners included Everyday Ankle Socks 5-Pack (11,506.91 gross margin), Canvas Weekender Bag (10,392.39), Polarized Sunglasses - Matte Black (9,081.11) and Polarized Sunglasses - Tortoise (8,333.70).

**Made money:** every other product sold in July (264 SKUs sold in total, minus the unknown-cost ones below).

**Can't tell: 42 products have no cost in the products export.** Their margin is unknown, not zero:
- the Classic Crew Tee, every colour and size (CT-… SKUs): probably renamed. 30 of these sold as CT-… while the products export has the same names under HP-TEE-CLS-… SKUs, e.g. CT-BLK-L vs HP-TEE-CLS-BLK-L (unit cost 7.40). Are they the same product? That cost stays unused until you confirm.
- Heavyweight Hoodie, Forest colour, every size (HP-HWH-FOR-L to HP-HWH-FOR-XXL)
- Linen Bucket Hat - Natural and Linen Bucket Hat - Olive
- items with no SKU: Custom embroidery (initials), Enamel Pin Set, Gift Wrap, Silk Bandana - Navy Dot, Silk Bandana - Paisley

Please send their costs (or confirm the tee SKUs), and I'll rerun it.

**Orders left out: 152** (cancelled, partly paid, payment pending, test gateway); each is listed by order number in the file.

Not spread over products: 27,308.20 in discounts, 83,060.38 in refunds and 9,121.94 in tips and gift cards sold (not products), so product margins are before discounts and refunds. 1420 orders had VAT inside their prices; their own tax was taken out of their lines. VAT removed: each order's own tax, where its prices include it.

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

The full checked answer, with the table of all SKUs, every unknown-cost and renamed SKU, and every left-out order number, is saved as `files/margins_2026-07.md` (seal 9bed6de72011).
