I checked every figure in Ledgerline's report against your October 4 Stripe exports. **8 of the 21 figures are right, 8 are wrong and 5 can't be checked from these files.**

The main figures come from the calculation your definitions are saved in, run for August 2026. Your full August answer from it, with every test payment, dispute and payout it names, is saved as `files/stripe-month-end_2026-08.md`.

That calculation doesn't give the refund and fee percentages, the euro payments, the returned payout or the renewal counts. I worked those out from the same exports with a short separate script. The renewal counts rest on my own reading, because your definitions don't cover renewals: renewal invoices paid in August, and renewal invoices neither paid nor cancelled by August 31. Please ask Ledgerline how they count renewals.

What the wrong figures come from, according to the exports:
- **Stripe fees:** the report leaves out the Billing and Tax fee rows, even though its label says they're included.
- **Paid out:** the report includes the payout that failed in mid-August.
- **Stripe balance:** the report adds the reserve into the balance; you count the reserve separately.
- **Euro payments:** the report gives the euro charges before Stripe's processing fees, but calls it "net of processing fees".
- **Disputes withdrawn:** the report's net sales line matches ours, but it only works with our disputes figure, not the report's own. Ledgerline would need to say which disputes they counted.

Here is the tie-out exactly as the check produced it (also saved as `files/report-tieout_2026-08.md`):

---

# Ledgerline's August 2026 report against your Stripe exports

- 8 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed); Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed); Refunds as a share of gross sales (2.36% in the report, 2.30 computed); Payments in euros, net of processing fees (17,641.65 in the report, 16,524.01 computed); Paid out to the bank (130,027.10 in the report, 126,339.05 computed); Stripe balance at month end (5,224.32 in the report, 3,751.31 computed); Renewals paid in the month (2,221 in the report, 2,364.00 computed); Renewal invoices unpaid at month end (58 in the report, 45.00 computed).

8 of 21 figures match, 8 do not, and 5 cannot be confirmed from these files.

## Figure by figure

- Sales, about: the report says 139k, computed from your files 139,409.16: matches
- Hours spent on the books: the report says 6.5; not confirmed: Ledgerline's own time sheet; nothing in the Stripe exports records it
- Gross sales: the report says 139,409.16, computed from your files 139,409.16: matches
- Refunds: the report says 3,204.12, computed from your files 3,204.12: matches
- Disputes (amounts withdrawn): the report says 265.14, computed from your files 289.21: does not match
- Disputes won back: the report says 53.45, computed from your files 53.45: matches
- Net sales after refunds and disputes: the report says 135,969.28, computed from your files 135,969.28: matches
- Total Stripe fees (processing, dispute and Billing/Tax usage fees): the report says 6,527.25, computed from your files 7,297.25: does not match
- Refunds as a share of gross sales: the report says 2.36%, computed from your files 2.30: does not match
- Processing fees as a share of gross sales: the report says 4.6%, computed from your files 4.60: matches
- Payments in euros, net of processing fees: the report says 17,641.65, computed from your files 16,524.01: does not match
- Paid out to the bank: the report says 130,027.10, computed from your files 126,339.05: does not match
- Still in transit at month end, about: the report says 10.1k, computed from your files 10,085.69: matches
- Payout returned in mid-August: the report says 3,688.05, computed from your files 3,688.05: matches
- Stripe balance at month end: the report says 5,224.32, computed from your files 3,751.31: does not match
- Dispute cases still open at month end: the report says 14; not confirmed: the exports show each dispute's status as of the October 4 export, not on August 31, and inquiries that hold no money leave no balance row; which cases were open at month end cannot be rebuilt
- Gridloft Pro MRR at month end: the report says 48,759.34; not confirmed: the subscriptions export is a snapshot of October 4 (current price, status and period), so the August 31 subscription book cannot be rebuilt, and no definition of MRR or of the rate for non-dollar plans was agreed
- MRR growth on July: the report says 4.9%; not confirmed: needs the July and August MRR, which these files cannot give (see MRR)
- Renewals paid in the month: the report says 2,221, computed from your files 2,364.00: does not match
- Renewal invoices unpaid at month end: the report says 58, computed from your files 45.00: does not match
- August Google Ads invoice: the report says 4,180.00; not confirmed: a Google Ads invoice; not in any Stripe export

Figures that do not match: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed), Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed), Refunds as a share of gross sales (2.36% in the report, 2.30 computed), Payments in euros, net of processing fees (17,641.65 in the report, 16,524.01 computed), Paid out to the bank (130,027.10 in the report, 126,339.05 computed), Stripe balance at month end (5,224.32 in the report, 3,751.31 computed), Renewals paid in the month (2,221 in the report, 2,364.00 computed), Renewal invoices unpaid at month end (58 in the report, 45.00 computed)

Figures these files cannot confirm: Hours spent on the books (6.5), Dispute cases still open at month end (14), Gridloft Pro MRR at month end (48,759.34), MRR growth on July (4.9%), August Google Ads invoice (4,180.00)

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same and has the same sign.
- A report figure that the files cannot give is not confirmed, and the reason is said.

Checked by report-tie-out v0.11.1 · seal faaf9054456d

---

$139k | right
6.5 hours | cannot check from these files
$139,409.16 | right
$3,204.12 | right
$265.14 | wrong, should be $289.21
$53.45 | right
$135,969.28 | right
$6,527.25 | wrong, should be $7,297.25
2.36% | wrong, should be 2.30%
4.6% | right
$17,641.65 | wrong, should be $16,524.01
$130,027.10 | wrong, should be $126,339.05
$10.1k | right
$3,688.05 | right
$5,224.32 | wrong, should be $3,751.31
14 | cannot check from these files
$48,759.34 | cannot check from these files
4.9% | cannot check from these files
2,221 | wrong, should be 2,364
58 | wrong, should be 45
$4,180.00 | cannot check from these files
