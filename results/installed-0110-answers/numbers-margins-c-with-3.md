Three products lost money in August 2026: two clearance lines and the free sample sachet. A fourth, Peptide Serum 30ml, sold well but isn't in `cogs.csv`, so I can't tell yet whether it made money. All amounts are in GBP, with the 20% VAT taken out of prices.

## Products that lost money in August

| Product | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---|---|---|---|---|
| GL-CLR-001 Summer Tin (clearance) | 21 | 105.00 | 121.80 | -16.80 | -16.0 |
| GL-CLR-002 Old Label Serum (clearance) | 35 | 280.00 | 294.00 | -14.00 | -5.0 |
| GL-SMP-001 Sample Sachet | 188 | 0.00 | 65.80 | -65.80 | (given away free, so all cost and no revenue) |

## Cost unknown

**GL-NEW-001 (Peptide Serum 30ml):** 180 units sold for 5,700.00 without VAT. Its margin is unknown, not zero, so it isn't in the table below. If you send me its unit cost, I'll add it and check whether it sold below cost.

## Orders left out

85 orders were left out:
- **Not shipped (pre-orders):** 70
- **Cancelled:** 7
- **Test orders:** 8 (4 tagged "test", 4 paid through the test payment gateway)

The order numbers are in the full answer file.

## All other products (all made money)

| SKU | Product | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---|---|---|---|---|---|
| GL-BAG-001 | Wash Bag | 220 | 2,750.00 | 1,056.00 | 1,694.00 | 61.6 |
| GL-BDY-200 | Body Lotion 200ml | 184 | 2,913.33 | 772.80 | 2,140.53 | 73.5 |
| GL-CLN-100 | Gentle Cleanser 100ml | 235 | 2,741.67 | 728.50 | 2,013.17 | 73.4 |
| GL-CLN-250 | Gentle Cleanser 250ml | 212 | 4,240.00 | 1,187.20 | 3,052.80 | 72.0 |
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
| GL-OIL-030 | Facial Oil 30ml | 206 | 4,463.33 | 1,256.60 | 3,206.73 | 71.8 |
| GL-SCR-150 | Coffee Scrub 150ml | 220 | 3,116.67 | 858.00 | 2,258.67 | 72.5 |
| GL-SER-030 | Vitamin C Serum 30ml | 178 | 4,746.67 | 1,406.20 | 3,340.47 | 70.4 |
| GL-SER-031 | Retinol Serum 30ml | 221 | 6,630.00 | 2,033.20 | 4,596.80 | 69.3 |
| GL-SOP-100 | Oat Soap Bar | 229 | 1,431.25 | 366.40 | 1,064.85 | 74.4 |
| GL-SPF-050 | Mineral SPF 50 | 216 | 3,780.00 | 1,166.40 | 2,613.60 | 69.1 |
| GL-TNR-150 | Rose Toner 150ml | 230 | 3,066.67 | 782.00 | 2,284.67 | 74.5 |
| GL-TWL-001 | Bamboo Face Towel | 206 | 1,545.00 | 494.40 | 1,050.60 | 68.0 |

Some amounts aren't assigned to any one product: 1,197.08 in discounts, 1,703.19 in refunds and 0.00 in tips and gift cards sold. They're left out of the margins above, so the true margin on some products may be a bit lower.

**Basis:** these figures cover 1,555 orders, with the 20% VAT taken out of prices. There are no warnings.

## How this was counted

- Orders tagged "test" and orders paid through Shopify's test gateway are left out of sales (your answer in `store_definitions.json`).
- A sale counts only once it has shipped; paid orders not yet shipped (pre-orders) are left out (also your answer there).
- Prices include VAT at 20% (as you said).
- The export has orders on all 31 days of August 2026.
- Nothing was checked against a figure from outside the export. If you give me a figure from Shopify or the bank, I can check against it.
- Files used: `orders_export.csv` (9,074 rows), `cogs.csv` (25 rows) and `store_definitions.json`.

## Open question

Please confirm that the export's values are what you expect:
- **Financial statuses:** paid, partially_refunded, refunded, voided
- **Fulfillment statuses:** fulfilled, unfulfilled
- **Currency:** GBP
- **Payment methods:** Bogus Gateway (test), Gift card, PayPal Express Checkout, Shopify Payments
- **Tags:** pre-order, test

The figures assume they are. If you confirm, I'll save them so that next month any new value gets flagged.

I've saved the full checked answer, including every excluded order number, as `files/margins_2026-08.md`. Its last line is the check stamp: `Checked by sku-margin-check v0.11.0 · seal 753d74d0ee97`.
