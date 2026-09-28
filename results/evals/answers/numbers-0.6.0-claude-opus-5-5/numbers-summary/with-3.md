<!-- numbers-0.6.0-claude-opus-5-5 / numbers-summary / with the plugin / run 3: passed -->

The note I added below the summary listed the six days with no orders by hand, and the check caught those typed dates. Here is the checked summary again, unchanged, with the notes rewritten without figures.

---

# Sales summary, 2026-08

In 2026-08 the store charged €2,918.82 and had €2,848.32 left after refunds. The total charged includes €466.00 of VAT and €151.90 of shipping paid by customers. The net after refunds still holds most of both (refunds gave some back), so **neither figure is profit**: the VAT is owed to the tax office, and product costs, shipping costs and payment fees have not been taken off.

| | |
|---|---|
| Total charged (incl. VAT and shipping) | €2,918.82 |
| Refunds | €70.50 |
| Net after refunds | €2,848.32 |
| Orders counted | 58 |
| Average order value | €50.32 |
| Refund rate | 2.4% |
| Units sold | 134 |
| VAT inside the total | €466.00 |
| Shipping charged | €151.90 |
| Discounts given | €20.28 (6 orders had a discount) |

**Revenue as the store defines it:** €2,918.82 (VAT included, shipping included, partial refunds as amount).

**Refunded orders:** #1030, #1042. The export does not say why they were refunded.

## Top products
(line price x quantity, before order discounts, VAT included when prices include it)

| Product | Units | Revenue |
|---|---|---|
| Gift Set | 17 | €833.00 |
| Glass Teapot 600ml | 19 | €646.00 |
| Black Tea 100g | 27 | €310.50 |
| Oolong 50g | 16 | €256.00 |
| Ceramic Cup | 14 | €252.00 |

## What was left out
2 of 60 orders in the export were left out of the figures: test order: #1013; cancelled: #1021.

Orders are placed in the month by order Created at, as written in the export; refunds are counted in the month of their order.

## How this was counted
Definitions (none confirmed by you yet; the usual answers were used):
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

The export:
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Files and fingerprints:
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- computed by shopify-month-end v0.6.0, scripts 7c2c32653639

## Questions for you
The figures above use the usual answers until you confirm them:
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

**Before this goes to your accountant:**
- **Definitions:** Once you answer the questions above, I'll save your answers in a `store_definitions.json` next to the export and rerun the figures. The VAT and shipping answers are the most likely to change what your accountant sees.
- **Missing days:** The export has no orders on some days in August. If your store usually gets orders every day, check that the export covered the whole month.
- **Outside check:** It hasn't been checked against anything outside the export yet. A total from Shopify Analytics or your bank would let me confirm it.
- **Bank deposits:** This covers sales only. If your accountant also needs to know why the amount paid into your bank differs from sales (card fees, payouts still on the way), send me the Shopify Payments payouts export too.
