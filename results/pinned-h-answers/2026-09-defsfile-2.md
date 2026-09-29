Here is September 2026. MRR ended the month at **$220,011.63**, up **$18,713.98** in net new MRR. That growth came almost entirely from new customers, partly offset by $7,967.00 of churn. Billings were $341,477.31 and cash collected was $330,573.95. Of that cash, Stripe kept $12,802.04 in fees and $338.88 went back out as refunds. $277,424.98 reached the bank. Revenue recognised was $228,760.09.

**MRR and customers**

| | |
|---|---|
| MRR at Aug 31 (August rates) | $201,106.26 |
| MRR at Aug 31 (September rates) | $201,297.65 |
| New (194 customers) | +$24,354.09 |
| Reactivation (4 customers) | +$520.74 |
| Expansion (114 customers) | +$4,497.44 |
| Contraction (74 customers) | −$2,691.29 |
| Churned (58 customers) | −$7,967.00 |
| **MRR at Sep 30** | **$220,011.63** |

The difference between the two August figures is exchange-rate movement worth $191.39. It is not part of net new MRR. Paying customers went from 1,408 to 1,548, and 58 customers were lost.

**Cash and revenue**
- **Billings:** $341,477.31 from 1,574 invoices finalized in September and not void. This includes the $52,260 enterprise invoice (PO 4500‑5245), which is still unpaid.
- **Cash collected:** $330,573.95. That is $265,093.91 from card charges plus $65,480.04 from two enterprise bank transfers. I left out two test-mode charges ($1,008) and 180 failed attempts. The total matches Stripe's September charge total exactly.
- **Refunds:** $338.88. The only refund that failed and came back was in August, so there is none to show separately for September.
- **Stripe fees:** $12,802.04. Per-transaction fees were $10,186.15, including $60 of dispute fees. The separate fee rows came to $2,615.89: the August Billing and Tax usage fees ($1,845.29 + $755.60) billed on Sept 2, plus $45 of dispute fees less $30 refunded. September's own usage fees ($3,218.94) were posted on Oct 2, so they fall in October.
- **Paid out to the bank:** $277,424.98, from four payouts arriving Sept 3, 10, 17 and 24.
- **Revenue recognised:** $228,760.09. Subscriptions were $206,952; enterprise contracts $19,603; one-off items $4,841; prorations −$425; credit notes −$2,211.
- **Deferred revenue:** $593,812.24. Most of it is annual subscriptions and enterprise contracts paid in advance.

**Judgement calls your bookkeeper should know about**
1. **The Oct 1 payout is left out.** A payout of $72,505.74 arrived on Oct 1. Stripe's September balance summary counts it, because it lands at 8 pm on Sept 30 New York time, and shows payouts of $349,930.72. Our rule uses the arrival date, which is Oct 1, so I put it in October.
2. **Some subscription changes aren't dated.** 40 subscriptions changed quantity or plan after their last invoice, and Stripe hasn't billed the adjustment yet. That means the exports don't show when the change happened. I assumed September, which is the likely case. The effect on MRR is only about −$400.
3. **Retention-coupon end dates are estimated.** Stripe doesn't export when a retention coupon was applied, so for three subscriptions I estimated whether the 25% retention coupon was still running at a month end. Each is worth a few dollars of MRR.

For your bookkeeper:

MRR at month end: $220,011.63
Net new MRR: $18,713.98
Churned MRR: $7,967.00
Paying customers at month end: 1,548
Customers lost: 58
Billings: $341,477.31
Cash collected: $330,573.95
Refunds: $338.88
Stripe fees: $12,802.04
Paid out to the bank: $277,424.98
Revenue recognised: $228,760.09
Deferred revenue at month end: $593,812.24
