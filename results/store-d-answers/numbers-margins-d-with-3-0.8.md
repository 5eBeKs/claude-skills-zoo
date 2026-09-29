**July 2026: no product with a known cost lost money. Every one of them made money, and 42 products can't be judged because they have no cost.** No warnings came up in the checks, and the export has records on 31 of 31 days of July.

## Made money
Every product with a cost in the products export sold above cost. The lowest margin was Slim Chino - Navy / 28 at 62.0%. By gross margin, the top earners were:

| Product | Units | Revenue ex VAT | Margin | Margin % |
|---|---:|---:|---:|---:|
| Everyday Ankle Socks 5-Pack | 706 | $15,036.91 | $11,506.91 | 76.5% |
| Canvas Weekender Bag | 108 | $15,360.39 | $10,392.39 | 67.7% |
| Polarized Sunglasses - Matte Black | 144 | $11,817.11 | $9,081.11 | 76.8% |
| Canvas Tote Bag | 406 | $11,092.78 | $8,656.78 | 78.0% |
| Polarized Sunglasses - Tortoise | 131 | $10,822.70 | $8,333.70 | 77.0% |

## Lost money
None: 0 products with a known cost sold below cost.

## Can't tell: 42 products with no cost
Their margin is unknown, not zero.

- **30 Classic Crew Tee variants (`CT-…`): may have been renamed.** They sold under `CT-…` SKUs, but your products export has the same product names under `HP-TEE-CLS-…` SKUs, at $7.40 each. **Are they the same product?** I didn't use that cost until you confirm.
- **The rest have no cost at all:** (no SKU) Custom embroidery (initials), (no SKU) Enamel Pin Set, (no SKU) Gift Wrap, (no SKU) Silk Bandana - Navy Dot, (no SKU) Silk Bandana - Paisley, HP-ACC-BKT-NAT, HP-ACC-BKT-OLV, HP-HWH-FOR-L, HP-HWH-FOR-M, HP-HWH-FOR-S, HP-HWH-FOR-XL, HP-HWH-FOR-XXL.
- Your products export has costs for SKUs that didn't sell in July (HP-VST-SHR-BLK-L, HP-VST-SHR-BLK-M, HP-VST-SHR-BLK-S, HP-VST-SHR-BLK-XL, HP-VST-SHR-OAT-L, HP-VST-SHR-OAT-M, HP-VST-SHR-OAT-S, HP-VST-SHR-OAT-XL). I haven't assumed they're related.

Please send the missing costs, or confirm the tee mapping, and I'll rerun.

## Things to know about these figures
- **Orders counted:** the figures cover 7875 orders. I left out 152 that were cancelled, only partly paid, test orders or still pending payment. The report file lists each one with its reason.
- **Not included in product margins:** $27,308.20 in discounts, $83,060.38 in refunds and $9,121.94 in tips and gift cards sold. They aren't split across products, so the margins above are before them.
- **VAT:** 1420 orders had VAT inside their prices. With no rate given, VAT removed: each order's own tax, where its prices include it.
- **Checks:** checked against nothing outside the export: give a figure from Shopify or the bank to check it.

**Warnings:**
- none

**How this was counted:**
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- no VAT rate given: each order's own tax is taken out of its lines where its prices include it (the usual answer; please confirm)
- orders_export.csv: 58,166 rows, SHA-256 4c14bc07ab3d150c
- products_export.csv: 278 rows, SHA-256 9bfaf73f89f87d36
- computed by shopify-month-end v0.8.0, scripts a2577a534305

**Questions for you.** The figures use the usual answers until you confirm; a different answer changes them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

The full report is saved as `files/margins_2026-07.md`, with all 264 products and every order that was left out.
