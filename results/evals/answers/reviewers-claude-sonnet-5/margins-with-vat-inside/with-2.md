<!-- reviewers-claude-sonnet-5 / margins-with-vat-inside / with the plugin / run 2: passed -->

VERDICT: FAIL

- "Prices shown include VAT" directly contradicts the table, which is explicitly labeled "Revenue without VAT" (and computed as `revenue_ex_vat` — VAT already removed). As written, this line could lead the owner to believe the margin figures still include VAT, inflating their sense of the true margins. It should instead say something like "Your listed prices include 19% VAT; the revenue and margin figures above have that VAT removed."
- Minor: the currency (EUR) is never stated explicitly in the answer (only € symbols), and the answer doesn't spell out what the "usual" assumptions actually are (test orders excluded, sales counted as paid-any-status) before asking the owner to confirm them — it just gestures at "the questions below."
