<!-- numbers-0.5.1-claude-opus-5-5 / numbers-margins-c / with the plugin / run 3: passed -->

In August, three products sold below cost: two clearance lines and the sample sachets. A fourth, **Peptide Serum 30ml**, has no cost on cogs.csv, so I can't tell whether it made or lost money. All other products made money on a product-by-product basis.

The complete report, including all 85 left-out order numbers, is saved as `files/margins_2026-08.md`. It passed the figure check against the computed results. Below is the same report, with the left-out orders given as a count instead of a list.

---

# Product margins, August 2026 (GBP)

## Sold below cost in August

| SKU | Product | Units | Revenue ex VAT | Cost | Margin |
|---|---|---:|---:|---:|---:|
| GL-CLR-001 | Summer Tin (clearance) | 21 | 105.00 | 121.80 | -16.80 |
| GL-CLR-002 | Old Label Serum (clearance) | 35 | 280.00 | 294.00 | -14.00 |
| GL-SMP-001 | Sample Sachet | 188 | 0.00 | 65.80 | -65.80 |

- The two clearance lines (Summer Tin (clearance) and Old Label Serum (clearance)) sold for less than their unit cost: a margin of -16.0% and -5.0%.
- Sample Sachet brought in no revenue at all (188 units went out at a price of zero), so its whole cost is a loss. If these are free samples added to orders, that is expected, but they are a cost of selling rather than a product.

## Cost unknown

GL-NEW-001 (Peptide Serum 30ml): 180 units, 5,700.00 revenue ex VAT. It is not on cogs.csv, so its margin is **unknown, not zero**, and it could be making or losing money. What is its unit cost?

## Orders left out

85 orders are not in the figures: cancelled orders, test orders (tagged or paid through the test gateway), and paid pre-orders not yet shipped. The full list by order number is in the saved file.

## All products

| SKU | Product | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---|---:|---:|---:|---:|---:|
| GL-BAG-001 | Wash Bag | 220 | 2750.00 | 1056.00 | 1694.00 | 61.6% |
| GL-BDY-200 | Body Lotion 200ml | 184 | 2913.33 | 772.80 | 2140.53 | 73.5% |
| GL-CLN-100 | Gentle Cleanser 100ml | 235 | 2741.67 | 728.50 | 2013.17 | 73.4% |
| GL-CLN-250 | Gentle Cleanser 250ml | 212 | 4240.00 | 1187.20 | 3052.80 | 72.0% |
| GL-CLR-001 | Summer Tin (clearance) | 21 | 105.00 | 121.80 | -16.80 | -16.0% |
| GL-CLR-002 | Old Label Serum (clearance) | 35 | 280.00 | 294.00 | -14.00 | -5.0% |
| GL-CND-001 | Rose Candle | 233 | 3883.33 | 1374.70 | 2508.63 | 64.6% |
| GL-EYE-015 | Eye Balm 15ml | 258 | 4730.00 | 1315.80 | 3414.20 | 72.2% |
| GL-GFT-001 | Starter Gift Box | 87 | 3262.50 | 1174.50 | 2088.00 | 64.0% |
| GL-GFT-002 | Deluxe Gift Box | 105 | 6912.50 | 2520.00 | 4392.50 | 63.5% |
| GL-HND-075 | Hand Cream 75ml | 238 | 2181.67 | 547.40 | 1634.27 | 74.9% |
| GL-LIP-004 | Lip Balm Trio | 207 | 2070.00 | 558.90 | 1511.10 | 73.0% |
| GL-MIN-001 | Travel Minis Set | 161 | 3354.17 | 1400.70 | 1953.47 | 58.2% |
| GL-MSK-075 | Clay Mask 75ml | 224 | 3360.00 | 851.20 | 2508.80 | 74.7% |
| GL-MST-050 | Day Moisturiser 50ml | 216 | 5040.00 | 1360.80 | 3679.20 | 73.0% |
| GL-MST-051 | Night Cream 50ml | 208 | 5200.00 | 1435.20 | 3764.80 | 72.4% |
| GL-NEW-001 | Peptide Serum 30ml | 180 | 5700.00 | unknown | unknown | unknown |
| GL-OIL-030 | Facial Oil 30ml | 206 | 4463.33 | 1256.60 | 3206.73 | 71.8% |
| GL-SCR-150 | Coffee Scrub 150ml | 220 | 3116.67 | 858.00 | 2258.67 | 72.5% |
| GL-SER-030 | Vitamin C Serum 30ml | 178 | 4746.67 | 1406.20 | 3340.47 | 70.4% |
| GL-SER-031 | Retinol Serum 30ml | 221 | 6630.00 | 2033.20 | 4596.80 | 69.3% |
| GL-SMP-001 | Sample Sachet | 188 | 0.00 | 65.80 | -65.80 | n/a (no revenue) |
| GL-SOP-100 | Oat Soap Bar | 229 | 1431.25 | 366.40 | 1064.85 | 74.4% |
| GL-SPF-050 | Mineral SPF 50 | 216 | 3780.00 | 1166.40 | 2613.60 | 69.1% |
| GL-TNR-150 | Rose Toner 150ml | 230 | 3066.67 | 782.00 | 2284.67 | 74.5% |
| GL-TWL-001 | Bamboo Face Towel | 206 | 1545.00 | 494.40 | 1050.60 | 68.0% |

Not spread over products: 1,197.08 in order discounts and 1,703.19 in refunds. The product margins above are before these, so the true margins are somewhat lower.

VAT removed at 0.2; the figures cover 1,555 orders. Two cost-sheet SKUs were written differently from the export and were matched anyway: GL-MST-050 , gl-ser-030 (a stray space and lower case).

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- a sale counts only once it is shipped; paid orders not yet shipped (pre-orders) are left out (your answer)
- prices include VAT at 20% (as given)
- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- cogs.csv: 25 rows, SHA-256 51553ddde8109275
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.5.1, scripts 8ce8d389332c

