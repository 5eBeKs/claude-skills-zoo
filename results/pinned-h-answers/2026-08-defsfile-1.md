I've closed August 2026 using the rules in `definitions.md`. The cash figures tie exactly to Stripe's balance report. The MRR and revenue figures had to be rebuilt from invoice history, because the subscription export only shows each subscription as it stood on October 3.

**MRR and customers**
- MRR at August 31 was **$201,106.34**, up from $179,095.82 at July 31 (at July's rates). Valued at August's rates, July was $178,734.01, so the net increase was **$22,372.33**. The other −$361.81 is just exchange-rate movement and isn't counted in the increase.
- How MRR moved:

| Movement | Customers | USD |
|---|---|---|
| New | 204 | +23,938.98 |
| Expansion | 118 | +3,977.29 |
| Reactivation | 2 | +51.21 |
| Contraction | 49 | −1,802.46 |
| Churned | 40 | −3,792.68 |

- **1,408 paying customers** at August 31, up from 1,242. You lost 40 and gained 206.

**Billing and cash**
- **Billings: $294,271.41.** This excludes a $67,158 enterprise invoice voided on August 3, and 13 August invoices voided in a batch on September 30.
- **Cash collected: $263,648.17** from 1,239 live payments, including two bank transfers ($13,242 and $7,500). It matches Stripe's balance transactions line for line; one test-mode charge is excluded.
- **Refunds: $359.60.** Refunds created in August total $366.79, but one $7.19 refund failed and came back on August 24. I've left it out and show it separately.
- **Stripe fees: $11,065.32.** That's $8,927.47 on charges, $45.00 on three chargebacks, $1,663.21 Billing and $399.64 Tax usage fees for July, and two $15 dispute fees.
- **Paid out to the bank: $195,967.18** in 13 payouts arriving August 3–27. This matches Stripe's August balance summary.

**Revenue**
- **Recognised: $203,123.41.** That's $204,772.94 from invoice lines less $1,649.53 of credit notes.
- **Deferred at August 31: $496,979.66.** This is mostly annual plans and enterprise licences.

**Where I had to use judgement**
- **Plan and seat changes:** the exports don't record the date of changes made without a prorated charge. I dated them from the next invoice's period start. Some seat changes after each customer's last September invoice appear only in the October 3 export, so they don't affect August.
- **Retention coupon timing:** for four subscriptions on the 25%-off retention offer, the start date is only known to within a billing month. I dated it from the first discounted invoice; this moves MRR by at most a few dollars.
- **Credit notes:** I spread each one over the service period of the invoice it credits. Spreading cancellation refunds only from the cancellation date would change August revenue by $3.40.
- **Voided invoices:** following "not void now", the invoices voided on September 30 count in neither billings nor revenue, even though they were still valid when August closed.

MRR at month end: $201,106.34
Net new MRR: $22,372.33
Churned MRR: $3,792.68
Paying customers at month end: 1,408 (count, not dollars)
Customers lost: 40 (count, not dollars)
Billings: $294,271.41
Cash collected: $263,648.17
Refunds: $359.60 (plus a $7.19 refund that failed and was returned, not included)
Stripe fees: $11,065.32
Paid out to the bank: $195,967.18
Revenue recognised: $203,123.41
Deferred revenue at month end: $496,979.66
