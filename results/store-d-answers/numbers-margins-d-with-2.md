# July 2026 product margins (USD)

**No product lost money in July.** Every product whose cost is in your products export sold above that cost. For 42 SKUs I can't tell, because they have no cost on file.

I read your data as a store that adds tax on top of its prices, so I didn't take any VAT out of the price. The export's totals show this: for US and Canadian orders, subtotal + shipping + tax = total. For the 1420 UK/EU orders, VAT was inside the price, so each order's own tax was taken out of its lines. The figures cover 7875 orders, and the export has records on every day of July.

## Made money
Every SKU with a known cost had a positive gross margin (revenue without tax, minus units × Cost per item). The table of all SKUs, with units, revenue, cost, margin and margin %, is in `files/margins_2026-07.md`.

## Lost money
None. No product with a known cost sold below that cost.

## Can't tell: 42 SKUs with no cost on file
Their margin is unknown, not zero.

| SKU | Product | Units | Revenue ex tax |
|---|---|---:|---:|
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

The other **30 are Classic Crew Tee SKUs** in every colour and size, sold under old `CT-…` SKUs such as `CT-BLK-L`. Your products export has the same product names under new `HP-TEE-CLS-…` SKUs. **Are these the same products?** If you say yes, I'll use the new SKUs' cost and re-run. Until then their margin stays unknown.

## What the margins don't include
- **Not spread over products:** $27,308.20 in order discounts, $83,060.38 in refunds, and $9,121.94 in tips and gift cards sold. Product margins are before these amounts.
- **Orders left out:** 152, covering cancelled orders, test-gateway orders, partly paid orders and one pending payment. The full list with reasons is in the saved file.
- **Costs on file but no July sales:** the eight `HP-VST-SHR-…` SKUs.
- **Checks:** nothing was checked against a figure from outside the export. A Shopify or bank total would let me cross-check.

## Questions for you
These answers change the figures. Until you confirm them, I've used the usual ones:
- **Test orders:** should orders tagged `test` or paid through the test gateway stay out of sales? I've left them out.
- **When a sale counts:** is it when the order is paid, or only once it ships? I've counted it when paid.
- **Export columns:** are the payment methods, statuses, tags and currency listed in the saved file all as expected? If they are, I'll save them as the export's normal layout, so any new value is flagged next month.
- **Missing costs:** can you send costs for the 12 products in the table above?

The full report, which passed the plugin's number check, is saved at `files/margins_2026-07.md`.
