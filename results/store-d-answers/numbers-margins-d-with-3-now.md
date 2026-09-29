# Product margins, July 2026

**Lost money:** none. 0 SKUs were sold below cost. This is gross margin (revenue without VAT minus cost per item); discounts, refunds and fees are not spread over products.

**Made money:** every SKU with a known cost had a positive gross margin. All figures for all SKUs are in `files/margins_2026-07.md`.

**Can't tell:** 42 SKUs have no known cost. Their margin is unknown, not zero; please send the costs:
(no SKU) Custom embroidery (initials), (no SKU) Enamel Pin Set, (no SKU) Gift Wrap, (no SKU) Silk Bandana - Navy Dot, (no SKU) Silk Bandana - Paisley, CT-BLK-L, CT-BLK-M, CT-BLK-S, CT-BLK-XL, CT-BLK-XS, CT-BLK-XXL, CT-HGR-L, CT-HGR-M, CT-HGR-S, CT-HGR-XL, CT-HGR-XS, CT-HGR-XXL, CT-NVY-L, CT-NVY-M, CT-NVY-S, CT-NVY-XL, CT-NVY-XS, CT-NVY-XXL, CT-OLV-L, CT-OLV-M, CT-OLV-S, CT-OLV-XL, CT-OLV-XS, CT-OLV-XXL, CT-WHT-L, CT-WHT-M, CT-WHT-S, CT-WHT-XL, CT-WHT-XS, CT-WHT-XXL, HP-ACC-BKT-NAT, HP-ACC-BKT-OLV, HP-HWH-FOR-L, HP-HWH-FOR-M, HP-HWH-FOR-S, HP-HWH-FOR-XL, HP-HWH-FOR-XXL

Possibly renamed: 30 Classic Crew Tee SKUs sold under `CT-…` codes, while your products export has the same product names under `HP-TEE-CLS-…` codes at 7.40 each: CT-BLK-L, CT-BLK-M, CT-BLK-S, CT-BLK-XL, CT-BLK-XS, CT-BLK-XXL, CT-HGR-L, CT-HGR-M, CT-HGR-S, CT-HGR-XL, CT-HGR-XS, CT-HGR-XXL, CT-NVY-L, CT-NVY-M, CT-NVY-S, CT-NVY-XL, CT-NVY-XS, CT-NVY-XXL, CT-OLV-L, CT-OLV-M, CT-OLV-S, CT-OLV-XL, CT-OLV-XS, CT-OLV-XXL, CT-WHT-L, CT-WHT-M, CT-WHT-S, CT-WHT-XL, CT-WHT-XS, CT-WHT-XXL. Are they the same products? That cost is not used until you confirm.

Not in any product's margin: 27,308.20 in discounts, 83,060.38 in refunds and 9,121.94 in tips and gift cards sold (not products).

1420 orders had VAT inside their prices (a store that adds tax on top, selling abroad); their own tax was taken out of their lines. VAT removed: each order's own tax, where its prices include it. Figures cover 7875 orders.

Orders left out (152): cancelled: #63887, #63829, #63806, #63801, #63770, #63738, #63690, #63680, #63637, #63594, #63583, #63508, #63459, #63449, #63407, #63392, #63143, #63124, #63097, #63090, #63076, #62795, #62775, #62737, #62720, #62638, #62546, #62410, #62352, #61949, #61930, #61927, #61768, #61687, #61637, #61636, #61628, #61593, #61575, #61543, #61541, #61383, #61335, #61329, #61308, #61295, #61162, #61130, #61049, #60903, #60814, #60740, #60572, #60549, #60533, #60504, #60341, #60297, #60286, #60229, #60214, #60197, #60141, #60131, #60128, #60100, #60065, #59979, #59968, #59965, #59948, #59870, #59860, #59838, #59837, #59780, #59757, #59756, #59634, #59396, #59392, #59361, #59317, #59276, #59264, #59213, #59202, #59142, #59104, #59069, #58998, #58821, #58801, #58800, #58681, #58673, #58649, #58369, #58319, #58258, #58232, #58175, #58142, #58095, #58075, #58045, #57993, #57961, #57953, #57936, #57882, #57861, #57628, #57616, #57496, #57479, #57416, #57294, #57293, #57205, #57177, #57172, #57170, #57161, #57077, #57007, #56975, #56933, #56924, #56902, #56743, #56586, #56555, #56437, #56319, #56267, #56120, #56028, #56005, #55965, #55886; partly paid: the export's Total is not what was received: #63532, #62143, #60731, #59100, #56556, #56493; payment pending, not a sale yet: #62794; test order (test payment gateway): #61410, #61407, #61405, #61399

## How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- no VAT rate given: each order's own tax is taken out of its lines where its prices include it (from the export)
- the orders export has records on 31 of 31 days of July 2026
- the orders export's shape is not recorded yet (financial status: authorized, expired, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: USD; payment method: (for testing) Bogus Gateway, Bank Deposit, Cash, Cash on Delivery (COD), Gift Card, PayPal Express Checkout, Shopify Payments, manual; tags: Net 15, Net 30, Subscription, Subscription First Order, Subscription Recurring Order, replacement, test, wholesale)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 58,166 rows, SHA-256 4c14bc07ab3d150c
- products_export.csv: 278 rows, SHA-256 9bfaf73f89f87d36
- computed by shopify-month-end v0.10.1, scripts 632933f9ff3a

## Open questions
The figures use the usual answers until you confirm them; a different answer changes them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-month-end v0.10.1 · seal 41611f556ef6
