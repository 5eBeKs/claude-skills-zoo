In August one product definitely lost money: the **Steel Strainer**, which sold below its unit cost. I can't tell yet whether the **Gift Set** made or lost money, because cogs.csv has no cost for it. Every other product had a margin between about 44% and 62%. The checked answer is below:

---

# Product margins, August 2026

## Sold below cost

- **Steel Strainer (STR-STL-001)**: 20 units, revenue without VAT 109.24, cost 142.00, gross margin -32.76 (-30.0%). Unit cost is 7.10.

## Cost unknown

- SET-GFT-001: 17 units, revenue without VAT 700.00. Its margin is unknown, not zero: please send its unit cost.

## All products

| SKU | Product | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---|---|---|---|---|---|
| CUP-CER-001 | Ceramic Cup | 14 | 211.76 | 105.00 | 106.76 | 50.4% |
| POT-GLS-600 | Glass Teapot 600ml | 19 | 542.86 | 302.10 | 240.76 | 44.4% |
| SET-GFT-001 | Gift Set | cost unknown, see above | | | | |
| STR-STL-001 | Steel Strainer | 20 | 109.24 | 142.00 | -32.76 | -30.0% |
| TEA-BLK-100 | Black Tea 100g | 27 | 260.92 | 102.60 | 158.32 | 60.7% |
| TEA-GRN-100 | Green Tea 100g | 13 | 140.92 | 53.30 | 87.62 | 62.2% |
| TEA-MAT-030 | Matcha 30g | 8 | 161.34 | 77.60 | 83.74 | 51.9% |
| TEA-OOL-050 | Oolong 50g | 16 | 215.13 | 99.20 | 115.93 | 53.9% |

Not spread over products: 20.28 in discounts, 70.50 in refunds and 0.00 in tips and gift cards sold (not products).

VAT rate taken out of prices: 0.19. Orders counted: 58.

Orders left out:
test order: #1013; cancelled: #1021

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- prices include VAT at 19% (as given)

- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- cogs.csv: 7 rows, SHA-256 af53eff44895fecd
- computed by shopify-month-end v0.11.6, scripts db4321daa942

## Open questions

These figures use the usual answers until you confirm them; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by sku-margin-check v0.11.6 · seal b3e639d9254a

---

**Next steps:**
- **Gift Set cost:** it had the most revenue of any product in August, so its cost matters most. Send me its unit cost and I'll rerun this.
- **Open questions above:** please answer them. Once you confirm the export looks as expected, I'll save it as the reference so any change next month gets flagged.
