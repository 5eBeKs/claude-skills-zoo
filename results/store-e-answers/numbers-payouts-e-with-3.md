**€351,295.07 reached the bank from Shopify Payments in August.** Card orders placed in August came to €436,193.70, so the gap is **€84,898.63**. That payout figure matches the payouts export (19 payouts), so you can check it against your bank statement. Every euro of the gap is accounted for; the unexplained difference is 0.00.

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 436,193.70 |
| − Refunds processed in August | 21,753.94 |
| of which on orders from earlier months | 11,769.23 |
| − Card fees | 9,559.62 |
| − Disputes: amount and fees | 811.49 + 45.00 |
| Reserve held (-) or released (+) by Shopify | -7,500.00 |
| − Still in transit at month end | 87,828.85 |
| = Paid out for August's card transactions | 313,784.04 |
| + Paid out in August for earlier months' transactions | 37,511.03 |
| = **Paid out to the bank in August** | **351,295.07** |

**Where the rest went:**
- **Still in transit, 87,828.85.** This is the biggest part. It covers 1,021 orders: most were paid out on 2 and 3 September, and 149 were in the failed payout below.
- **Failed payout on 2026-08-28, 14,902.03.** It wasn't paid again in August. Check in Shopify whether it has been paid since, and whether the bank details there are correct.
- **Refunds, 21,753.94.** Of this, 11,769.23 was for orders placed before August.
- **Card fees, 9,559.62.**
- **Reserve, 7,500.00.** Shopify was still holding this at month end.
- **Disputes, 856.49 net cost** across 7 disputes: #54410, #59420, #47732, #56944, #55843, #57176, #55031. None was won back in August.
- **Late-July sales, 37,511.03.** Payouts in early August also carried this money from late-July sales, which makes the gap smaller.

**Not in the payouts at all:** 2,058 orders (€240,650.52) were paid with PayPal, Klarna, bank deposit, cash, gift card or manual payment. That money comes through those channels, not Shopify payouts, so don't look for it there.

**Orders where the charge and the order don't line up one-to-one:**
- **No card charge found for 6 orders:** #66633, #65713, #64777, #63765, #63758, #63757.
- **Charged amount differs from the order total for 19 orders:** #66587, #65607, #65290, #65125, #64246, #63920, #63249, #63194, #62844, #62770, #62729, #62643, #62317, #61764, #61581, #61533, #61128, #60414, #60345.
- **No counted August order for 73 card charges.**
- **Rest charged after month end:** #66416 was charged 189.00 on 2026-09-01.
- **Gift card plus card:** 50 orders were paid partly with a gift card. Only the card part reaches the payouts.

**Questions for you.** The figures above use the usual answers until you confirm them; a different answer would change them.
- Test orders (tagged "test", or paid through Shopify's test gateway): should they be left out of sales (the usual answer), or counted?
- Are the payment methods, statuses, tags and currencies in the full report the ones you expect? If so, I'll record them, and any new value next month will be flagged.

The full report, with every order in each list, is saved at `files/reconciliation_2026-08.md`.

Checked by payout-reconciliation v0.10.1 · seal 8c309a37b1f2
