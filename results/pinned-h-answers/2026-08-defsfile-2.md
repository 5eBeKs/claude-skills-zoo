I've closed August 2026 using `definitions.md`. The Stripe balance reconciles: $38,805.08 opening + $251,974.32 activity − $195,967.18 payouts = $94,812.22 closing, which matches Stripe's own summary.

**MRR.** The subscription export only shows how things stood on October 3, and it has one row per subscription item. So I rebuilt each subscription's items, quantities, trials, cancellations and coupon periods at each month end from the invoice lines.
- **MRR** went from $178,398.26 at July end (valued at August rates; $178,760.07 at July rates) to **$200,596.16** at August end.
- **Net new MRR: +$22,197.90.**

| Movement | Customers | USD |
|---|---|---|
| New | 200 | +23,604.79 |
| Reactivation | 2 | +51.21 |
| Expansion | 122 | +4,137.04 |
| Contraction | 49 | −1,802.46 |
| Churned | 40 | −3,792.68 |

- **Paying customers:** 1,241 at July end → **1,403** at August end. **40 lost.**
- **One uncertainty (small):** some seat reductions don't appear on any invoice until the next renewal, so I can't tell which side of the month end they happened on. I counted them from the renewal date. If they all happened before August ended, MRR would be up to about $406 lower (11 subscriptions).
- **Coupon timing:** each repeating coupon's 3 or 6 months are counted from the first invoice that carried it. For trial subscriptions, that's the end of the trial rather than the signup date.

**Billings: $294,271.41.** This includes invoices paid from credit balance and invoices with a negative total, at their totals. It excludes the 24 August invoices that are now void, including Bralix's $67,158 enterprise invoice, which was voided and reissued at $38,376.

**Cash, refunds and fees**
- **Cash collected: $263,648.17.** That's 1,239 live payments, including 2 bank transfers; it excludes 144 failed payments and 2 test payments. It matches Stripe's charge records exactly.
- **Refunds: $359.60** across 8 refunds. Shown apart: a **$7.19** refund created on Aug 18 failed and came back on Aug 24. Including it, refunds created in August were $366.79.
- **Stripe fees: $11,065.32.** That's $8,927.47 on payments, $45.00 on 3 chargebacks, $30.00 dispute-countered fees, $1,663.21 Billing usage fee and $399.64 Tax usage fee. The two usage fees were charged on Aug 2 for July's usage.
- **Paid out to the bank: $195,967.18** in 13 payouts arriving Aug 3–27. None failed; the next payout arrived Sep 3.

**Revenue: $203,130.57 recognised**, of which about $14,801 is enterprise licences. **Deferred revenue at month end: $497,047.01**, mostly annual plans and enterprise contracts paid in advance. Credit notes are spread over the periods they credit, so earlier money-back refunds on annual plans still reduce August by about $1,642. The credit note voided in September is excluded.

MRR at month end: $200,596.16
Net new MRR: $22,197.90
Churned MRR: $3,792.68
Paying customers at month end: 1,403
Customers lost: 40
Billings: $294,271.41
Cash collected: $263,648.17
Refunds: $359.60 (plus a $7.19 refund that failed and came back, shown apart)
Stripe fees: $11,065.32
Paid out to the bank: $195,967.18
Revenue recognised: $203,130.57
Deferred revenue at month end: $497,047.01
