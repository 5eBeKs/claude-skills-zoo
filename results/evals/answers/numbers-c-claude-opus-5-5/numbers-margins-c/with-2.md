<!-- numbers-c-claude-opus-5-5 / numbers-margins-c / with the plugin / run 2: passed -->

I ran the margin check on August only (1555 orders, 20% VAT taken out of prices, amounts in GBP). **Three products lost money in August**, and one more can't be checked because it has no cost in cogs.csv.

**Sold below cost**

- **GL-CLR-001 Summer Tin (clearance)**: 21 units brought in 105.00 without VAT and cost 121.80, a margin of **-16.80** (-16.0%).
- **GL-CLR-002 Old Label Serum (clearance)**: 35 units brought in 280.00 without VAT and cost 294.00, a margin of **-14.00** (-5.0%).
- **GL-SMP-001 Sample Sachet**: 188 units went out free (revenue 0.00) and cost 65.80, a margin of **-65.80**. These are free samples, so the loss is just what they cost. The 0.0% margin in the table doesn't mean anything when there's no revenue.

**Cost unknown**: GL-NEW-001 Peptide Serum 30ml sold 180 units for 5,700.00 without VAT, but it isn't in cogs.csv. Its margin is unknown, not zero. Can you send its unit cost so I can check it?

**All products**

| SKU | Product | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---|---:|---:|---:|---:|---:|
| GL-BAG-001 | Wash Bag | 220 | 2,750.00 | 1,056.00 | 1,694.00 | 61.6 |
| GL-BDY-200 | Body Lotion 200ml | 184 | 2,913.33 | 772.80 | 2,140.53 | 73.5 |
| GL-CLN-100 | Gentle Cleanser 100ml | 235 | 2,741.67 | 728.50 | 2,013.17 | 73.4 |
| GL-CLN-250 | Gentle Cleanser 250ml | 212 | 4,240.00 | 1,187.20 | 3,052.80 | 72.0 |
| GL-CLR-001 | Summer Tin (clearance) | 21 | 105.00 | 121.80 | -16.80 | -16.0 |
| GL-CLR-002 | Old Label Serum (clearance) | 35 | 280.00 | 294.00 | -14.00 | -5.0 |
| GL-CND-001 | Rose Candle | 233 | 3,883.33 | 1,374.70 | 2,508.63 | 64.6 |
| GL-EYE-015 | Eye Balm 15ml | 258 | 4,730.00 | 1,315.80 | 3,414.20 | 72.2 |
| GL-GFT-001 | Starter Gift Box | 87 | 3,262.50 | 1,174.50 | 2,088.00 | 64.0 |
| GL-GFT-002 | Deluxe Gift Box | 105 | 6,912.50 | 2,520.00 | 4,392.50 | 63.5 |
| GL-HND-075 | Hand Cream 75ml | 238 | 2,181.67 | 547.40 | 1,634.27 | 74.9 |
| GL-LIP-004 | Lip Balm Trio | 207 | 2,070.00 | 558.90 | 1,511.10 | 73.0 |
| GL-MIN-001 | Travel Minis Set | 161 | 3,354.17 | 1,400.70 | 1,953.47 | 58.2 |
| GL-MSK-075 | Clay Mask 75ml | 224 | 3,360.00 | 851.20 | 2,508.80 | 74.7 |
| GL-MST-050 | Day Moisturiser 50ml | 216 | 5,040.00 | 1,360.80 | 3,679.20 | 73.0 |
| GL-MST-051 | Night Cream 50ml | 208 | 5,200.00 | 1,435.20 | 3,764.80 | 72.4 |
| GL-NEW-001 | Peptide Serum 30ml | 180 | 5,700.00 | unknown | unknown | unknown |
| GL-OIL-030 | Facial Oil 30ml | 206 | 4,463.33 | 1,256.60 | 3,206.73 | 71.8 |
| GL-SCR-150 | Coffee Scrub 150ml | 220 | 3,116.67 | 858.00 | 2,258.67 | 72.5 |
| GL-SER-030 | Vitamin C Serum 30ml | 178 | 4,746.67 | 1,406.20 | 3,340.47 | 70.4 |
| GL-SER-031 | Retinol Serum 30ml | 221 | 6,630.00 | 2,033.20 | 4,596.80 | 69.3 |
| GL-SMP-001 | Sample Sachet | 188 | 0.00 | 65.80 | -65.80 | 0.0 |
| GL-SOP-100 | Oat Soap Bar | 229 | 1,431.25 | 366.40 | 1,064.85 | 74.4 |
| GL-SPF-050 | Mineral SPF 50 | 216 | 3,780.00 | 1,166.40 | 2,613.60 | 69.1 |
| GL-TNR-150 | Rose Toner 150ml | 230 | 3,066.67 | 782.00 | 2,284.67 | 74.5 |
| GL-TWL-001 | Bamboo Face Towel | 206 | 1,545.00 | 494.40 | 1,050.60 | 68.0 |

These product figures don't include 1,197.08 of order discounts or 1,703.19 of refunds, because those aren't split across products.

**How this was counted** (from `store_definitions.json`)

- Orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer).
- A sale counts only once it's shipped, so paid orders not yet shipped (pre-orders) are left out (your answer).
- Prices include VAT at 20% (as you said).

**Automated number check:** every figure above matched the computed results except two, which the checker flagged: "50" from the product name "Mineral SPF 50" and "20%" from the VAT line. Both are words, not calculated figures, so I left the text as it is. Two entries in cogs.csv were written slightly differently from the order SKUs (`GL-MST-050` with a trailing space, and lowercase `gl-ser-030`), and they were matched to the right products.
