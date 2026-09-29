In August, three products sold below cost. A fourth, **GL-NEW-001 (Peptide Serum 30ml)**, might also be losing money, but I can't tell because it isn't in cogs.csv.

**Sold below cost (revenue without the 20% VAT):**

| Product | Units | Revenue | Cost | Margin |
|---|---:|---:|---:|---:|
| Summer Tin (clearance), GL-CLR-001 | 21 | 105.00 | 121.80 | **-16.80 (-16.0%)** |
| Old Label Serum (clearance), GL-CLR-002 | 35 | 280.00 | 294.00 | **-14.00 (-5.0%)** |
| Sample Sachet, GL-SMP-001 | 188 | 0.00 | 65.80 | **-65.80** |

- **The two clearance lines** are priced below what they cost you.
- **Sample Sachet** earns nothing by design, since the samples are given away. That loss is the cost of the giveaway, not a pricing problem.

**Cost unknown:** GL-NEW-001 (Peptide Serum 30ml) sold 180 units for 5,700.00 without VAT. Its margin is unknown, not zero. **What is its unit cost?**

**Everything else has a margin between 58.2% (Travel Minis Set) and 74.9% (Hand Cream 75ml).** The table with every product is in the saved file.

**Not included in the product figures:**
- **Not split across products:** 1,197.08 in discounts and 1,703.19 in refunds. These figures are therefore gross margin before discounts and refunds.
- **Orders counted:** 1,555. Left out: 7 cancelled orders, 8 test orders and 70 paid orders that hadn't shipped yet (pre-orders), following your store settings. The order numbers are in the file.
- **Nothing to check against:** the figures weren't compared with any total from outside the export. If you give me a figure from Shopify or the bank, I can compare them.
- **Cost sheet typos:** two SKUs, `gl-ser-030` and `GL-MST-050 ` (with a trailing space), were matched to their products anyway.

**One question:** this is the first run on this export, so I'd like you to confirm what's in it:
- **Payment methods:** Shopify Payments, PayPal Express Checkout, Gift card and Bogus Gateway (the test gateway)
- **Payment statuses:** paid, partially_refunded, refunded, voided
- **Tags:** pre-order, test

If these are all expected, I'll save them so that any new value in a later month gets flagged.

The full answer, which passed the plugin's figure check (seal `ff3be78242ba`), is saved as `files/margins_2026-08.md`.
