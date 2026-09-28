<!-- numbers-0.6.0-claude-opus-5-5 / numbers-margins / with the plugin / run 2: passed -->

Only one product lost money in August: the Steel Strainer. It sold 20 units for less than they cost. One other product, the Gift Set, isn't in `cogs.csv`, so I can't tell whether it made money. The full report is below, and every figure in it was traced back to the export and cost sheet.

## Product margins, 2026-08 (EUR, excluding VAT)

**Sold below cost:**
- **Steel Strainer (STR-STL-001)**: 20 units, revenue 109.24 ex VAT against cost 142.00 (7.10 each), margin **-32.76 (-30.0%)**.

**Cost unknown:** SET-GFT-001. Gift Set sold 17 units for 700.00 ex VAT, but it is not in cogs.csv, so its margin is unknown (not zero). Please send its unit cost.

**Orders left out:** test order: #1013; cancelled: #1021.

| SKU | Product | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---|---:|---:|---:|---:|---:|
| STR-STL-001 | Steel Strainer | 20 | 109.24 | 142.00 | -32.76 | -30.0% |
| SET-GFT-001 | Gift Set | 17 | 700.00 | unknown | unknown | unknown |
| POT-GLS-600 | Glass Teapot 600ml | 19 | 542.86 | 302.10 | 240.76 | 44.4% |
| CUP-CER-001 | Ceramic Cup | 14 | 211.76 | 105.00 | 106.76 | 50.4% |
| TEA-MAT-030 | Matcha 30g | 8 | 161.34 | 77.60 | 83.74 | 51.9% |
| TEA-OOL-050 | Oolong 50g | 16 | 215.13 | 99.20 | 115.93 | 53.9% |
| TEA-BLK-100 | Black Tea 100g | 27 | 260.92 | 102.60 | 158.32 | 60.7% |
| TEA-GRN-100 | Green Tea 100g | 13 | 140.92 | 53.30 | 87.62 | 62.2% |

Not spread over products: 20.28 in order-level discounts and 70.50 in refunds. VAT removed at 0.19; figures cover 58 orders.

### How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- prices include VAT at 19% (as given)
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- cogs.csv: 7 rows, SHA-256 af53eff44895fecd
- computed by shopify-month-end v0.6.0, scripts 71e84560c08d

### Open questions
The figures use the usual answers below until you confirm them; a different answer changes them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
