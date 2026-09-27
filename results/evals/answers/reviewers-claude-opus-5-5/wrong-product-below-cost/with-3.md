<!-- reviewers-claude-opus-5-5 / wrong-product-below-cost / with the plugin / run 3: passed -->

VERDICT: FAIL
- Wrong product named as the loss-maker: "Sold below cost" says Ceramic Cup (CUP-CER-001), but the figures there (20 units, €109.24, €142.00, €-32.76, -30.0%) belong to Steel Strainer (STR-STL-001). The results list only STR-STL-001 in `below_cost`.
- The answer contradicts itself: Ceramic Cup is called a loss-maker at the top, but the table shows it with 14 units and a profit of €106.76 (50.4%).
- Steel Strainer, the only product that actually loses money, is missing from the table.
- Gift Set (SET-GFT-001) is missing from the table, so its 17 units and €700.00 of revenue without VAT aren't shown anywhere. It should appear with margin "unknown".
