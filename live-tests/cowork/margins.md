<!-- Cowork in claude.ai (September 2026), the plugin 0.11.7 uploaded as a ZIP, Opus 5.5 High, store A's orders_export.csv and cogs.csv attached. Question: "Which of our products actually lose money? The August orders export and our unit costs (cogs.csv) are attached. Prices include 19% VAT." The skill fired on its own; the session shows "Edited a file, created a file, and 9 more steps". Copied from the page as text, so Markdown formatting is lost. -->

One product loses money: the Steel Strainer. Gift Set can't be judged yet because it has no cost in your sheet. All amounts are in EUR.

Sold below cost
Steel Strainer (STR-STL-001): 20 units sold for 109.24 without VAT, against a cost of 142.00. Gross margin -32.76 (-30.0%). Its unit cost of 7.10 is above what it sells for once VAT is taken out, so every unit sold loses money before shipping or fees.
Cost unknown
SET-GFT-001: no cost in cogs.csv, so its margin is unknown, not zero. It is the biggest product by revenue here (17 units, 700.00 without VAT), so its cost is worth adding: send it and I'll rerun.
Orders left out

test order: #1013; cancelled: #1021

All products (August 2026, prices without VAT)
Product Units Revenue Cost Margin Margin %
Black Tea 100g (TEA-BLK-100) 27 260.92 102.60 158.32 60.7%
Green Tea 100g (TEA-GRN-100) 13 140.92 53.30 87.62 62.2%
Oolong 50g (TEA-OOL-050) 16 215.13 99.20 115.93 53.9%
Matcha 30g (TEA-MAT-030) 8 161.34 77.60 83.74 51.9%
Ceramic Cup (CUP-CER-001) 14 211.76 105.00 106.76 50.4%
Glass Teapot 600ml (POT-GLS-600) 19 542.86 302.10 240.76 44.4%
Steel Strainer (STR-STL-001) 20 109.24 142.00 -32.76 -30.0%
Gift Set, cost unknown 17 700.00

Not spread over products: 20.28 in discounts, 70.50 in refunds and 0.00 in tips and gift cards sold (not products). Product margins above are before these, and before shipping and payment fees.

VAT rate taken out of prices: 0.19. The figures cover 58 orders.

How this was counted
orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
a sale counts once it is paid, shipped or not (the usual answer; please confirm)
prices include VAT at 19% (as given)
the orders export has records on 25 of 31 days of August 2026
the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
checked against nothing outside the export: give a figure from Shopify or the bank to check it
orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
cogs.csv: 7 rows, SHA-256 af53eff44895fecd
computed by shopify-month-end v0.11.7, scripts db4321daa942
Open questions

The figures use the usual answers below until you confirm them; a different answer changes them.

Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
Does a sale count when it is paid, or only once it is shipped?
The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by sku-margin-check v0.11.7 · seal 536706c89aa8
