<!-- numbers-c-claude-opus-5-5 / numbers-margins-c / without the plugin / run 1: passed -->

Two products you actually sell lost money in August: both **clearance lines**. The free Sample Sachet also shows a loss, but that's expected since it's given away.

| Product | Units | Revenue (ex VAT, after discounts and refunds) | Cost of goods | Profit |
|---|---|---|---|---|
| Summer Tin (clearance), GL-CLR-001 | 21 | £100.87 | £121.80 | **−£20.93** |
| Old Label Serum (clearance), GL-CLR-002 | 35 | £276.29 | £294.00 | **−£17.71** |
| Sample Sachet, GL-SMP-001 (free) | 188 | £0.00 | £65.80 | −£65.80 |

**Why the clearance lines lose money:** once you take the 20% VAT out, they sell for less than they cost, even before any discount codes.
- Summer Tin: £6.00 including VAT is £5.00 without it, against a £5.80 unit cost.
- Old Label Serum: £9.60 including VAT is £8.00 without it, against an £8.40 unit cost.

Refunds didn't affect either one; neither had any refunds in August.

**Everything else made money,** with margins between about 57% and 74%. Across all products, August profit before overheads and shipping costs was about £60,000, on £85,129 of revenue.

**Peptide Serum (GL-NEW-001) isn't in `cogs.csv`,** so I can't give you its profit. It brought in £5,558 on 180 units (£31.67 each without VAT). It would only lose money if it costs more than about £30.90 a unit, so it's probably fine, but please add its cost.

**How I counted, following `store_definitions.json`:**
- **Which orders count:** only August orders that have shipped. I left out the 9 test orders tagged "test", the 7 test-payment orders, pre-orders, voided or cancelled orders, and anything not yet shipped.
- **Revenue:** without VAT and without the shipping fee. Discount codes are split across each item in the order by its value.
- **Refunds:** taken off the order's month, split across its items the same way.
- **Product cost:** charged on every shipped unit, including refunded ones. I don't know which refunded items came back to you.
- **Cost file fixes:** two product codes in `cogs.csv` were written differently from the orders file (`gl-ser-030` in lowercase, `GL-MST-050 ` with a trailing space). I matched them to the orders anyway.
