<!-- numbers-0.5.2-claude-opus-5-5 / numbers-summary-b / with the plugin / run 2: passed -->

August went well: $4,205.63 in sales, only $58.06 refunded, and the export had no problems. The numbers below all come from the script and passed the number check. The rules I counted by are the usual ones for Shopify stores, not ones you've confirmed. Your answers to the questions at the end could change the figures, so it's worth answering them before this goes to your bookkeeper.

---

## August sales summary (2026-08)

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes $284.28 of VAT/tax and $229.35 of shipping, and the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: the tax is owed, and product and shipping costs are not taken off.

| Figure | Amount |
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
| Discounts given | $10.00 (2 orders) |

**Revenue as the store defines it:** $4,205.63 (VAT included, shipping included, partial refunds as amount).

**Refunds:** #2038, #2049. The export does not say why.

### Top products
(line price x quantity, before order discounts, VAT included when prices include it)

1. Reed Diffuser: 39 units, $1,248.00
2. Cedar Candle 8oz: 28 units, $672.00
3. Fig Candle 8oz: 22 units, $528.00
4. Travel Tin Trio: 24 units, $468.00
5. Match Cloche: 34 units, $408.00

### What was left out
3 orders were left out of the export's 70: cancelled: #2008; test order (test payment gateway): #2011, #2044.

Orders are placed in the month by order Created at, as written in the export. Refunds are counted in the month of their order, not the month they were paid back.

The export has no orders on 2026-08-02, 2026-08-07, 2026-08-13, 2026-08-22. It does not start late or stop early, so this is likely just quiet days, but worth a glance if any of those should have had sales.

### How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

Computed from:
- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- computed by shopify-month-end v0.5.2, scripts ae0423f29e4e

### Questions for you
These figures use the usual answers until you confirm them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

When you answer those questions, I'll save your answers as `store_definitions.json` and redo the numbers. After that, next month's export will be counted the same way automatically.
