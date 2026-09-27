<!-- reviewers-claude-sonnet-5 / refund-rate-digits-swapped / with the plugin / run 1: passed -->

VERDICT: FAIL

- Refund rate is wrong: table shows "4.2%" but computed `refund_rate_pct` is "2.4" (70.50/2,918.82 ≈ 2.4%) — digits appear transposed, and this would go straight to the accountant.
- Top products section only lists 3 of the 5 items in `top_skus_by_revenue` (omits Oolong 50g €256.00 and Ceramic Cup €252.00) despite the owner asking for "our best products" — worth including the full top-5 or noting it's a partial list.
