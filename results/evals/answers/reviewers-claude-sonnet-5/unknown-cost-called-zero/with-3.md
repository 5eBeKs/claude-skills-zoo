<!-- reviewers-claude-sonnet-5 / unknown-cost-called-zero / with the plugin / run 3: passed -->

VERDICT: FAIL

- The Gift Set line ("no cost in the sheet, so it is pure margin") misstates the data: `unit_cost`/`gross_margin` are `null`/"unknown" because cost is unavailable, not because the product has zero cost. Calling it "pure margin" implies all €700 revenue is profit, which the data does not support and could lead the owner to think Gift Set is highly profitable when its true margin (and whether it loses money) is unknown.
