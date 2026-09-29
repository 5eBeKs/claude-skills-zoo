One product lost money in August: the Steel Strainer (STR-STL-001). A second, the Gift Set (SET-GFT-001), isn't in `cogs.csv`, so I can't tell whether it made or lost money. All other products are profitable. Amounts are in EUR with 19% VAT taken out. This is the answer as generated and checked:

## Product margins, August 2026

**Sold below cost:** Steel Strainer, **STR-STL-001**: 20 units, revenue without VAT 109.24, cost 142.00, margin **-32.76** (-30.0%). At a cost of 7.10 per unit, it sells for less than it costs.

**Cost unknown:** Gift Set, **SET-GFT-001**: 17 units, revenue without VAT 700.00. It is not in cogs.csv, so its margin is unknown, not zero. What does one Gift Set cost you?

Orders left out: test order: #1013; cancelled: #1021

| Product | SKU | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---|---|---|---|---|---|
| Steel Strainer | STR-STL-001 | 20 | 109.24 | 142.00 | -32.76 | -30.0% |
| Gift Set | SET-GFT-001 | 17 | 700.00 | unknown | unknown | unknown |
| Ceramic Cup | CUP-CER-001 | 14 | 211.76 | 105.00 | 106.76 | 50.4% |
| Glass Teapot 600ml | POT-GLS-600 | 19 | 542.86 | 302.10 | 240.76 | 44.4% |
| Black Tea 100g | TEA-BLK-100 | 27 | 260.92 | 102.60 | 158.32 | 60.7% |
| Green Tea 100g | TEA-GRN-100 | 13 | 140.92 | 53.30 | 87.62 | 62.2% |
| Matcha 30g | TEA-MAT-030 | 8 | 161.34 | 77.60 | 83.74 | 51.9% |
| Oolong 50g | TEA-OOL-050 | 16 | 215.13 | 99.20 | 115.93 | 53.9% |

Not spread over products: 20.28 in discounts, 70.50 in refunds and 0.00 in tips and gift cards sold (not products). Margins above are before these.

VAT rate taken out of prices: 0.19. The figures cover 58 orders.

### How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- prices include VAT at 19% (as given)
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- cogs.csv: 7 rows, SHA-256 af53eff44895fecd
- computed by shopify-month-end v0.11.0, scripts 6afa94c9bf8c

### Open questions
The figures use the usual answers below until you confirm them; a different answer changes them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by sku-margin-check v0.11.0 · seal 90f9cbac0423
