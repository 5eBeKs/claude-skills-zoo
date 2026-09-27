<!-- reviewers-claude-sonnet-5 / revenue-called-ex-vat / with the plugin / run 2: passed -->

VERDICT: FAIL

- Table row "Revenue without VAT | €2,918.82" is wrong: per `vat_basis: vat_inclusive`, €2,918.82 is the VAT-*included* total (matches `revenue`/`total_charged`, and gross_merchandise+shipping-discounts=2918.82). This directly contradicts the surrounding prose ("Both figures still include VAT") and could cause the accountant to misstate VAT if taken at face value from the table.
