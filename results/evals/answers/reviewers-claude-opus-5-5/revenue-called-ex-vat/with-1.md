<!-- reviewers-claude-opus-5-5 / revenue-called-ex-vat / with the plugin / run 1: passed -->

VERDICT: FAIL
- The first table row is labelled "Revenue without VAT", but €2,918.82 includes VAT: the results give `vat_basis: vat_inclusive`, with €466.00 of VAT inside that total. The answer's own opening sentence says the figure includes VAT, so the table contradicts it, and the accountant could book the wrong basis. The row should read "Total charged (VAT and shipping included)". The figure without VAT is €2,452.82, but the results don't report it, so it should only be added if it is computed and labelled.
