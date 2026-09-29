Only one product lost money in August: the Sample Votive, which went out free. Every product you actually sell made a margin of 60% or more. Here is the checked answer (amounts in USD):

## Which products lose money: 2026-08

**One product sold below cost.** MO-SMP-001 went out 9 times with revenue of 0.00, so it has a cost of 9.90 and a margin of -9.90. This is the Sample Votive. It looks like a free sample given with orders, so this is what the samples cost rather than a pricing mistake. Every other product made money.

- Products with unknown cost: none.
- SKUs that may have been renamed: none.
- The cost sheet spells one SKU differently (lowercase, with a trailing space): mo-cnd-001 . It was matched to MO-CND-001. You may want to fix it in the sheet.

### Orders left out
cancelled: #2008; test order (test payment gateway): #2011, #2044

### All products

| Product | SKU | Units | Revenue (no sales tax) | Cost | Margin | Margin % |
|---|---|---|---|---|---|---|
| Cedar Candle 8oz | MO-CND-001 | 28 | 672.00 | 207.20 | 464.80 | 69.2% |
| Fig Candle 8oz | MO-CND-002 | 22 | 528.00 | 173.80 | 354.20 | 67.1% |
| Travel Tin Trio | MO-CND-010 | 24 | 468.00 | 146.40 | 321.60 | 68.7% |
| Reed Diffuser | MO-DIF-001 | 39 | 1,248.00 | 436.80 | 811.20 | 65.0% |
| Match Cloche | MO-MAT-001 | 34 | 408.00 | 163.20 | 244.80 | 60.0% |
| Sample Votive | MO-SMP-001 | 9 | 0.00 | 9.90 | -9.90 | 0.0% |
| Wick Trimmer | MO-WCK-001 | 27 | 378.00 | 140.40 | 237.60 | 62.9% |

Some amounts are not split across products: 10.00 in discounts, 58.06 in refunds and 0.00 in tips and gift cards sold (these are not products). So the margins above are before discounts and refunds.

Sales tax removed from prices: 0%, because your prices do not include it. The figures cover 67 orders.

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
The figures use the usual answers below until you confirm them. A different answer would change them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by sku-margin-check v0.11.6 · seal c72311e67a99
