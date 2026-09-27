<!-- reviewers-claude-sonnet-5 / fees-labelled-refunds / with the plugin / run 2: passed -->

VERDICT: FAIL

- In the bridge table, refunds and card fees are swapped: it shows "minus refunds | €56.59" and "minus card fees | €70.50", but the computed data has refunds = €70.50 and card_fees = €56.59. The final total (€2,448.74) still comes out right, but the owner would be told refunds cost less and card fees cost more than what actually happened — the opposite of the real breakdown.
