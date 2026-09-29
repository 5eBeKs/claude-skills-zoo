## August 2026: €351,295.07 reached the bank, €84,898.63 less than card sales

The full answer is saved at `files/reconciliation_2026-08.md`. It lists every order, and the check passed (`Checked by payout-reconciliation v0.10.1 · seal f99a0dd6d096`). Below are the same figures with the long order lists shortened to counts.

Card orders placed in August came to **€436,193.70**. The 19 payouts that reached the bank in August came to **€351,295.07**, which matches your payouts export. After the order-level differences described below, nothing is left unexplained (€0.00).

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 436,193.70 |
| − Refunds processed in August | 21,753.94 |
| of which on orders from earlier months | 11,769.23 |
| − Card fees | 9,559.62 |
| − Disputes: amount and fees | 811.49 + 45.00 |
| Reserve held (-) or released (+) by Shopify | -7,500.00 |
| − Still in transit at month end | 87,828.85 |
| **= Paid out for August's card transactions** | **313,784.04** |
| + Paid out in August for earlier months' transactions | 37,511.03 |
| **= Paid out to the bank in August** | **351,295.07** |

**Where the rest went:**
- **Still in transit (the biggest part):** 1,021 late-August transactions were paid out in early September, so they aren't in August's bank figure.
- **Refunds:** about half of the refund total was on orders from July, not August.
- **Card fees.**
- **Reserve:** Shopify is still holding €7,500.00 at month end.
- **Disputes:** 7 disputes, with a net cost of €856.49. They are on orders #54410, #59420, #47732, #56944, #55843, #57176 and #55031.
- **Partly offset by July sales:** 434 transactions from the end of July were paid out in August.

**The middle lines of the table don't add up on their own.** The rows between card orders and "paid out for August" come up short of the "paid out" line. I checked that the unmatched items below make up exactly that difference:
- 73 charges have no counted order.
- 6 card orders have no charge: #66633, #65713, #64777, #63765, #63758, #63757.
- 19 orders were charged a different amount than the order total, for example #66587 (233.00 ordered, 114.00 charged).
- #66416 had the rest of its payment charged on 2026-09-01.

They're worth a look, but they aren't missing money.

**Also worth checking:**
- **Failed payout:** the payout of 14,902.03 on 2026-08-28 failed and wasn't paid again in August. Check on your bank statement whether and when it arrived.
- **Sales not paid through Shopify Payments:** 2,058 orders (€240,650.52) were paid by PayPal, Klarna, bank deposit and similar. They never appear in Shopify payouts, so look for that money in those accounts.
- **Gift cards:** on 50 orders a gift card paid part of the total. Only the card part reaches the payouts.

**How this was counted:** the orders and transactions cover all 31 days of August. The bank figure was checked against the payouts export.

**Two questions for you.** The figures use the usual answer to each until you confirm, and a different answer would change them:
- **Test orders:** should orders tagged "test", or paid through Shopify's test gateway, stay out of sales (the usual choice), or be counted?
- **Export format:** are the payment methods, statuses, tags and currencies listed in the saved file all what you'd expect? If so, I'll record them, and anything new next month will be flagged.