## Open question

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

The figures use the usual answer until you confirm it; a different answer would change them.

<!-- the report this run saved next to the exports: margins_2026-08.md -->

# Product margins, August 2026 (GBP)

## Sold below cost in August

| SKU | Product | Units | Revenue ex VAT | Cost | Margin |
|---|---|---:|---:|---:|---:|
| GL-CLR-001 | Summer Tin (clearance) | 21 | 105.00 | 121.80 | -16.80 |
| GL-CLR-002 | Old Label Serum (clearance) | 35 | 280.00 | 294.00 | -14.00 |
| GL-SMP-001 | Sample Sachet | 188 | 0.00 | 65.80 | -65.80 |

- The two clearance lines (Summer Tin (clearance) and Old Label Serum (clearance)) sold for less than their unit cost: a margin of -16.0% and -5.0%.
- Sample Sachet brought in no revenue at all (188 units went out at a price of zero), so its whole cost is a loss. If these are free samples added to orders, that is expected, but they are a cost of selling rather than a product.

## Cost unknown

GL-NEW-001 (Peptide Serum 30ml): 180 units, 5,700.00 revenue ex VAT. It is not on cogs.csv, so its margin is **unknown, not zero**, and it could be making or losing money. What is its unit cost?

## Orders left out

85 orders are not in the figures: cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449.

## All products

| SKU | Product | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---|---:|---:|---:|---:|---:|
| GL-BAG-001 | Wash Bag | 220 | 2750.00 | 1056.00 | 1694.00 | 61.6% |
| GL-BDY-200 | Body Lotion 200ml | 184 | 2913.33 | 772.80 | 2140.53 | 73.5% |
| GL-CLN-100 | Gentle Cleanser 100ml | 235 | 2741.67 | 728.50 | 2013.17 | 73.4% |
| GL-CLN-250 | Gentle Cleanser 250ml | 212 | 4240.00 | 1187.20 | 3052.80 | 72.0% |
| GL-CLR-001 | Summer Tin (clearance) | 21 | 105.00 | 121.80 | -16.80 | -16.0% |
| GL-CLR-002 | Old Label Serum (clearance) | 35 | 280.00 | 294.00 | -14.00 | -5.0% |
| GL-CND-001 | Rose Candle | 233 | 3883.33 | 1374.70 | 2508.63 | 64.6% |
| GL-EYE-015 | Eye Balm 15ml | 258 | 4730.00 | 1315.80 | 3414.20 | 72.2% |
| GL-GFT-001 | Starter Gift Box | 87 | 3262.50 | 1174.50 | 2088.00 | 64.0% |
| GL-GFT-002 | Deluxe Gift Box | 105 | 6912.50 | 2520.00 | 4392.50 | 63.5% |
| GL-HND-075 | Hand Cream 75ml | 238 | 2181.67 | 547.40 | 1634.27 | 74.9% |
| GL-LIP-004 | Lip Balm Trio | 207 | 2070.00 | 558.90 | 1511.10 | 73.0% |
| GL-MIN-001 | Travel Minis Set | 161 | 3354.17 | 1400.70 | 1953.47 | 58.2% |
| GL-MSK-075 | Clay Mask 75ml | 224 | 3360.00 | 851.20 | 2508.80 | 74.7% |
| GL-MST-050 | Day Moisturiser 50ml | 216 | 5040.00 | 1360.80 | 3679.20 | 73.0% |
| GL-MST-051 | Night Cream 50ml | 208 | 5200.00 | 1435.20 | 3764.80 | 72.4% |
| GL-NEW-001 | Peptide Serum 30ml | 180 | 5700.00 | unknown | unknown | unknown |
| GL-OIL-030 | Facial Oil 30ml | 206 | 4463.33 | 1256.60 | 3206.73 | 71.8% |
| GL-SCR-150 | Coffee Scrub 150ml | 220 | 3116.67 | 858.00 | 2258.67 | 72.5% |
| GL-SER-030 | Vitamin C Serum 30ml | 178 | 4746.67 | 1406.20 | 3340.47 | 70.4% |
| GL-SER-031 | Retinol Serum 30ml | 221 | 6630.00 | 2033.20 | 4596.80 | 69.3% |
| GL-SMP-001 | Sample Sachet | 188 | 0.00 | 65.80 | -65.80 | n/a (no revenue) |
| GL-SOP-100 | Oat Soap Bar | 229 | 1431.25 | 366.40 | 1064.85 | 74.4% |
| GL-SPF-050 | Mineral SPF 50 | 216 | 3780.00 | 1166.40 | 2613.60 | 69.1% |
| GL-TNR-150 | Rose Toner 150ml | 230 | 3066.67 | 782.00 | 2284.67 | 74.5% |
| GL-TWL-001 | Bamboo Face Towel | 206 | 1545.00 | 494.40 | 1050.60 | 68.0% |

Not spread over products: 1,197.08 in order discounts and 1,703.19 in refunds. Product margins above are before these, so the true margins are somewhat lower.

VAT removed at 0.2; the figures cover 1,555 orders. Two cost-sheet SKUs were written differently from the export and were matched anyway: GL-MST-050 , gl-ser-030 (a stray space and lower case).

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- a sale counts only once it is shipped; paid orders not yet shipped (pre-orders) are left out (your answer)
- prices include VAT at 20% (as given)
- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- cogs.csv: 25 rows, SHA-256 51553ddde8109275
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.5.1, scripts 8ce8d389332c

## Open question

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

The figures use the usual answer until you confirm it; a different answer would change them.

