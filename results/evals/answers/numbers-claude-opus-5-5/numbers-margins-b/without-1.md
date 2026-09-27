<!-- numbers-claude-opus-5-5 / numbers-margins-b / without the plugin / run 1: passed -->

**Short answer: only the Sample Votive (MO-CND-SMP-001) loses money.** It's given away at $0.00 and costs $1.10, so it's a deliberate giveaway rather than a pricing problem. Every product you actually charge for has a healthy margin.

**August gross margin by product** (price minus unit cost; tax isn't counted as revenue)

| Product | SKU | Price | Unit cost | Margin/unit | Units | Aug. margin |
|---|---|---|---|---|---|---|
| Reed Diffuser | MO-DIF-001 | $32.00 | $11.20 | $20.80 (65%) | 39 | $811.20 |
| Cedar Candle 8oz | MO-CND-001 | $24.00 | $7.40 | $16.60 (69%) | 27 | $448.20 |
| Fig Candle 8oz | MO-CND-002 | $24.00 | $7.90 | $16.10 (67%) | 22 | $354.20 |
| Travel Tin Trio | MO-CND-010 | $19.50 | $6.10 | $13.40 (69%) | 24 | $321.60 |
| Wick Trimmer | MO-WCK-001 | $14.00 | $5.20 | $8.80 (63%) | 27 | $237.60 |
| Match Cloche | MO-MAT-001 | $12.00 | $4.80 | $7.20 (60%) | 33 | $237.60 |
| **Sample Votive** | MO-SMP-001 | **$0.00** | $1.10 | **−$1.10** | 9 | **−$9.90** |

Total is about $2,400, or about $2,380 after the two $5 SUMMER5 discounts and a $12 partial refund. Those don't change the answer for any product.

**What I left out of the order export:**
- Orders #1998–2000, because they were placed on July 31.
- #2008, which was voided.
- #2011 and #2044, which were paid through "Bogus Gateway (for testing)".
- #2038, which was fully refunded. If those items weren't returned, you also lost $12.20 in product cost on it.
- One SKU in `cogs.csv` is written `mo-cnd-001 ` (lowercase, with a trailing space). I matched it to Cedar Candle, but a strict lookup would miss it, so it's worth fixing.

**Things worth checking:**
1. **Travel Tin Trio cost.** If $6.10 is the cost of one tin rather than the whole set of three, the Trio actually costs $18.30. That leaves only $1.20 on a $19.50 sale, and payment fees would push it into a loss. Please confirm which it is.
2. **Costs I don't have.** The analysis only covers product cost. It doesn't include payment processing fees, your actual shipping costs (orders over about $50 ship free), or packaging. Those hit the $12 Match Cloche and $14 Wick Trimmer hardest when someone orders one by itself. If you share shipping and fee costs, I can work out profit per order.
