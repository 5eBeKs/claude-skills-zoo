<!-- numbers-c-claude-opus-5-5 / numbers-margins-c / without the plugin / run 3: passed -->

Three products lost money in August. A fourth, Peptide Serum (GL-NEW-001), has no unit cost in `cogs.csv`, so I couldn't check it. These figures are gross profit only: revenue without VAT, minus unit costs. I didn't have shipping, payment fees or ad spend, so they aren't included.

| SKU | Product | Units | Revenue (ex VAT) | Unit costs | Profit / loss |
|---|---|---|---|---|---|
| GL-SMP-001 | Sample Sachet | 188 | £0.00 | £65.80 | **−£65.80** |
| GL-CLR-001 | Summer Tin (clearance) | 21 | £100.87 | £121.80 | **−£20.93** (−21%) |
| GL-CLR-002 | Old Label Serum (clearance) | 35 | £276.29 | £294.00 | **−£17.71** (−6%) |

- **Sample Sachet** is given away free at £0.00, so every one shipped costs you £0.35. That's expected for a sample, but it's the largest loss.
- **The two clearance lines sell for less than they cost.** Summer Tin is £6.00 with VAT, which is £5.00 without it, against a £5.80 cost. Old Label Serum is £9.60 with VAT (£8.00 without) against £8.40. They also lost money in June and July, so this isn't new in August.
- **Peptide Serum (GL-NEW-001)** has no cost in `cogs.csv`, although 180 were sold in August for about £5,558 without VAT. It averaged £30.88 per unit without VAT after discounts and refunds. It only lost money if its unit cost is above that, which seems unlikely. Please add its cost so it can be confirmed.

Every other product made money, with gross margins of about 57–74%.

How I counted August:
- **Which orders:** orders placed in August that have shipped. I left out test orders (tagged "test" or paid through the test payment gateway), voided orders, and paid orders not yet shipped, including pre-orders. This follows the rules in `files/store_definitions.json`.
- **Revenue:** prices with the 20% VAT taken out. Shipping charges aren't counted as revenue.
- **Discounts:** each order-level discount (SUMMER10, WELCOME5) is split across that order's items in proportion to their price.
- **Refunds:** each refund reduces revenue by the refunded share of the order and counts in the month the order was placed. Refunded items that had already shipped still count their unit cost, because I assumed returned cosmetics can't be resold.
- **Cost list:** two entries in `cogs.csv` were written differently from the order export (`gl-ser-030` in lowercase, `GL-MST-050 ` with a trailing space). I matched them to their products.
