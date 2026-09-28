<!-- numbers-0.5.1-claude-opus-5-5 / numbers-summary-b / with the plugin / run 1: passed -->

I've saved the August summary for your bookkeeper as `files/summary_2026-08.md`, next to the export. Nothing in the export contradicts itself, so the figures below are ready to use as they are:

---

# Sales summary: 2026-08

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes $284.28 of VAT/sales tax and $229.35 of shipping paid by customers; the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: product costs, Shopify and card fees, and the tax you owe are all still to come out of it.

| Figure | 2026-08 |
|---|---|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| VAT/tax inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 (2 orders had a discount) |

**Revenue as the store defines it:** $4,205.63 (VAT included, shipping included, partial refunds as amount).

**Refunds:** #2038, #2049. The export does not say why they were refunded.

## Top products (line price x quantity, before order discounts, VAT included when prices include it)

1. Reed Diffuser: 39 units, $1,248.00
2. Cedar Candle 8oz: 28 units, $672.00
3. Fig Candle 8oz: 22 units, $528.00
4. Travel Tin Trio: 24 units, $468.00
5. Match Cloche: 34 units, $408.00

## What was left out

3 orders were left out of every figure: cancelled: #2008; test order (test payment gateway): #2011, #2044.

Orders are placed in the month by order Created at, as written in the export; refunds are counted in the month of their order, not the month they were paid back.

## How this was counted

Definitions:

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

The export:

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Days of the month with no orders in the export: 2026-08-02, 2026-08-07, 2026-08-13, 2026-08-22. The export's first and last days are both there, so it does not look cut off, but please check that these were just quiet days.

Files and version:

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- computed by shopify-month-end v0.5.1, scripts f1930a1babf4

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

If you send your August Shopify Payments payouts export, I can check these sales against what actually reached your bank.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# Sales summary: 2026-08

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes $284.28 of VAT/sales tax and $229.35 of shipping paid by customers; the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: product costs, Shopify and card fees, and the tax you owe are all still to come out of it.

| Figure | 2026-08 |
|---|---|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| VAT/tax inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 (2 orders had a discount) |

**Revenue as the store defines it:** $4,205.63 (VAT included, shipping included, partial refunds as amount).

**Refunds:** #2038, #2049. The export does not say why they were refunded.

## Top products (line price x quantity, before order discounts, VAT included when prices include it)

1. Reed Diffuser: 39 units, $1,248.00
2. Cedar Candle 8oz: 28 units, $672.00
3. Fig Candle 8oz: 22 units, $528.00
4. Travel Tin Trio: 24 units, $468.00
5. Match Cloche: 34 units, $408.00

## What was left out

3 orders were left out of every figure: cancelled: #2008; test order (test payment gateway): #2011, #2044.

Orders are placed in the month by order Created at, as written in the export; refunds are counted in the month of their order, not the month they were paid back.

## How this was counted

Definitions:

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

The export:

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Days of the month with no orders in the export: 2026-08-02, 2026-08-07, 2026-08-13, 2026-08-22. The export's first and last days are both there, so it does not look cut off, but please check that these were just quiet days.

Files and version:

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- computed by shopify-month-end v0.5.1, scripts f1930a1babf4

## Questions for you

The figures above use the usual answers until you confirm them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

