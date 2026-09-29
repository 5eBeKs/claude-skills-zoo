In August 2026 you sold $139,409.16 in gross charges. Net volume was $135,969.28. Stripe kept $7,297.25 in fees. $126,339.05 was paid out to the bank, and $10,085.69 of that was still in transit at month end. All figures follow `definitions.md`. They come from the balance transactions, which reconcile to every payout to the cent. The month-end balance also matches a roll-forward from the July 31 balance.

**What you sold**
- **Gross charges:** 4,264 successful live charges. 17 test-mode payments were left out.
- **Refunds:** 104 refunds were created in August, including 20 on June and July payments. One refund of an August payment failed and came back on September 2, so it reduces September, not August.
- **Disputes:** 10 disputes took $289.21 from the balance. Two disputes from June were won back, returning $53.45.
- **Sales tax:** $8,404.78, taken from invoice tax on subscription charges and the recorded tax on one-off orders. Each charge was converted to US dollars at its own exchange rate. The largest amounts are in EUR, GBP and USD.

**What Stripe kept**
- Processing fees: $6,407.25
- Dispute fees: 10 × $15 withdrawn, less 2 × $15 returned, which is $120.00
- Billing and Tax usage fees: $770.00, in 63 rows. Two things to know:
  - On August 11 the Billing usage fee for August 10 ($11.51) was charged twice. Stripe credited it back on September 9. As your rules say, that credit is not netted here, so it will show up in September.
  - The usage fees for July 31 were charged on August 1, so they count in August.

**What reached the bank**
- 18 payouts were created in August and did not fail.
- The August 13 payout of $3,688.05 failed on August 14 and is left out. That money was paid again in the August 18 payout.
- The August 31 payout of $10,085.69 arrived on September 1, so it was in transit at month end.

**What is still on its way**
- The balance at 00:00 UTC on September 1 was $3,751.31. That is $3,776.41 pending less $25.10 available, which is negative because of an August 31 dispute.
- A 5% rolling reserve started on August 25. The seven amounts withheld from August 25 to 31 add up to $1,473.01, and none of it had been released by month end. Stripe releases each amount after 30 days, starting September 24.

Gross charges: $139,409.16
Refunds: $3,204.12
Disputes withdrawn: $289.21
Disputes won back: $53.45
Net volume: $135,969.28
Sales tax collected: $8,404.78
Stripe fees: $7,297.25
Paid out to the bank: $126,339.05
Still in transit at month end: $10,085.69
Stripe balance at month end: $3,751.31
Held in reserve at month end: $1,473.01
