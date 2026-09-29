I've closed August 2026 against `definitions.md`. The subscription export only shows each subscription as of October 3, so I rebuilt the July 31 and August 31 positions from the invoice lines. That reconstruction is checked in the last section.

**MRR (at the August month-end rates)**
- MRR at August month end: **$200,371.90**. At July month end it was $178,971.56 at July rates, or $178,610.45 at August rates.
- Net new MRR: **+$21,761.45**. Exchange-rate changes took off another $361.11, which is not part of net new.
  - New: +$23,428.79 (199 customers)
  - Reactivation: +$51.21 (2)
  - Expansion: +$3,970.54 (117)
  - Contraction: −$1,896.40 (49)
  - Churned: −$3,792.68 (40)
- Paying customers went from 1,242 to **1,403**, and **40** were lost.

**Billings: $294,271.41.** This covers 1,421 invoices finalized in August, including tax and invoices paid from credit balance. It leaves out the 24 August invoices that have since been voided, including a $67,158 enterprise invoice.

**Cash and Stripe**
- **Cash collected: $263,648.17.** That is 1,239 card charges plus two bank transfers ($20,742), leaving out a $49 test charge. It matches Stripe's charge rows to the cent.
- **Refunds: $366.79** across 10 refunds. One refund of $7.19 failed and the money came back on August 24; I show that separately, so net refunds are $359.60. Chargebacks of $248.93 are a separate item and not counted as refunds.
- **Stripe fees: $11,065.32.** This is $8,927.47 in processing fees, $45 in dispute fees, $30 in dispute-countered fees, and the July Billing and Tax usage fees ($1,663.21 and $399.64) charged on August 2. The August usage fees are charged in September.
- **Paid out to the bank: $195,967.18** in 17 payouts arriving August 3–27. The one failed payout was in July.
- Check: $263,648.17 − $8,972.47 − $2,092.85 − $366.79 + $7.19 − $248.93 = $251,974.32, which is exactly Stripe's August activity total.

**Revenue: $203,123.41 recognised, $496,979.66 deferred at month end.**
- Revenue includes about $14.8k from enterprise contracts and $4.2k from one-off items, less $1.65k from credit notes.
- Deferred revenue is mostly annual plans, plus $103.5k of enterprise contracts.

**How reliable the MRR is**
- My rebuilt subscription values match the October 3 export for all but 41 of 2,335 subscriptions. Those 41 are changes after their last invoice, which Stripe hasn't billed yet.
- Some changes have no exact timestamp:
  - 11 seat reductions weren't prorated. For each, I only know the billing month it happened in, not whether it came before or after August 31. They're worth $406 in total, and I used the midpoint of each window.
  - 3 retention coupons (25% off for 3 months) have unknown start dates, worth a few dollars.
- The August month-end MRR could be off by up to a few hundred dollars. The billing, cash, fee and payout figures come straight from Stripe's records, and cash, refunds and fees reconcile exactly to Stripe's August activity total.
- You said the exports were taken on October 3, but today is [run date]. The data does run to October 3, so I treated that as the snapshot date for deciding which invoices are void "now".

MRR at month end: $200,371.90
Net new MRR: $21,761.45
Churned MRR: $3,792.68
Paying customers at month end: 1,403
Customers lost: 40
Billings: $294,271.41
Cash collected: $263,648.17
Refunds: $366.79
Stripe fees: $11,065.32
Paid out to the bank: $195,967.18
Revenue recognised: $203,123.41
Deferred revenue at month end: $496,979.66
