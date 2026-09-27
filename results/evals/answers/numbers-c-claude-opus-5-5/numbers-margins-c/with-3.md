<!-- numbers-c-claude-opus-5-5 / numbers-margins-c / with the plugin / run 3: passed -->

In August, three products sold below cost. One more product has no cost in `cogs.csv`, so I can't tell yet whether it made or lost money.

## Products that lost money in August 2026

- **Summer Tin (clearance), GL-CLR-001:** 21 units sold for £105.00 excluding VAT. They cost £121.80, so the loss was **£-16.80** (-16.0%).
- **Old Label Serum (clearance), GL-CLR-002:** 35 units sold for £280.00 excluding VAT. They cost £294.00, so the loss was **£-14.00** (-5.0%).
- **Sample Sachet, GL-SMP-001:** 188 units went out with no revenue. They cost £65.80, so the loss was **£-65.80**. These are free samples, so this loss is expected.

**Cost unknown:** Peptide Serum 30ml (GL-NEW-001) sold 180 units for £5,700.00 excluding VAT, but it isn't in `cogs.csv`. Its margin is unknown, not zero. Could you send me its unit cost?

Every other product made money: margins ranged from 58.2% (Travel Minis Set) to 74.9% (Hand Cream 75ml).

| Product | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---:|---:|---:|---:|---:|
| Wash Bag (GL-BAG-001) | 220 | £2,750.00 | £1,056.00 | £1,694.00 | 61.6% |
| Body Lotion 200ml (GL-BDY-200) | 184 | £2,913.33 | £772.80 | £2,140.53 | 73.5% |
| Gentle Cleanser 100ml (GL-CLN-100) | 235 | £2,741.67 | £728.50 | £2,013.17 | 73.4% |
| Gentle Cleanser 250ml (GL-CLN-250) | 212 | £4,240.00 | £1,187.20 | £3,052.80 | 72.0% |
| Summer Tin (clearance) (GL-CLR-001) | 21 | £105.00 | £121.80 | £-16.80 | -16.0% |
| Old Label Serum (clearance) (GL-CLR-002) | 35 | £280.00 | £294.00 | £-14.00 | -5.0% |
| Rose Candle (GL-CND-001) | 233 | £3,883.33 | £1,374.70 | £2,508.63 | 64.6% |
| Eye Balm 15ml (GL-EYE-015) | 258 | £4,730.00 | £1,315.80 | £3,414.20 | 72.2% |
| Starter Gift Box (GL-GFT-001) | 87 | £3,262.50 | £1,174.50 | £2,088.00 | 64.0% |
| Deluxe Gift Box (GL-GFT-002) | 105 | £6,912.50 | £2,520.00 | £4,392.50 | 63.5% |
| Hand Cream 75ml (GL-HND-075) | 238 | £2,181.67 | £547.40 | £1,634.27 | 74.9% |
| Lip Balm Trio (GL-LIP-004) | 207 | £2,070.00 | £558.90 | £1,511.10 | 73.0% |
| Travel Minis Set (GL-MIN-001) | 161 | £3,354.17 | £1,400.70 | £1,953.47 | 58.2% |
| Clay Mask 75ml (GL-MSK-075) | 224 | £3,360.00 | £851.20 | £2,508.80 | 74.7% |
| Day Moisturiser 50ml (GL-MST-050) | 216 | £5,040.00 | £1,360.80 | £3,679.20 | 73.0% |
| Night Cream 50ml (GL-MST-051) | 208 | £5,200.00 | £1,435.20 | £3,764.80 | 72.4% |
| Peptide Serum 30ml (GL-NEW-001) | 180 | £5,700.00 | unknown | unknown | unknown |
| Facial Oil 30ml (GL-OIL-030) | 206 | £4,463.33 | £1,256.60 | £3,206.73 | 71.8% |
| Coffee Scrub 150ml (GL-SCR-150) | 220 | £3,116.67 | £858.00 | £2,258.67 | 72.5% |
| Vitamin C Serum 30ml (GL-SER-030) | 178 | £4,746.67 | £1,406.20 | £3,340.47 | 70.4% |
| Retinol Serum 30ml (GL-SER-031) | 221 | £6,630.00 | £2,033.20 | £4,596.80 | 69.3% |
| Sample Sachet (GL-SMP-001) | 188 | £0.00 | £65.80 | £-65.80 | n/a (no revenue) |
| Oat Soap Bar (GL-SOP-100) | 229 | £1,431.25 | £366.40 | £1,064.85 | 74.4% |
| Mineral SPF 50 (GL-SPF-050) | 216 | £3,780.00 | £1,166.40 | £2,613.60 | 69.1% |
| Rose Toner 150ml (GL-TNR-150) | 230 | £3,066.67 | £782.00 | £2,284.67 | 74.5% |
| Bamboo Face Towel (GL-TWL-001) | 206 | £1,545.00 | £494.40 | £1,050.60 | 68.0% |

The export doesn't split discounts or refunds by product, so the margins above are before £1,197.08 in discounts and £1,703.19 in refunds.

I removed VAT at 0.20, and the figures cover 1555 August orders.

### How this was counted
- Orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer).
- A sale counts only once it is shipped, so paid orders not yet shipped (pre-orders) are left out (your answer).
- Prices include VAT at 20% (as given).

---

- **Number check:** the check that traces every figure back to the calculation flagged two items: the "50" in "Mineral SPF 50" and the "20%" in the VAT line under "How this was counted". Both are text rather than calculated figures. Every margin, revenue and cost figure matched.
- **Cost sheet fixes:** two SKUs in `cogs.csv` were written slightly differently from the orders export. `GL-MST-050 ` had a trailing space and `gl-ser-030` was lowercase. I matched them to the right products, but you may want to correct them in the file.
