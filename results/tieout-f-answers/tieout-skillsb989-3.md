I checked the report against your Stripe exports using the August calculation you already had pinned, run as it was set up with your definitions. It passed all its internal checks. Of the report's 21 numeric figures, **8 are right, 6 are wrong and 7 can't be checked from these files**. The report also mentions "two" disputes that need a response, written as a word; that can't be checked either.

Here is what each side counts where they differ. The files don't show why Ledgerline counted this way, so ask them:
- **Paid out:** the report's figure is ours plus the payout that failed on 14 August. Your definition leaves failed payouts out, and the report itself says that payout bounced.
- **Balance:** the report's figure is ours plus the money held in reserve. Your definition keeps the reserve on its own line.
- **Stripe fees:** the report leaves out the daily Billing and Tax usage fee rows, even though its label says they're included.
- **Disputes withdrawn:** the report's figure is lower than the 10 disputes Stripe withdrew in August. The report's own net figure, which is right, only adds up with our dispute total.
- **Euro payments:** the report's figure is the euro charges before Stripe's fees, though it says "net of fees."
- **Refund rate:** the report's percentage doesn't follow from its own refunds and gross sales.

A small extra script I wrote gave four of the figures; they are not part of your pinned calculation: the euro payments after fees, the refund rate, the processing-fee share and the failed payout. I saved this check as `files/report-tieout_2026-08.md` and your pinned August summary as `files/stripe-month-end_2026-08.md`.

---

# Ledgerline's August 2026 summary, checked against your Stripe exports

- 6 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed); Total Stripe fees (6,527.25 in the report, 7,297.25 computed); Refunds as % of gross sales (2.36% in the report, 2.30 computed); Euro payments net of processing fees (17,641.65 in the report, 16,524.01 computed); Paid out to the bank (130,027.10 in the report, 126,339.05 computed); Stripe balance at month end (5,224.32 in the report, 3,751.31 computed).

8 of 21 figures match, 6 do not, and 7 cannot be confirmed from these files.

## Figure by figure

- Sales (approximate): the report says 139k, computed from your files 139,409.16: matches
- Bookkeeping hours: the report says 6.5; not confirmed: Ledgerline's own time; not in the Stripe exports
- Gross sales: the report says 139,409.16, computed from your files 139,409.16: matches
- Refunds: the report says 3,204.12, computed from your files 3,204.12: matches
- Disputes (amounts withdrawn): the report says 265.14, computed from your files 289.21: does not match
- Disputes won back: the report says 53.45, computed from your files 53.45: matches
- Net sales after refunds and disputes: the report says 135,969.28, computed from your files 135,969.28: matches
- Total Stripe fees: the report says 6,527.25, computed from your files 7,297.25: does not match
- Refunds as % of gross sales: the report says 2.36%, computed from your files 2.30: does not match
- Processing fees as % of gross sales: the report says 4.6%, computed from your files 4.60: matches
- Euro payments net of processing fees: the report says 17,641.65, computed from your files 16,524.01: does not match
- Paid out to the bank: the report says 130,027.10, computed from your files 126,339.05: does not match
- In transit at month end (approximate): the report says 10.1k, computed from your files 10,085.69: matches
- Returned payout: the report says 3,688.05, computed from your files 3,688.05: matches
- Stripe balance at month end: the report says 5,224.32, computed from your files 3,751.31: does not match
- Dispute cases open at month end: the report says 14; not confirmed: a dispute's status at 31 August cannot be rebuilt: the payments export gives each dispute's status as of October 4 with no closing date, and an inquiry that holds no money has no balance row
- Gridloft Pro MRR: the report says 48,759.34; not confirmed: MRR is not among your agreed definitions, and subscriptions.csv shows each subscription as of October 4, not at 31 August
- MRR growth on July: the report says 4.9%; not confirmed: MRR is not among your agreed definitions, and the subscriptions export is an October 4 snapshot, so neither July's nor August's month-end MRR can be rebuilt
- Renewals paid: the report says 2,221; not confirmed: 'renewals paid' is not among your agreed definitions; the invoices export counts 2,364 renewal (subscription_cycle) invoices paid in August, or 2,344 created and paid in August, and neither reading gives the report's figure: ask Ledgerline how they count
- Renewal invoices unpaid at month end: the report says 58; not confirmed: 'unpaid at month end' is not among your agreed definitions; rebuilding from the invoices' paid and voided times gives 45 renewal invoices issued by 31 August that were neither paid nor voided before September 1: ask Ledgerline how they count
- Google Ads invoice: the report says 4,180.00; not confirmed: Google Ads invoice; not in the Stripe exports

Do not match: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed), Total Stripe fees (6,527.25 in the report, 7,297.25 computed), Refunds as % of gross sales (2.36% in the report, 2.30 computed), Euro payments net of processing fees (17,641.65 in the report, 16,524.01 computed), Paid out to the bank (130,027.10 in the report, 126,339.05 computed), Stripe balance at month end (5,224.32 in the report, 3,751.31 computed)

Cannot be confirmed from these files: Bookkeeping hours (6.5), Dispute cases open at month end (14), Gridloft Pro MRR (48,759.34), MRR growth on July (4.9%), Renewals paid (2,221), Renewal invoices unpaid at month end (58), Google Ads invoice (4,180.00)

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same and has the same sign.
- A report figure that the files cannot give is not confirmed, and the reason is said.

Checked by report-tie-out v0.11.1 · seal 110c4e92438c

---

$139k | right
6.5 hours | cannot check from these files
$139,409.16 | right
$3,204.12 | right
$265.14 | wrong, should be $289.21
$53.45 | right
$135,969.28 | right
$6,527.25 | wrong, should be $7,297.25
2.36% | wrong, should be 2.30 (percent of gross sales)
4.6% | right
$17,641.65 | wrong, should be $16,524.01
$130,027.10 | wrong, should be $126,339.05
$10.1k | right
$3,688.05 | right
$5,224.32 | wrong, should be $3,751.31
14 | cannot check from these files
two | cannot check from these files
$48,759.34 | cannot check from these files
4.9% | cannot check from these files
2,221 | cannot check from these files
58 | cannot check from these files
$4,180.00 | cannot check from these files
