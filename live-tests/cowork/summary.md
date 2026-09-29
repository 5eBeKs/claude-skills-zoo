<!-- Cowork in claude.ai (September 2026), the plugin uploaded as a ZIP (Customize > Plugins > Upload plugin), Opus 5.5 High, store A's orders_export.csv attached. Question: "Hi! Our Shopify orders export for August is attached (orders_export.csv). How did the month go? I need the key numbers for my accountant." The skill fired on its own. Steps shown by the session: Loaded skill shopify-monthly-summary; a first command failed; Find the skill's scripts on disk; Compute August KPIs from the orders export; Created summary.tmpl.md; Render, check and seal the summary; Save the checked summary to outputs; Shared summary_2026-08.md. Copied from the page as text, so Markdown formatting is lost. -->

August went smoothly: 58 orders counted, only one full refund, and gift sets and teapots brought in the most money. Below is the checked summary, exactly as it's in the file above.

August 2026 sales summary

In 2026-08 the store charged €2,918.82 and had €2,848.32 left after refunds. The total charged includes €466.00 of VAT and €151.90 of shipping. The net after refunds still holds most of both (refunds gave some back), so neither figure is profit: VAT is owed to the tax office, and product costs, shipping costs and payment fees have not been taken off.

Figure 2026-08
Total charged €2,918.82
Refunds €70.50
Net after refunds €2,848.32
Orders counted 58
Refunded orders 1
Average order value €50.32
Refund rate 2.4%
Units sold 134
VAT inside the total €466.00
Shipping charged €151.90
Discounts given €20.28

Revenue as the store defines it: €2,918.82 (VAT included, shipping included, partial refunds as amount). 6 orders had a discount.

Top products (line price x quantity, before order discounts, VAT included when prices include it)

Gift Set: €833.00
Glass Teapot 600ml: €646.00
Black Tea 100g: €310.50
Oolong 50g: €256.00
Ceramic Cup: €252.00

Left out: 2 orders, test order: #1013; cancelled: #1021. Orders are placed in the month by order Created at, as written in the export, and refunds are counted in the month of their order.

How this was counted

orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
a sale counts once it is paid, shipped or not (the usual answer; please confirm)
revenue is reported with VAT, as customers paid (the usual answer; please confirm)
the shipping customers pay is part of revenue (the usual answer; please confirm)
a partial refund takes off only the amount refunded (the usual answer; please confirm)
a refund belongs to the month of its order (the usual answer; please confirm)

Computed from:

the orders export has records on 25 of 31 days of August 2026
the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
Subtotal in this export is before discounts (6 orders)
checked against nothing outside the export: give a figure from Shopify or the bank to check it
orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
computed by shopify-month-end v0.11.7, scripts ab61cfedc85c

Questions for you (the figures above use the usual answers until you confirm them)

Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
Does a sale count when it is paid, or only once it is shipped?
Should revenue be reported with VAT, as the customer paid, or without VAT?
Is the shipping fee customers pay part of revenue, or kept out of it?
A partially refunded order: is it still a sale (usual), or a refunded order? Either way only the amount refunded comes off.
A refund belongs to the month of the order (this export can only do that), or the month of the refund?
The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-monthly-summary v0.11.7 · seal 63a5a5f5da7c

The questions at the end are worth a quick look with your accountant, especially whether they want revenue reported with or without VAT. Once you've answered them, I'll re-run the numbers on those rules, and they'll stay fixed for September. If you also have the Shopify Payments payout export, I can show how these sales line up with what actually reached your bank.
