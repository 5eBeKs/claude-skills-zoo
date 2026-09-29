Three products lost money in August: the two clearance lines and the free sample sachet. One more product, GL-NEW-001 Peptide Serum 30ml, isn't in `cogs.csv`, so I can't tell whether it made money. I left out June and July and took the 20% VAT out of prices. I saved the full answer as `files/margins_2026-08.md`, and it passed the plugin's number check.

---

# Product margins, August 2026

Warnings: none.

## Products sold below cost in August

- **GL-CLR-001 Summer Tin (clearance)**: 21 units, revenue 105.00 without VAT, cost 121.80, gross margin -16.80 (-16.0%)
- **GL-CLR-002 Old Label Serum (clearance)**: 35 units, revenue 280.00 without VAT, cost 294.00, gross margin -14.00 (-5.0%)
- **GL-SMP-001 Sample Sachet**: 188 units, revenue 0.00 without VAT, cost 65.80, gross margin -65.80 (given away free, so all cost and no revenue)

## Product with unknown cost

GL-NEW-001 (Peptide Serum 30ml): 180 units, revenue 5,700.00 without VAT. It is not in cogs.csv, so its margin is unknown, not zero. What does it cost per unit?

## All products

| Product | Units | Revenue without VAT | Cost | Gross margin | Margin % |
|---|---|---|---|---|---|
| GL-BAG-001 Wash Bag | 220 | 2,750.00 | 1,056.00 | 1,694.00 | 61.6% |
| GL-BDY-200 Body Lotion 200ml | 184 | 2,913.33 | 772.80 | 2,140.53 | 73.5% |
| GL-CLN-100 Gentle Cleanser 100ml | 235 | 2,741.67 | 728.50 | 2,013.17 | 73.4% |
| GL-CLN-250 Gentle Cleanser 250ml | 212 | 4,240.00 | 1,187.20 | 3,052.80 | 72.0% |
| GL-CLR-001 Summer Tin (clearance) | 21 | 105.00 | 121.80 | -16.80 | -16.0% |
| GL-CLR-002 Old Label Serum (clearance) | 35 | 280.00 | 294.00 | -14.00 | -5.0% |
| GL-CND-001 Rose Candle | 233 | 3,883.33 | 1,374.70 | 2,508.63 | 64.6% |
| GL-EYE-015 Eye Balm 15ml | 258 | 4,730.00 | 1,315.80 | 3,414.20 | 72.2% |
| GL-GFT-001 Starter Gift Box | 87 | 3,262.50 | 1,174.50 | 2,088.00 | 64.0% |
| GL-GFT-002 Deluxe Gift Box | 105 | 6,912.50 | 2,520.00 | 4,392.50 | 63.5% |
| GL-HND-075 Hand Cream 75ml | 238 | 2,181.67 | 547.40 | 1,634.27 | 74.9% |
| GL-LIP-004 Lip Balm Trio | 207 | 2,070.00 | 558.90 | 1,511.10 | 73.0% |
| GL-MIN-001 Travel Minis Set | 161 | 3,354.17 | 1,400.70 | 1,953.47 | 58.2% |
| GL-MSK-075 Clay Mask 75ml | 224 | 3,360.00 | 851.20 | 2,508.80 | 74.7% |
| GL-MST-050 Day Moisturiser 50ml | 216 | 5,040.00 | 1,360.80 | 3,679.20 | 73.0% |
| GL-MST-051 Night Cream 50ml | 208 | 5,200.00 | 1,435.20 | 3,764.80 | 72.4% |
| GL-NEW-001 Peptide Serum 30ml | 180 | 5,700.00 | unknown | unknown | unknown |
| GL-OIL-030 Facial Oil 30ml | 206 | 4,463.33 | 1,256.60 | 3,206.73 | 71.8% |
| GL-SCR-150 Coffee Scrub 150ml | 220 | 3,116.67 | 858.00 | 2,258.67 | 72.5% |
| GL-SER-030 Vitamin C Serum 30ml | 178 | 4,746.67 | 1,406.20 | 3,340.47 | 70.4% |
| GL-SER-031 Retinol Serum 30ml | 221 | 6,630.00 | 2,033.20 | 4,596.80 | 69.3% |
| GL-SMP-001 Sample Sachet | 188 | 0.00 | 65.80 | -65.80 | 0.0% |
| GL-SOP-100 Oat Soap Bar | 229 | 1,431.25 | 366.40 | 1,064.85 | 74.4% |
| GL-SPF-050 Mineral SPF 50 | 216 | 3,780.00 | 1,166.40 | 2,613.60 | 69.1% |
| GL-TNR-150 Rose Toner 150ml | 230 | 3,066.67 | 782.00 | 2,284.67 | 74.5% |
| GL-TWL-001 Bamboo Face Towel | 206 | 1,545.00 | 494.40 | 1,050.60 | 68.0% |

Not spread over products: 1,197.08 in discounts, 1,703.19 in refunds and 0.00 in tips and gift cards sold (not products). The margins above are before these.

VAT rate taken out of prices: 0.2. Orders counted: 1555.

## Orders left out

cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449

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
- computed by shopify-month-end v0.11.6, scripts db4321daa942

## Open questions

The figures use the usual answers until you confirm them; a different answer changes them.

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by sku-margin-check v0.11.6 · seal 1f362276f99a
