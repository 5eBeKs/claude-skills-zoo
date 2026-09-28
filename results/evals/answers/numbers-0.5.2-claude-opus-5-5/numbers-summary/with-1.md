<!-- numbers-0.5.2-claude-opus-5-5 / numbers-summary / with the plugin / run 1: passed -->

August went well. The store took **€2,918.82** in 58 orders and refunded only €70.50, leaving **€2,848.32**. Every figure below comes from the plugin's scripts, and a separate check traced each number in the text back to them. It passed. The export itself had no internal inconsistencies.

# Sales summary, 2026-08

In 2026-08 the store charged **€2,918.82** and had **€2,848.32** left after refunds. The total charged includes €466.00 of VAT and €151.90 of shipping. The net after refunds still holds most of both, since refunds gave only part of them back. Neither figure is profit: the VAT is owed to the tax office, and product costs, shipping costs and payment fees have not been subtracted.

| Figure | Amount |
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

Refunds came from 2 orders: #1030 and #1042. The export does not say why.

## Top products

Ranked by product revenue (line price × quantity, before order discounts, VAT included when prices include it):

1. Gift Set: 17 units, €833.00
2. Glass Teapot 600ml: 19 units, €646.00
3. Black Tea 100g: 27 units, €310.50
4. Oolong 50g: 16 units, €256.00
5. Ceramic Cup: 14 units, €252.00

## Left out

2 of the 60 orders in the export were left out: test order #1013 and cancelled order #1021.

Orders are placed in the month by their "Created at" date, as written in the export. Refunds are counted in the month of their order, not the month the money went back.

## How this was counted

Definitions (you haven't confirmed any of these yet):

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

Files and version:

- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- computed by shopify-month-end v0.5.2, scripts ae0423f29e4e

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

**For your accountant:** The VAT question matters most. If they want revenue without VAT, tell me and I'll rerun it. It would also help to have one total from outside the export, like the total from Shopify's own report or the bank. So far the figures have only been checked against the export itself. This summary covers sales only, not what reached the bank. If you share your Shopify Payments payout export, I can reconcile the two.
