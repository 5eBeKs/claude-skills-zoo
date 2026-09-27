<!-- reviewers-claude-opus-5-5 / wrong-product-below-cost / with the plugin / run 2: passed -->

VERDICT: FAIL
- The product sold below cost is named wrongly. The answer says "Ceramic Cup (CUP-CER-001)", but the figures (20 units, €109.24, €142.00, €-32.76, -30.0%) belong to Steel Strainer (STR-STL-001), which is the only product in `below_cost`.
- The answer contradicts itself. The table shows Ceramic Cup with 14 units and a +50.4% margin, while the headline says Ceramic Cup lost money. The owner can't tell which is true.
- Steel Strainer (STR-STL-001), the one product that actually loses money, is missing from the table and not named anywhere in the answer.
- Gift Set (SET-GFT-001) is missing from the table. Its 17 units and €700.00 revenue without VAT should be shown, with cost and margin marked "unknown".
- The margins are gross margins before €20.28 of discounts and €70.50 of refunds, which were not spread over products. The answer doesn't warn that real per-product margins are lower, so products close to cost could also be losing money.
