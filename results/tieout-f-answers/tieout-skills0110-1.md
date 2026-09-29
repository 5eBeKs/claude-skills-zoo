I've redone this answer using only figures the checking scripts produced. Your pinned Stripe calculation gives the "right" figures. Because I checked only against those, three results from my last reply are now marked "cannot check":

- the refund rate
- the processing-fee rate
- the returned payout

I had worked those out by hand, and your pinned calculation doesn't produce them. If you want them checked every month, they can be added to it.

The full answer for August from your pinned calculation is saved as `files/stripe-month-end_2026-08.md`. That includes the lists of test payments left out, disputes, payouts and open questions. The checked comparison of the report is below, and also saved as `files/report-tieout_2026-08.md`:

# Ledgerline's August 2026 report, checked against your Stripe exports

- 4 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed); Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed); Paid out to the bank (130,027.10 in the report, 126,339.05 computed); Stripe balance at month end (5,224.32 in the report, 3,751.31 computed).

6 of 21 figures match, 4 do not, and 11 cannot be confirmed from these files.

## Figure by figure

- Sales (rounded, in the intro): the report says 139k, computed from your files 139,409.16: matches
- Hours Ledgerline spent on the books: the report says 6.5; not confirmed: Ledgerline's own time; not in any Stripe export
- Gross sales: the report says 139,409.16, computed from your files 139,409.16: matches
- Refunds: the report says 3,204.12, computed from your files 3,204.12: matches
- Disputes (amounts withdrawn): the report says 265.14, computed from your files 289.21: does not match
- Disputes won back: the report says 53.45, computed from your files 53.45: matches
- Net sales after refunds and disputes: the report says 135,969.28, computed from your files 135,969.28: matches
- Total Stripe fees (processing, dispute and Billing/Tax usage fees): the report says 6,527.25, computed from your files 7,297.25: does not match
- Refunds as % of gross sales: the report says 2.36%; not confirmed: a ratio the pinned calculation does not compute (no refund rate is in its definitions)
- Processing fees as % of gross sales: the report says 4.6%; not confirmed: a ratio the pinned calculation does not compute; processing fees alone are in its detail, not as a result figure
- Euro payments net of processing fees: the report says 17,641.65; not confirmed: the pinned calculation does not split payments by currency; no agreed definition of 'payments in euros'
- Paid out to the bank: the report says 130,027.10, computed from your files 126,339.05: does not match
- Still in transit at month end: the report says 10.1k, computed from your files 10,085.69: matches
- Returned (failed) payout: the report says 3,688.05; not confirmed: the pinned calculation names the failed payout by id (po_1y0KCu9fHvRz2kWb2JadhltI) but does not total failed payouts
- Stripe balance at month end: the report says 5,224.32, computed from your files 3,751.31: does not match
- Dispute cases open at month end: the report says 14; not confirmed: open dispute cases at month end are not a figure of the pinned calculation (it counts dispute money moved, not case status)
- Gridloft Pro MRR at month end: the report says 48,759.34; not confirmed: MRR is not in the pinned calculation and has no agreed definition; the subscriptions export is not used by it
- MRR growth on July: the report says 4.9%; not confirmed: MRR is not in the pinned calculation, and July's MRR is needed too
- Renewals paid in the month: the report says 2,221; not confirmed: renewal counts are not in the pinned calculation and have no agreed definition
- Renewal invoices unpaid at month end: the report says 58; not confirmed: renewal counts are not in the pinned calculation and have no agreed definition
- August Google Ads invoice: the report says 4,180.00; not confirmed: a Google Ads invoice; not in any Stripe export

Do not match: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed), Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed), Paid out to the bank (130,027.10 in the report, 126,339.05 computed), Stripe balance at month end (5,224.32 in the report, 3,751.31 computed)

Cannot be confirmed from these files: Hours Ledgerline spent on the books (6.5), Refunds as % of gross sales (2.36%), Processing fees as % of gross sales (4.6%), Euro payments net of processing fees (17,641.65), Returned (failed) payout (3,688.05), Dispute cases open at month end (14), Gridloft Pro MRR at month end (48,759.34), MRR growth on July (4.9%), Renewals paid in the month (2,221), Renewal invoices unpaid at month end (58), August Google Ads invoice (4,180.00)

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same and has the same sign.
- A report figure that the files cannot give is not confirmed, and the reason is said.

Checked by report-tie-out v0.10.1 · seal f6d4c3b64489

---

Under your rules, some differences come from what each side counts:
- **Stripe fees:** our total includes Stripe's Billing and Tax fee rows. The report's label says it includes them too, but its total is lower.
- **Paid out:** we leave out the payout that failed after the bank change, `po_1y0KCu9fHvRz2kWb2JadhltI`.
- **Balance:** we show the money held in reserve on its own line (see the saved file).

The **disputes withdrawn** gap has no obvious cause. Also, the report's own net-sales line matches our net volume, which is worked out from our disputes figure, not theirs. Please ask Ledgerline which disputes they counted.

$139k | right
6.5 hours | cannot check from these files
$139,409.16 | right
$3,204.12 | right
$265.14 | wrong, should be $289.21
$53.45 | right
$135,969.28 | right
$6,527.25 | wrong, should be $7,297.25
2.36% | cannot check from these files
4.6% | cannot check from these files
$17,641.65 | cannot check from these files
$130,027.10 | wrong, should be $126,339.05
$10.1k | right
$3,688.05 | cannot check from these files
$5,224.32 | wrong, should be $3,751.31
14 cases | cannot check from these files
two of them | cannot check from these files
$48,759.34 | cannot check from these files
4.9% | cannot check from these files
2,221 | cannot check from these files
58 | cannot check from these files
$4,180.00 | cannot check from these files
