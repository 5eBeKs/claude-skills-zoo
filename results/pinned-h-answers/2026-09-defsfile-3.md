I've worked out every figure in your list from the October 3 exports, using the rules in `definitions.md`. The bookkeeping cross-checks all tie out. Billings less tax plus credit notes equals revenue recognised plus the change in deferred revenue, to within a cent. Cash, refunds and fees match Stripe's own September balance summary exactly.

**MRR:** $219,986.90 at September 30, up from $197,868.29 at August 31. September's rates add $184.28 to August's figure, which the definitions exclude from the movement. That leaves net new MRR of **+$21,934.33**:
- New: +$24,348.82 (194 customers)
- Expansion: +$4,554.45 (113 customers)
- Reactivation: +$520.74 (4 customers)
- Contraction: −$2,551.58 (71 customers)
- Churned: −$4,938.09 (42 customers)

**Customers:** 1,548 paying at month end, up from 1,392. We lost 42 and gained 198.

**Money in and out:**
- **Billings** were $341,477.31. This includes an unpaid $52,260 enterprise invoice and a £20,000 enterprise prepayment.
- **Cash collected** was $330,573.95: $265,093.91 by card and $65,480.04 by bank transfer.
- **Refunds** were $338.88. None failed in September.
- **Stripe fees** were $12,802.04: $10,126.15 on payments, $60 in chargeback fees, and $2,615.89 in separate fee rows (net of $30 of dispute fees Stripe returned).
- **Paid out to the bank** was $277,424.98, from four payouts that arrived Sep 3, 10, 17 and 24.

**Revenue:** $228,758.85 recognised; $593,809.997 deferred, which rounds to $593,810.00 — that's not a placeholder. The deferred balance is large because the enterprise licences were billed a year ahead.

**Decisions that change the numbers — please confirm:**
1. **Payout arriving Oct 1.** A $72,505.74 payout was created Sep 30 and arrives Oct 1, so I left it out. Stripe's September balance summary counts it, so its payout total is $349,930.72.
2. **16 subscriptions stuck unpaid since spring.** They were cancelled on Sep 30, but their invoices had failed and further invoices stopped being charged months earlier. They count as zero MRR at both month ends, not as September churn.
3. **Fee timing.** The fees include Stripe's August usage fees ($1,845.29 Billing and $755.60 Tax), because Stripe charged them on Sep 2. September's own usage fees ($2,319.33 + $899.61) were charged Oct 2, so they fall in October.
4. **Changes with unknown timing.** About 40 subscriptions changed seat count or plan with no invoice showing when. I placed each change at the midpoint of its possible window. If all of them happened before month end, MRR would be $82.62 higher.
5. **Cancellation credit notes.** Prorated cancellation refunds reduce revenue only for the unused part of the period after cancellation. All other credit notes reduce revenue over the whole invoice period.
6. **Reading the exports.** The subscriptions export has one row per plan, not per subscription: 368 subscriptions have two rows (a Business plan plus Business seats). The Oct 3 export blanks the coupon on cancelled subscriptions, so I took their coupon history from the invoices.

For my bookkeeper:
MRR at month end: $219,986.90
Net new MRR: $21,934.33
Churned MRR: $4,938.09
Paying customers at month end: 1,548
Customers lost: 42
Billings: $341,477.31
Cash collected: $330,573.95
Refunds: $338.88
Stripe fees: $12,802.04
Paid out to the bank: $277,424.98
Revenue recognised: $228,758.85
Deferred revenue at month end: $593,810.00
