I checked every product's July margin against the costs in your products export. **No product with a known cost lost money in July. For 42 SKUs I can't tell, because they have no cost in the products export.** The full report with every figure is saved at `files/margins_2026-07.md` and passed the number check. Below is the short version. Long lists are shortened here and appear in full in that file.

---

## Lost money (sold below cost)

**None.** Every product with a known cost sold above that cost in July. The thinnest margin was HP-CHN-NVY-28 (Slim Chino - Navy / 28): 30 units, revenue $1,655.77, margin $1,025.77 (62.0%).

## Made money

264 SKUs sold in July. Every one that has a cost in the products export made money. These margins are before discounts, refunds, shipping, fees and ads. The full per-SKU table is in the saved file.

## Can't tell: no cost in the products export (42 SKUs)

Their margin is unknown, not zero. Please send their unit costs.

**Classic Crew Tee under older SKUs (30 SKUs).** July orders use `CT-…` SKUs. The products export has the same product names under `HP-TEE-CLS-…`, with a cost. Are they the same product? Until you say so, I don't use the `HP-TEE-CLS-…` cost for them. Each pair is listed in the saved file.

**Other products with no cost:**

| SKU | Name | Units | Revenue |
|---|---|--:|--:|
| (no SKU) | Custom embroidery (initials) | 6 | 90.00 |
| (no SKU) | Enamel Pin Set | 221 | 2,870.52 |
| (no SKU) | Gift Wrap | 133 | 793.00 |
| (no SKU) | Silk Bandana - Navy Dot | 101 | 3,334.92 |
| (no SKU) | Silk Bandana - Paisley | 115 | 3,812.79 |
| HP-ACC-BKT-NAT | Linen Bucket Hat - Natural | 70 | 2,440.78 |
| HP-ACC-BKT-OLV | Linen Bucket Hat - Olive | 78 | 2,715.84 |
| HP-HWH-FOR-L | Heavyweight Hoodie - Forest / L | 37 | 3,055.97 |
| HP-HWH-FOR-M | Heavyweight Hoodie - Forest / M | 37 | 3,040.30 |
| HP-HWH-FOR-S | Heavyweight Hoodie - Forest / S | 25 | 2,047.79 |
| HP-HWH-FOR-XL | Heavyweight Hoodie - Forest / XL | 20 | 1,653.91 |
| HP-HWH-FOR-XXL | Heavyweight Hoodie - Forest / XXL | 3 | 252.00 |

## Not included in the per-product figures

These amounts are not split across products: $27,308.20 in discounts, $83,060.38 in refunds, and $9,121.94 in tips and gift cards sold. The refunds are large, so a product's real margin can be lower than shown.

Eight Sherpa vest SKUs (HP-VST-SHR-BLK/OAT, sizes S–XL) have a cost but had no July sales.

## Orders left out

152 orders were left out because they were cancelled, partly paid, paid through the test gateway, or still pending payment. Each order and its reason is in the saved file.

## How this was counted

- The figures cover 7,875 orders created in July 2026. The export has orders on all 31 days of July.
- I treated your prices as excluding tax (rate 0). There was no `store_definitions.json` to say otherwise, so I read this from the export: US and Canadian orders have tax added on top of the price. For 1,420 UK and EU orders, VAT was inside the price, so I took each order's own tax out of its lines.
- I haven't checked these figures against anything outside the export, such as a total from Shopify or your bank.

## Questions for you

The figures use the usual answers below until you confirm them. A different answer changes the figures.

- **Tax:** Is it right that your prices exclude tax, with US/Canadian tax added on top?
- **Test orders:** Should orders tagged `test` or paid through Shopify's test gateway stay out of sales (the usual answer), or be counted?
- **When a sale counts:** Does a sale count once it's paid (the usual answer), or only once it has shipped?
- **Export values:** Are the order statuses, payment methods, tags and currencies in this export all as expected? They're listed in the saved file. If you confirm them, I'll save them as `store_shape.json`, and any new value next month will be flagged.
