<!-- numbers-0.5.2-claude-opus-5-5 / numbers-summary-b / with the plugin / run 3: passed -->

August went fine: $4,205.63 in sales and $4,147.57 after refunds. Refunds were small at 1.4%. Nothing in the export contradicts itself, and every figure below was checked against the data by the plugin's script. Two things before you send it:

- **The export has no orders on 4 days:** Aug 2, 7, 13 and 22. It covers Aug 1 to 31, so it's probably fine, but check that no orders are missing on those days.
- **Your store has no settings file yet,** so the figures use the standard counting rules. Please look at the questions at the end, especially whether revenue should include VAT and shipping. Your bookkeeper may want it without VAT.

---

## 2026-08 sales summary

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes $284.28 of VAT/sales tax and $229.35 of shipping paid by customers; the net after refunds still holds most of both (refunds gave only some back). Neither figure is profit: the tax is owed to the tax authority, and shipping and product costs have not been taken off.

| | |
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

**Refunded orders:** #2038, #2049. The export does not say why.

### Top products
(line price x quantity, before order discounts, VAT included when prices include it)

1. Reed Diffuser: $1,248.00 (39 units)
2. Cedar Candle 8oz: $672.00 (28 units)
3. Fig Candle 8oz: $528.00 (22 units)
4. Travel Tin Trio: $468.00 (24 units)
5. Match Cloche: $408.00 (34 units)

### What was left out
Of 70 orders in the export, 3 were left out: cancelled: #2008; test order (test payment gateway): #2011, #2044.

Orders are placed in the month by order Created at, as written in the export, and refunds are counted in the month of their order.

### How this was counted
Definitions (none confirmed by you yet):
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

Files and version:
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- computed by shopify-month-end v0.5.2, scripts ae0423f29e4e

### Questions for you
The figures above use the usual answers until you confirm them:
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

Once you answer the questions, I'll re-run the numbers with your settings. If you confirm the statuses and payment methods listed above, I'll also save them so any new one gets flagged next month.
