<!-- reviewers-claude-sonnet-5 / revenue-called-ex-vat / with the plugin / run 1: passed -->

VERDICT: FAIL

- Table row "Revenue without VAT | €2,918.82" is wrong and self-contradicting: this figure is `total_charged`/`revenue`, which is VAT-inclusive (confirmed by `vat_basis: vat_inclusive` and the €466.00 VAT figure), and the very next sentence above the table states "Both figures still include VAT." An accountant relying on this label would misclassify a VAT-inclusive total as an ex-VAT figure. Should read "Revenue (VAT included)" or "Total charged (VAT included)".
