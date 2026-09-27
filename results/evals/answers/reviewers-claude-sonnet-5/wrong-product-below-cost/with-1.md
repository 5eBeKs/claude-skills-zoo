<!-- reviewers-claude-sonnet-5 / wrong-product-below-cost / with the plugin / run 1: passed -->

VERDICT: FAIL

- The "Sold below cost" callout mislabels the loss-making product: it names "Ceramic Cup (CUP-CER-001)" but the figures given (20 units, €109.24 revenue, €142.00 cost, €-32.76 margin, -30.0%) belong to Steel Strainer (STR-STL-001), not Ceramic Cup. Ceramic Cup's actual data (14 units, €211.76, €105.00, +€106.76, +50.4%) is a healthy margin and correctly shown in the table.
- As a result, the owner is told the wrong product loses money — Steel Strainer, the actual below-cost SKU, is never named anywhere in the answer (it's silently dropped from the table), while a profitable product (Ceramic Cup) is wrongly flagged as a loss-maker.
