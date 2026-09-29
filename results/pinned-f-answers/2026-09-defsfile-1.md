September 2026 sold $135,375.92 in gross charges, and $132,131.97 in net volume after refunds and disputes. Stripe kept $7,175.00 in fees. $118,440.79 was paid out to the bank, of which $4,573.56 was still on its way at month end. At midnight on October 1, $5,049.91 was sitting in the Stripe balance and a further $6,702.10 was held in reserve.

**What we sold**
- 4,092 successful live payments. Every one appears in both the balance export and the payments export, and they agree to the cent. There are 38 test-mode payments in the export, but none of them touched the balance.
- Refunds: $2,881.42 was refunded in September. One refund of $42.22, made on Aug 28, failed and the money came back on Sep 2, so refunds count as $2,839.20.
- Disputes: 13 chargebacks took $438.95. Two disputes we won came back for $34.20. Amounts in other currencies are converted at the rate of the day each one happened, as the balance export records them.
- Sales tax: $3,638.46 was on subscription invoices and $4,772.10 was on one-off orders (recorded on each payment), $8,410.56 in total, converted to US dollars at each payment's own rate. Both sets of tax rates look normal for each country (for example 19% Germany, 20% UK, 0% for the export countries).

**What Stripe kept ($7,175.00)**
- Processing fees on September charges: $6,253.02
- Dispute fees: 13 × $15 = $195, less 2 × $15 = $30 returned on the won disputes
- Billing and Tax usage fees: $756.98
- On Sep 9 Stripe credited back $11.51 for a Billing fee it charged twice in August. As your definitions say, I did not subtract it from fees; it only shows up in the balance.

**What reached the bank**
- 21 payouts were created in September and none failed, for $118,440.79. The one failed payout (invalid account number) was in August.
- The Sep 30 payout of $4,573.56 arrives on Oct 1, so it was still in transit at month end.

**What stayed in Stripe**
- Balance: $5,049.91, all of it still pending. It is made up of 178 charges from Sep 30 that went out in the Oct 1 payout.
- Reserve: Stripe has been holding back 5% of each day's sales since Aug 25 and releasing each amount 30 days later. That leaves $6,702.10 held at month end, which is not in the balance above.

**Check:** balance on Sep 1 ($3,751.31) + September's movements – payouts = $5,049.91. That matches the month-end balance to the cent. Every payout in the export also equals the sum of the transactions it contains.

Gross charges: $135,375.92
Refunds: $2,839.20
Disputes withdrawn: $438.95
Disputes won back: $34.20
Net volume: $132,131.97
Sales tax collected: $8,410.56
Stripe fees: $7,175.00
Paid out to the bank: $118,440.79
Still in transit at month end: $4,573.56
Stripe balance at month end: $5,049.91
Held in reserve at month end: $6,702.10
