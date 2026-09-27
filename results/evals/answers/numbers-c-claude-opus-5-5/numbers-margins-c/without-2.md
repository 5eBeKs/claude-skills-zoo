<!-- numbers-c-claude-opus-5-5 / numbers-margins-c / without the plugin / run 2: passed -->

Three products lost money in August, and one more couldn't be checked because it has no unit cost on file.

| Product | Units | Revenue (ex VAT) | Cost of goods | **Profit** |
|---|---|---|---|---|
| Sample Sachet (GL-SMP-001) | 188 | £0.00 | £65.80 | **–£65.80** |
| Summer Tin, clearance (GL-CLR-001) | 21 | £100.87 | £121.80 | **–£20.93** |
| Old Label Serum, clearance (GL-CLR-002) | 35 | £276.29 | £294.00 | **–£17.71** |

The combined August loss on these three is about **£104**.

- **Sample Sachet:** it sells for £0, so every sachet costs £0.35 with nothing coming back. That's probably an intended giveaway rather than a problem.
- **The two clearance lines are priced below cost.** Summer Tin sells for £6.00, which is £5.00 after VAT, against a £5.80 cost. Old Label Serum sells for £9.60, which is £8.00 after VAT, against £8.40. They lose money on every unit even before discounts. The same three products lost money in June and July too.
- **Peptide Serum (GL-NEW-001) has no row in `cogs.csv`.** It made £5,558 revenue excluding VAT on 180 units, but I can't calculate its profit without a cost. It would only lose money if each unit cost more than about £30.88, which seems unlikely, but you should add its cost to confirm.

Every other product made money. Margins ranged from about 57% (Travel Minis Set) to 74% (Hand Cream).

**How I counted, using the rules in `store_definitions.json`:**
- **Which orders count:** August means orders created in August. Only shipped orders count; I left out test orders, Bogus Gateway orders, pre-orders, unshipped orders and voided or cancelled orders.
- **Revenue:** it excludes VAT and shipping. Discounts are split across each order's items by value, and refunds come off in proportion to each item's share of the order.
- **SKU matching:** some SKUs in `cogs.csv` had lowercase letters or trailing spaces (for example `gl-ser-030` and `GL-MST-050 `). I normalised them so they match the orders.
- **Refunded orders:** I kept the cost of goods on shipped orders that were later refunded, assuming the stock doesn't come back. None of the three loss-makers depends on this assumption.
