In August, three products sold for less than they cost, and a fourth may have too, but I can't tell because it has no cost in cogs.csv. Figures are in GBP with the 20% VAT taken out.

**Sold below cost:**
- **Summer Tin (clearance)** (GL-CLR-001): 21 units sold for 105.00 against 121.80 in cost, a loss of 16.80 (-16.0%).
- **Old Label Serum (clearance)** (GL-CLR-002): 35 units sold for 280.00 against 294.00 in cost, a loss of 14.00 (-5.0%).
- **Sample Sachet** (GL-SMP-001): 188 units cost 65.80 and brought in nothing. These are free samples, so this is what they cost you rather than a pricing problem.

**No cost in cogs.csv:**
- **Peptide Serum 30ml** (GL-NEW-001): 180 units, 5,700.00 in sales. Without a cost I can't say whether it made money; I haven't treated it as costing zero. **What does one unit cost you?** With that I can finish this one.

Every other product made money, with margins between 58.2% (Travel Minis Set) and 74.9% (Hand Cream 75ml). The full table is in the saved report.

**Before discounts and refunds:** these margins don't include 1,197.08 in discounts or 1,703.19 in refunds. Those are only known per order, not per product. A clearance line with a discount on it could have lost more than shown above.

**How it was counted:**
- The figures cover 1555 August orders, using the rules in your `store_definitions.json`. Cancelled orders, test orders and paid orders not yet shipped (pre-orders) are left out; the saved report lists each one by order number.
- The export has records on all 31 days of August.
- Nothing outside the export was used to confirm the totals.
- Two SKUs were written differently in cogs.csv ("GL-MST-050 " with a trailing space, and "gl-ser-030" in lower case). I matched them to the SKUs in the orders anyway.

**Open question:** this is the first time I've read your export, so I haven't saved its format yet. It contains:
- **Payment methods:** Shopify Payments, PayPal Express Checkout, Gift card, and Bogus Gateway (Shopify's test payment method)
- **Financial statuses:** paid, partially refunded, refunded, voided
- **Tags:** pre-order, test

If these are all what you'd expect, I'll save them. Then anything new in next month's export will be pointed out. The figures above assume they're as expected.

I saved the full checked report, with the table of every product, as `files/margins_2026-08.md`.
