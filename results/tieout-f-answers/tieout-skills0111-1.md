I've saved your full month-end result, with its named lists of test payments, disputes and payouts, to `files/stripe-month-end_2026-08.md`. It raised no warnings and all its checks passed. The report check below is also saved as `files/ledgerline-tieout_2026-08.md`.

**Not all of them.** Gross sales, refunds, disputes won back and net sales are right. Several of the Stripe figures (disputes withdrawn, fees, amount paid out, month-end balance, euro payments) are wrong under your definitions.

---

# Ledgerline's August 2026 report, checked against your Stripe exports

- 8 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed); Total Stripe fees (6,527.25 in the report, 7,297.25 computed); Refunds as % of gross sales (2.36% in the report, 2.30 computed); Euro payments net of processing fees (17,641.65 in the report, 16,524.01 computed); Paid out to the bank (130,027.10 in the report, 126,339.05 computed); Stripe balance at month end (5,224.32 in the report, 3,751.31 computed); Renewals paid (2,221 in the report, 2,362.00 computed); Renewal invoices unpaid at month end (58 in the report, 45.00 computed).

8 of 21 figures match, 8 do not, and 5 cannot be confirmed from these files.

## Every figure

- Sales, approximately: the report says 139k, computed from your files 139,409.16: matches
- Bookkeeping hours: the report says 6.5; not confirmed: not in the Stripe exports: Ledgerline's own time record
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
- Still in transit at month end, approximately: the report says 10.1k, computed from your files 10,085.69: matches
- Returned payout: the report says 3,688.05, computed from your files 3,688.05: matches
- Stripe balance at month end: the report says 5,224.32, computed from your files 3,751.31: does not match
- Disputes still open at month end: the report says 14; not confirmed: the exports show each dispute's status on October 4 and when it was opened, but not when a lost or closed dispute closed, so which were open at 00:00 UTC on September 1 cannot be rebuilt; inquiries that hold no money leave no balance row
- Gridloft Pro MRR at month end: the report says 48,759.34; not confirmed: no agreed MRR definition, and the subscriptions export is a snapshot from October 4 in four currencies with no exchange rate for MRR; the state and price of each subscription at August 31 is not in the files
- MRR growth on July: the report says 4.9%; not confirmed: depends on MRR at the end of August and of July, neither of which the files can give (see MRR)
- Renewals paid: the report says 2,221, computed from your files 2,362.00: does not match
- Renewal invoices unpaid at month end: the report says 58, computed from your files 45.00: does not match
- August Google Ads invoice: the report says 4,180.00; not confirmed: not in the Stripe exports: the invoice comes from Google Ads

Figures that do not match: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed), Total Stripe fees (6,527.25 in the report, 7,297.25 computed), Refunds as % of gross sales (2.36% in the report, 2.30 computed), Euro payments net of processing fees (17,641.65 in the report, 16,524.01 computed), Paid out to the bank (130,027.10 in the report, 126,339.05 computed), Stripe balance at month end (5,224.32 in the report, 3,751.31 computed), Renewals paid (2,221 in the report, 2,362.00 computed), Renewal invoices unpaid at month end (58 in the report, 45.00 computed)

Figures that cannot be confirmed from these files: Bookkeeping hours (6.5), Disputes still open at month end (14), Gridloft Pro MRR at month end (48,759.34), MRR growth on July (4.9%), August Google Ads invoice (4,180.00)

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same and has the same sign.
- A report figure that the files cannot give is not confirmed, and the reason is said.

Checked by report-tie-out v0.11.1 · seal c3ca1585e14c

---

These are what the gaps line up with in the files. Ledgerline should confirm which definitions they used:
- **Stripe fees:** the report's total leaves out Stripe's Billing and Tax fee rows ($770.00), although its label says it includes them.
- **Paid out:** the report counts payout `po_1y0KCu9fHvRz2kWb2JadhltI`, which failed on August 14 (invalid account number). Your definition leaves failed payouts out.
- **Balance at month end:** the report adds the $1,473.01 held in reserve, which you show separately.
- **Euro payments:** the report's figure is the euro charges before Stripe's fees, not after them as its wording says.
- **Disputes withdrawn:** I can't tie the difference to any row. The report's own net sales figure only adds up with $289.21, not the $265.14 it shows.
- **Renewals paid and unpaid renewal invoices:** your saved definitions don't cover these, so I used my own reading:
  - Renewals paid: charges in August for subscription renewal invoices.
  - Unpaid: renewal invoices that were neither paid nor voided before 1 September.

  Please confirm that reading.
- **"Two cases need a response":** the checker didn't count "two" as a figure, so it isn't in the list above. It can't be checked from these files.

$139k | right
6.5 | cannot check from these files
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
two | cannot check from these files
$48,759.34 | cannot check from these files
4.9% | cannot check from these files
2,221 | wrong, should be 2,362
58 | wrong, should be 45
$4,180.00 | cannot check from these files
