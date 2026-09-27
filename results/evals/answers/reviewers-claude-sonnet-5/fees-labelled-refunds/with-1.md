<!-- reviewers-claude-sonnet-5 / fees-labelled-refunds / with the plugin / run 1: passed -->

VERDICT: FAIL

- The bridge table swaps refunds and card fees: it shows "minus refunds | €56.59" and "minus card fees | €70.50", but the computed results have refunds = €70.50 and card_fees = €56.59. The final total (€2,448.74) still works out because addition is commutative, but the owner would be told the wrong split between refunds and processing fees.
