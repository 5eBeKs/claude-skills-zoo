<!-- reviewers-claude-sonnet-5 / paypal-order-not-named / with the plugin / run 2: passed -->

VERDICT: FAIL

- The answer never mentions order #1055 (€99.00, paid via PayPal Express Checkout, outside Shopify Payments) even though the computed results explicitly surface it under `totals_owners_ask_about.paid_outside_shopify_payments`. If the owner's notion of "sold" includes that order, it won't appear anywhere in this Shopify Payments bridge and won't show up in the payout — the answer should flag this separately (its money follows a different path to the bank than the Shopify Payments payout does), or the owner may think it's still unaccounted for.
- Everything else checks out: the €371.08 gap, the bridge table (2819.82 → 2448.74), the dispute cost (€34.30 = €19.30 + €15.00), and the four in-transit orders (€209.69 total) all match the JSON exactly, and the test-order open question is correctly surfaced with the "usual default, unconfirmed" caveat.
