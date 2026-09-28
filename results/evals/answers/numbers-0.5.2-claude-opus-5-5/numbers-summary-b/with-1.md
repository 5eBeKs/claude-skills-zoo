<!-- numbers-0.5.2-claude-opus-5-5 / numbers-summary-b / with the plugin / run 1: passed -->

Here's the August summary. It's the checked output, unchanged:

---

# Sales summary: 2026-08

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes $284.28 of VAT and $229.35 of shipping, and the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: VAT is owed to the tax authority, shipping pays the carrier, and product costs and fees are not taken off.

| | |
|---|---|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| VAT inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 (2 orders had a discount) |

**Revenue as the store defines it:** $4,205.63 (VAT included, shipping included, partial refunds as amount).

**Refunds** came from 2 orders: #2038, #2049. The export does not say why.

## Top products
Basis: line price x quantity, before order discounts, VAT included when prices include it.

1. Reed Diffuser: $1,248.00 (39 units)
2. Cedar Candle 8oz: $672.00 (28 units)
3. Fig Candle 8oz: $528.00 (22 units)
4. Travel Tin Trio: $468.00 (24 units)
5. Match Cloche: $408.00 (34 units)

## What was left out
3 orders were left out of the figures: cancelled: #2008; test order (test payment gateway): #2011, #2044.

Orders are placed in the month by order Created at, as written in the export; refunds are counted in the month of their order.

## How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

The export and what it was checked against:
- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Files and version:
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
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

**To pass this to your bookkeeper:**
- **These figures aren't final yet.** They use the usual answers to the questions above. Your answers can change them, especially whether revenue includes VAT and shipping. Once you answer, I'll save them in a `store_definitions.json` file so future months are counted your way.
- **They haven't been checked against anything outside the export.** If you give me one figure from Shopify Analytics or your bank, I can compare it with these.
- **This summary doesn't cover what reached your bank.** It leaves out card fees and payouts still in transit. If your bookkeeper needs that too, send me the Shopify Payments payouts export for August and I'll match it against these sales.
