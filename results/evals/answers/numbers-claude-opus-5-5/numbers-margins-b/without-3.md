<!-- numbers-claude-opus-5-5 / numbers-margins-b / without the plugin / run 3: passed -->

**Only one product loses money: the Sample Votive (MO-SMP-001).** You give it away at $0.00 and it costs $1.10, so the 9 sent out in August cost you **$9.90**. Every product you charge for makes a healthy gross margin of 60–69%.

### August gross margin by product

I used line-item prices, which don't include tax, minus unit cost from `cogs.csv`.

| Product | SKU | Units | Price | Unit cost | Margin/unit | Gross profit | Margin |
|---|---|---|---|---|---|---|---|
| Reed Diffuser | MO-DIF-001 | 39 | $32.00 | $11.20 | $20.80 | $811.20 | 65% |
| Cedar Candle 8oz | MO-CND-001 | 27 | $24.00 | $7.40 | $16.60 | $448.20 | 69% |
| Fig Candle 8oz | MO-CND-002 | 22 | $24.00 | $7.90 | $16.10 | $354.20 | 67% |
| Travel Tin Trio | MO-CND-010 | 24 | $19.50 | $6.10 | $13.40 | $321.60 | 69% |
| Wick Trimmer | MO-WCK-001 | 27 | $14.00 | $5.20 | $8.80 | $237.60 | 63% |
| Match Cloche | MO-MAT-001 | 33 | $12.00 | $4.80 | $7.20 | $237.60 | 60% |
| **Sample Votive** | MO-SMP-001 | 9 | $0.00 | $1.10 | **−$1.10** | **−$9.90** | — |

### Orders I left out or adjusted
- **Excluded:**
  - #1998–#2000, which were placed on July 31.
  - #2008, which was voided and cancelled.
  - #2011 and #2044, which were paid through "Bogus Gateway (for testing)".
- **#2038 (fully refunded, one Cedar Candle and one Match Cloche):** I didn't count it as a sale. If those items weren't returned to stock, it cost you another $12.20 in goods.
- **Small adjustments that don't change the answer:** two SUMMER5 discounts ($10 total) and a $12 partial refund on #2049.
- **Cost sheet fix:** `cogs.csv` lists the Cedar Candle SKU as `mo-cnd-001 `, in lowercase with a trailing space. I matched it to `MO-CND-001`. Any tool that matches SKUs exactly would miss it and show the Cedar Candle as having no cost.

### What this doesn't cover
This only counts the cost of the goods. The data doesn't include shipping, packaging or card fees. Shipping is the one to check: orders of about $50 or more were charged $0 shipping. Small free-shipping orders are where another product could turn out to lose money, and the Match Cloche is closest because it has the smallest margin at $7.20 a unit. If you share your average shipping and fee costs, I can redo this with them included.

I counted everything by hand because I didn't have a way to run a script here. The margins are large enough that a small counting error wouldn't change which product loses money.
