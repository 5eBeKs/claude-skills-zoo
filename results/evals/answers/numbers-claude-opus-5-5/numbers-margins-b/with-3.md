<!-- numbers-claude-opus-5-5 / numbers-margins-b / with the plugin / run 3: passed -->

**Only one product lost money in August: Sample Votive (MO-SMP-001).** 9 units went out with no revenue, so their cost of 9.90 USD is a straight loss (margin -9.90). They look like free samples given away, not a product priced below cost. Whether that's worth it depends on what the samples bring in, and this data doesn't show that.

Every other product sells well above cost. Every SKU sold had a cost in cogs.csv.

| SKU | Product | Units | Revenue (no tax) | Cost | Margin | Margin % |
|---|---|---:|---:|---:|---:|---:|
| MO-DIF-001 | Reed Diffuser | 39 | 1,248.00 | 436.80 | 811.20 | 65.0% |
| MO-CND-001 | Cedar Candle 8oz | 28 | 672.00 | 207.20 | 464.80 | 69.2% |
| MO-CND-002 | Fig Candle 8oz | 22 | 528.00 | 173.80 | 354.20 | 67.1% |
| MO-CND-010 | Travel Tin Trio | 24 | 468.00 | 146.40 | 321.60 | 68.7% |
| MO-MAT-001 | Match Cloche | 34 | 408.00 | 163.20 | 244.80 | 60.0% |
| MO-WCK-001 | Wick Trimmer | 27 | 378.00 | 140.40 | 237.60 | 62.9% |
| MO-SMP-001 | Sample Votive | 9 | 0.00 | 9.90 | -9.90 | n/a (no revenue) |

All amounts are in USD.

- **Discounts and refunds:** 10.00 in order-level discounts and 58.06 in refunds aren't assigned to individual products. They're too small to push any other product below cost.
- **Scope:** the figures cover 67 orders. No sales tax was taken out of prices, since your prices don't include it.
- **Cost sheet:** one SKU in cogs.csv was written differently ("mo-cnd-001 ", lowercase with a trailing space). It was still matched to Cedar Candle 8oz.

**How this was counted**
- Orders tagged "test" and orders paid through Shopify's test gateway are left out of sales. This is the usual approach; please confirm.
- A sale counts once it's paid, whether or not it has shipped. This is also the usual approach; please confirm.
- Prices contain no sales tax, as you said.

**Please confirm:** the figures above use the usual answers to these two questions. A different answer would change the figures:
- Should test orders stay out of sales, or be counted?
- Does a sale count when it's paid, or only once it has shipped?
