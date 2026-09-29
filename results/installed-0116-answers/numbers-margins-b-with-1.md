Only one product lost money in August: the Sample Votive (MO-SMP-001). It went out for free (no revenue), so its whole cost was a loss. That looks like a marketing cost rather than a pricing problem. Every other product made money. Amounts are in USD, and the result below passed the check and is shown exactly as produced:

---

## Product margins, August 2026

**Sold below cost:** MO-SMP-001 is the only product that lost money. MO-SMP-001 sold 9 units for 0.00 in revenue, so its whole cost of 9.90 is a loss: margin -9.90. This is the Sample Votive, and it looks like a free sample given away with orders. If so, the loss is a marketing cost, not a pricing problem.

Every other product makes money (see the table). No product is missing a cost, and no SKU looks renamed. In the cost sheet, `mo-cnd-001 ` (lowercase, trailing space) was read as MO-CND-001.

**Orders left out:**
cancelled: #2008; test order (test payment gateway): #2011, #2044

| Product | SKU | Units | Revenue (no tax) | Cost | Margin | Margin % |
|---|---|---:|---:|---:|---:|---:|
| Cedar Candle 8oz | MO-CND-001 | 28 | 672.00 | 207.20 | 464.80 | 69.2% |
| Fig Candle 8oz | MO-CND-002 | 22 | 528.00 | 173.80 | 354.20 | 67.1% |
| Travel Tin Trio | MO-CND-010 | 24 | 468.00 | 146.40 | 321.60 | 68.7% |
| Reed Diffuser | MO-DIF-001 | 39 | 1,248.00 | 436.80 | 811.20 | 65.0% |
| Match Cloche | MO-MAT-001 | 34 | 408.00 | 163.20 | 244.80 | 60.0% |
| Sample Votive | MO-SMP-001 | 9 | 0.00 | 9.90 | -9.90 | 0.0% |
| Wick Trimmer | MO-WCK-001 | 27 | 378.00 | 140.40 | 237.60 | 62.9% |

Not spread over products: 10.00 in discounts, 58.06 in refunds and 0.00 in tips and gift cards sold (not products). Product margins come before discounts and refunds.

Tax rate taken out of prices: 0%. You said your prices don't include sales tax. The figures cover 67 orders.

### How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- prices include VAT at 0% (as given)
- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- cogs.csv: 7 rows, SHA-256 ebfd4f1c3958ee7b
- computed by shopify-month-end v0.11.6, scripts db4321daa942

### Open questions
Until you confirm these, the figures use the usual answers. A different answer would change them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by sku-margin-check v0.11.6 · seal 663979ef4fc3
