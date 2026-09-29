I've saved two files next to your exports:

- `files/stripe-month-end_2026-08.md` is the full August answer from your pinned calculation, including every item it lists by ID: 17 test payments left out, 10 disputes withdrawn, 2 disputes won back, 1 failed payout, 1 payout in transit and 1 payout that includes rows from before the balance export begins. All of its checks passed and it gave no warnings.
- `files/report-tieout_2026-08.md` is the check of the report, figure by figure.

Here are August's figures from the pinned calculation, exactly as it wrote them:

Gross charges: $139,409.16
Refunds: $3,204.12
Disputes withdrawn: $289.21
Disputes won back: $53.45
Net volume: $135,969.28
Sales tax collected: $8,404.87
Stripe fees: $7,297.25
Paid out to the bank: $126,339.05
Still in transit at month end: $10,085.69
Stripe balance at month end: $3,751.31
Held in reserve at month end: $1,473.01

Here is the check of the report, exactly as it came out:

# Ledgerline's August 2026 report checked against your Stripe exports

- 6 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed); Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed); Refunds as a share of gross sales (2.36% in the report, 2.30 computed); Euro payments net of processing fees (17,641.65 in the report, 16,524.01 computed); Paid out to the bank (130,027.10 in the report, 126,339.05 computed); Stripe balance at month end (5,224.32 in the report, 3,751.31 computed).

8 of 21 figures match, 6 do not, and 7 cannot be confirmed from these files.

## Figure by figure

- Sales (rounded, in intro): the report says 139k, computed from your files 139,409.16: matches
- Bookkeeping hours: the report says 6.5; not confirmed: not in the files: the bookkeeper's own time
- Gross sales: the report says 139,409.16, computed from your files 139,409.16: matches
- Refunds: the report says 3,204.12, computed from your files 3,204.12: matches
- Disputes (amounts withdrawn): the report says 265.14, computed from your files 289.21: does not match
- Disputes won back: the report says 53.45, computed from your files 53.45: matches
- Net sales after refunds and disputes: the report says 135,969.28, computed from your files 135,969.28: matches
- Total Stripe fees (processing, dispute and Billing/Tax usage fees): the report says 6,527.25, computed from your files 7,297.25: does not match
- Refunds as a share of gross sales: the report says 2.36%, computed from your files 2.30: does not match
- Processing fees as a share of gross sales: the report says 4.6%, computed from your files 4.60: matches
- Euro payments net of processing fees: the report says 17,641.65, computed from your files 16,524.01: does not match
- Paid out to the bank: the report says 130,027.10, computed from your files 126,339.05: does not match
- Still in transit at month end: the report says 10.1k, computed from your files 10,085.69: matches
- Returned payout: the report says 3,688.05, computed from your files 3,688.05: matches
- Stripe balance at month end: the report says 5,224.32, computed from your files 3,751.31: does not match
- Open dispute cases at month end: the report says 14; not confirmed: not in these files: there is no disputes export, and the balance export shows only money moved, not a case's status or whether it is an inquiry
- Gridloft Pro MRR at end of August: the report says 48,759.34; not confirmed: not on the owner's definitions: MRR is not one of the agreed month-end figures and no definition of it (which plans, discounts, currencies, trials, past-due) has been agreed, so it is not computed
- MRR growth on July: the report says 4.9%; not confirmed: not on the owner's definitions: needs an agreed MRR definition for both July and August
- Renewals paid: the report says 2,221; not confirmed: not on the owner's definitions: what counts as a renewal (billing reason, paid in or created in the month) has not been agreed, so it is not computed
- Renewal invoices unpaid at month end: the report says 58; not confirmed: not on the owner's definitions, and the invoices export was taken on October 4, so an invoice's status at August month end cannot be read from it
- August Google Ads invoice: the report says 4,180.00; not confirmed: not in these files: the Google Ads invoice is outside Stripe

Do not match: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed), Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed), Refunds as a share of gross sales (2.36% in the report, 2.30 computed), Euro payments net of processing fees (17,641.65 in the report, 16,524.01 computed), Paid out to the bank (130,027.10 in the report, 126,339.05 computed), Stripe balance at month end (5,224.32 in the report, 3,751.31 computed)

Cannot be confirmed from these files: Bookkeeping hours (6.5), Open dispute cases at month end (14), Gridloft Pro MRR at end of August (48,759.34), MRR growth on July (4.9%), Renewals paid (2,221), Renewal invoices unpaid at month end (58), August Google Ads invoice (4,180.00)

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same and has the same sign.
- A report figure that the files cannot give is not confirmed, and the reason is said.

Checked by report-tie-out v0.10.1 · seal 3d59371f49cb

---

Three things to know about the check:

- **Extra figures:** the two percentages, the euro total and the returned payout aren't in the pinned calculation. I worked them out from its results and the same exports: the euro total from the balance export, the payout amount from the payouts export.
- **Ask Ledgerline:** I can't tell what the report counts for disputes withdrawn, Stripe fees, paid out, the balance or the euro payments. Ask them to say, figure by figure.
- **"Two" disputes:** the report writes this count as a word, which the checking tool doesn't read, so I added it to the list below myself. There's no disputes export, so it can't be checked.

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
two | cannot check from these files
$48,759.34 | cannot check from these files
4.9% | cannot check from these files
2,221 | cannot check from these files
58 | cannot check from these files
$4,180.00 | cannot check from these files
