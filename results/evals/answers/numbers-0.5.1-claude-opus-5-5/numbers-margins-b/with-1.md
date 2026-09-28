<!-- numbers-0.5.1-claude-opus-5-5 / numbers-margins-b / with the plugin / run 1: passed -->

The only product that lost money in August is the free sample. Every product you actually sell made money on each sale. Figures are in USD, with no sales tax taken off since your prices don't include it. The report below passed the plugin's number check:

---

**Sold below cost in August 2026**

- **Sample Votive (MO-SMP-001)**: 9 units, revenue 0.00, cost 9.90, margin **-9.90**. These are free add-on lines (price 0.00) inside paid orders, so this is the cost of giving samples away rather than a product priced too low.

Every other product sold above cost. Products with unknown cost: none.

**Orders left out:** cancelled: #2008; test order (test payment gateway): #2011, #2044

**All products** (revenue without sales tax)

| SKU | Product | Units | Revenue | Cost | Margin | Margin % |
|---|---|---|---|---|---|---|
| MO-CND-001 | Cedar Candle 8oz | 28 | 672.00 | 207.20 | 464.80 | 69.2% |
| MO-CND-002 | Fig Candle 8oz | 22 | 528.00 | 173.80 | 354.20 | 67.1% |
| MO-CND-010 | Travel Tin Trio | 24 | 468.00 | 146.40 | 321.60 | 68.7% |
| MO-DIF-001 | Reed Diffuser | 39 | 1,248.00 | 436.80 | 811.20 | 65.0% |
| MO-MAT-001 | Match Cloche | 34 | 408.00 | 163.20 | 244.80 | 60.0% |
| MO-SMP-001 | Sample Votive | 9 | 0.00 | 9.90 | -9.90 | n/a (free) |
| MO-WCK-001 | Wick Trimmer | 27 | 378.00 | 140.40 | 237.60 | 62.9% |

Not spread over products: 10.00 in order discounts and 58.06 in refunds. Product margins are before these.

Sales tax rate removed from prices: 0 (you said prices exclude tax). Figures cover 67 orders. One cost-sheet SKU was written differently from the export and matched after normalizing: mo-cnd-001 .

**How this was counted**

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- prices include VAT at 0% (as given)
- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- cogs.csv: 7 rows, SHA-256 ebfd4f1c3958ee7b
- computed by shopify-month-end v0.5.1, scripts 8ce8d389332c

**Please confirm** (the figures use the usual answers until you do; a different answer changes them):

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

In `cogs.csv`, the first SKU is written `mo-cnd-001 ` (lowercase with a trailing space). It was matched to MO-CND-001 anyway, but you may want to fix it in the sheet.
