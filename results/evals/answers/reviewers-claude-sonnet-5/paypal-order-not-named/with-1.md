<!-- reviewers-claude-sonnet-5 / paypal-order-not-named / with the plugin / run 1: passed -->

VERDICT: FAIL

- The answer omits order #1055 (€99.00, paid via PayPal Express Checkout, not Shopify Payments) even though the computed results explicitly flag `paid_outside_shopify_payments: 99.00` under `totals_owners_ask_about`. This order is a real August sale that never entered the Shopify Payments bridge at all — it's not covered by refunds, fees, disputes, or in-transit, and won't show up in the Shopify Payments payout the answer reconciles against. Since the owner is asking generally "we sold more than landed in the bank," they need to know this €99 sale settled to a separate PayPal balance rather than the bank via Shopify Payouts, or their idea of "total sold" won't match the €2,819.82 "card sales" figure the whole bridge is anchored to.
