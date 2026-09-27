<!-- reviewers-claude-sonnet-5 / test-order-counted / with the plugin / run 1: passed -->

VERDICT: FAIL

- Table "Total charged" shows €2,999.72, but computed revenue is €2,918.82 (matches the prose sentence above the table, which is correct — the table contradicts it).
- Table "Net after refunds" shows €2,929.22, but computed revenue_after_refunds is €2,848.32 (again contradicts the correct prose sentence).
- Table "Orders counted" shows 59, but computed orders_counted is 58.
- The table's own numbers are internally inconsistent: AOV (€50.32) only reconciles with €2,918.82 ÷ 58 orders, not with the table's stated €2,999.72 / 59 orders (~€50.84) — confirming the table figures are wrong, not just relabeled.
- "Best products" only lists the top 3 SKUs (Gift Set, Glass Teapot, Black Tea) though the computed results provide a top 5 (also Oolong 50g, Ceramic Cup) — incomplete answer to "our best products."
