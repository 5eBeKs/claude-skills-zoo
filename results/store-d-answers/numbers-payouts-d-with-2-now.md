**$572,456.23 reached your bank from Shopify Payments in June.** Card orders placed in June came to $691,562.27, so the gap is **$119,106.04**. Every dollar of that gap is accounted for (unexplained difference: $0.00), and the June total matches your payouts export exactly.

**Warning:** $105,011.68 of the bank figure comes from the payouts export alone. The payouts of June 1–4 carry transactions from before the transactions export starts, so that part couldn't be checked one transaction at a time.

**Separately,** $82,635.67 of June orders were paid outside Shopify Payments (PayPal, cash, bank deposit, manual, gift card). That money never goes through Shopify payouts, so don't look for it in the payout report.

## From June sales to the bank

| | USD |
|---|---:|
| Card orders placed in June (Shopify Payments, shipped yet or not) | 691,562.27 |
| Refunds processed in June | -82,726.47 |
| of which on orders from earlier months | 45,616.95 |
| Card fees | -25,967.07 |
| Disputes: amount and fees | -1,212.93 / -240.00 |
| Reserve held (-) or released (+) by Shopify | 0.00 |
| Failed payout paid again | 0.00 |
| Shopify adjustments | 0.00 |
| Still in transit at month end | -117,366.90 |
| **Paid out for June's card transactions** | **467,444.55** |
| Paid out in June for transactions before the transactions export starts | 105,011.68 |
| **Paid out to the bank in June** | **572,456.23** |

**Where the rest went:**
- **Timing:** $117,366.90 was still in transit at month end, in 1,512 orders due in early-July payouts.
- **Refunds:** $82,726.47 was refunded in June. Part of that was on May orders.
- **Card fees:** $25,967.07.
- **Disputes:** 16 disputes cost $1,452.93 in total, and none were won back in June.
- **Offsetting part of the gap:** the first June payouts partly carried May transactions.

## Things to check
- **Failed payout:** the payout of 2026-06-30 for $18,132.40 failed and was not paid again in June, so it isn't in the bank figure. Check that it was re-sent in July. A failed payout usually means the bank rejected it, for example after a change of account details.
- **Items that don't match up:**
  - 135 charges have no counted June order.
  - 179 orders were charged a different amount than the order total.
  - 5 orders were charged after June ended: #55864, #55838, #55835, #55667, #55378.
  - 87 orders were paid with a gift card plus a card; only the card part reaches payouts.
- **June 1–4 payouts:** the amounts from before the transactions export starts were 2026-06-04: 5,867.00; 2026-06-03: 60,256.61; 2026-06-02: 21,209.54; 2026-06-01: 17,678.53.

## Questions for you
These figures use the usual answer to each question until you confirm it. A different answer would change them.
- **Test orders** (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- **Export format:** are the payment methods, statuses, tags and currencies listed under "How this was counted" in the full report what you expect? If you confirm, they'll be saved as `store_shape.json`, and any new value next month will be flagged.

The full report is saved as `files/reconciliation_2026-06.md`. It lists every order in each list above, the 16 disputes one by one, the June 1–4 payout breakdown, and how each figure was counted, with file checksums. It passed the skill's number check (`Checked by shopify-month-end v0.10.1 · seal 94cc49258b58`).
