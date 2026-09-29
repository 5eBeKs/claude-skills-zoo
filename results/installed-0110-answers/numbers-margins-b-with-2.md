Only one product lost money in August: **Sample Votive**. It was given away at $0.00. Every other product has a gross margin between 60% and 69%.

Your prices don't include sales tax, so I took no tax out of them (the report shows this as 0%). Here is the checked report, word for word:

---

# Product margins, 2026-08

## Sold below cost

- **Sample Votive (MO-SMP-001)**: 9 units, revenue 0.00, cost 9.90, margin -9.90. It was given away at no charge (free samples), so its whole cost is a loss.

No other product sells below cost. Products with unknown cost: none. SKUs that may have been renamed: none.

## All products

| SKU | Product | Units | Revenue (ex tax) | Cost | Margin | Margin % |
|---|---|---|---|---|---|---|
| MO-CND-001 | Cedar Candle 8oz | 28 | 672.00 | 207.20 | 464.80 | 69.2% |
| MO-CND-002 | Fig Candle 8oz | 22 | 528.00 | 173.80 | 354.20 | 67.1% |
| MO-CND-010 | Travel Tin Trio | 24 | 468.00 | 146.40 | 321.60 | 68.7% |
| MO-DIF-001 | Reed Diffuser | 39 | 1,248.00 | 436.80 | 811.20 | 65.0% |
| MO-MAT-001 | Match Cloche | 34 | 408.00 | 163.20 | 244.80 | 60.0% |
| MO-SMP-001 | Sample Votive | 9 | 0.00 | 9.90 | -9.90 | 0.0% |
| MO-WCK-001 | Wick Trimmer | 27 | 378.00 | 140.40 | 237.60 | 62.9% |

Not spread over products: 10.00 in discounts, 58.06 in refunds and 0.00 in tips and gift cards sold (not products).

Sales tax removed from prices: 0% (your prices do not include it). Figures cover 67 orders.

The cost sheet spelled one SKU differently (case/spaces), and it was matched anyway: mo-cnd-001 .

## Orders left out

cancelled: #2008; test order (test payment gateway): #2011, #2044

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

Checked by sku-margin-check v0.11.0 · seal 8ae01c4461ae

---

The report is saved as `margins.md`. Sample Votive's revenue is $0.00, so it looks like a free sample, but please confirm that. If you answer the three open questions, I can record the export's shape so any change next month gets flagged.
