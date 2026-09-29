Only one product lost money in August: the **Sample Votive (MO-SMP-001)**. It had no revenue, so its cost was a straight loss. It looks like a free sample, which would make it a giveaway cost rather than a pricing problem. Every product you actually charge for made money, with margins from 60% to 69%.

Because your prices don't include sales tax, I didn't take any tax out of them. The answer is below. It's also saved as `margins.md`.

---

# Product margins, August 2026

**Sold below cost:** MO-SMP-001. Sample Votive, MO-SMP-001: 9 units, revenue 0.00, cost 9.90, margin -9.90. It brought in no revenue, so its whole cost is a loss; if it is a free sample given away on purpose, that is a marketing cost rather than a pricing problem.

Every other product sells above its cost.

**Unknown cost:** none (none).

**Orders left out:**
cancelled: #2008; test order (test payment gateway): #2011, #2044

## All products

| Product | SKU | Units | Revenue (ex tax) | Cost | Margin | Margin % |
|---|---|---|---|---|---|---|
| Cedar Candle 8oz | MO-CND-001 | 28 | 672.00 | 207.20 | 464.80 | 69.2% |
| Fig Candle 8oz | MO-CND-002 | 22 | 528.00 | 173.80 | 354.20 | 67.1% |
| Travel Tin Trio | MO-CND-010 | 24 | 468.00 | 146.40 | 321.60 | 68.7% |
| Reed Diffuser | MO-DIF-001 | 39 | 1,248.00 | 436.80 | 811.20 | 65.0% |
| Match Cloche | MO-MAT-001 | 34 | 408.00 | 163.20 | 244.80 | 60.0% |
| Sample Votive | MO-SMP-001 | 9 | 0.00 | 9.90 | -9.90 | 0.0% |
| Wick Trimmer | MO-WCK-001 | 27 | 378.00 | 140.40 | 237.60 | 62.9% |

Not spread over products: 10.00 in discounts, 58.06 in refunds and 0.00 in tips and gift cards sold (not products).

Sales tax removed from prices: 0% (your prices exclude sales tax, so none was taken out). Figures cover 67 orders. The cost sheet spelled one SKU differently (mo-cnd-001 ); it was matched after trimming spaces and case.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- prices include VAT at 0% (as given)

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- cogs.csv: 7 rows, SHA-256 ebfd4f1c3958ee7b
- computed by shopify-month-end v0.11.0, scripts 6afa94c9bf8c

## Open questions

The figures use the usual answers below until you confirm them; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by sku-margin-check v0.11.0 · seal 96efc9e07ae8
