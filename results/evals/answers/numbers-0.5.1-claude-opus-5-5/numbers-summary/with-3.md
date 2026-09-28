<!-- numbers-0.5.1-claude-opus-5-5 / numbers-summary / with the plugin / run 3: passed -->

August went through without data issues: the export is internally consistent, it covers 1–31 August with no late start or early stop, and every figure below has been checked against the calculation. It hasn't been checked against anything outside the export, though. A total from Shopify or the bank would let me confirm it.

---

## August 2026 — sales summary

In 2026-08 the store charged €2,918.82 and had €2,848.32 left after refunds. The total charged includes €466.00 of VAT and €151.90 of shipping. The net after refunds still holds most of both, because refunds only gave some of it back. **Neither figure is profit.** Product costs, fees, VAT owed and shipping costs have not been subtracted.

| | |
|---|---|
| Total charged | €2,918.82 |
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

**Refunds:** #1030 (partially_refunded, €10.00) and #1042 (refunded, €60.50). The export does not say why they were refunded.

### Top products
Product revenue is calculated as line price x quantity, before order discounts, VAT included when prices include it.

1. Gift Set: 17 units, €833.00
2. Glass Teapot 600ml: 19 units, €646.00
3. Black Tea 100g: 27 units, €310.50
4. Oolong 50g: 16 units, €256.00
5. Ceramic Cup: 14 units, €252.00

### What was left out
2 of 60 orders in the export were left out: test order: #1013; cancelled: #1021. Orders are assigned to a month by order Created at, as written in the export. Refunds are counted in the month of their order.

### How this was counted
Definitions used:
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

What the export contains and what it was checked against:
- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Source files and versions:
- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- computed by shopify-month-end v0.5.1, scripts f1930a1babf4

### Questions for you (please answer before the accountant relies on these)
The figures above use the usual answers until you confirm them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

If you answer the questions above, I'll save your answers so they're used every month and redo the numbers if any answer changes them. Your accountant may also want to know why the bank received less than this, since card fees and payouts still on their way make a difference. If so, send me the Shopify Payments payout export and I'll reconcile it against these sales.
