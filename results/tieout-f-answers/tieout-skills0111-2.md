I checked the report against the calculation you already agreed and saved for your Stripe month-end, using your definitions. Four of its money figures are wrong, and three more are off when I checked them directly against the exports. Gross sales, refunds, disputes won back, net sales and the in-transit amount are right.

- **Fees, payouts and balance:** each difference comes to an exact amount from your files.
  - **Stripe fees:** the report leaves out Stripe's Billing and Tax fee rows, even though its label says they're included.
  - **Paid out to the bank:** the report counts the payout that bounced on 14 August.
  - **Stripe balance at month end:** the report includes the money held in reserve.
- **Disputes withdrawn:** I can't explain the gap from the files. Ledgerline should say how they got their figure.
- **Refund rate, euro payments and returned payout:** your saved calculation doesn't produce these, so the check below lists them as "not confirmed". I checked them with direct sums on the exports, and that is where the last lines come from. The euro figure in the report is the gross amount; it isn't net of Stripe's fees as the report says.
- **Open disputes, MRR and renewals:** the exports show these only as of October 4, not at the end of August. Your definitions also don't cover MRR or renewals, so ask Ledgerline how they count them.

The full August answer from your saved calculation is in `files/stripe-month-end_2026-08.md`. It lists every item left out, including the 17 test payments. The check below is also saved as `files/report-tieout_2026-08.md`:

---

# Ledgerline August 2026 report, checked against your Stripe exports

- 4 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed); Total Stripe fees (6,527.25 in the report, 7,297.25 computed); Paid out to the bank (130,027.10 in the report, 126,339.05 computed); Stripe balance at month end (5,224.32 in the report, 3,751.31 computed).

6 of 21 figures match, 4 do not, and 11 cannot be confirmed from these files.

## Figure by figure

- Sales (approx.): the report says 139k, computed from your files 139,409.16: matches
- Gross sales: the report says 139,409.16, computed from your files 139,409.16: matches
- Refunds: the report says 3,204.12, computed from your files 3,204.12: matches
- Disputes (amounts withdrawn): the report says 265.14, computed from your files 289.21: does not match
- Disputes won back: the report says 53.45, computed from your files 53.45: matches
- Net sales after refunds and disputes: the report says 135,969.28, computed from your files 135,969.28: matches
- Total Stripe fees: the report says 6,527.25, computed from your files 7,297.25: does not match
- Refunds as % of gross sales: the report says 2.36%; not confirmed: a ratio the pinned calculation does not publish; from its figures, refunds 3,204.12 / gross charges 139,409.16 = 2.30%
- Processing fees as % of gross sales: the report says 4.6%; not confirmed: a ratio the pinned calculation does not publish; from its figures, processing fees 6,407.25 / gross charges 139,409.16 = 4.60%
- Euro payments net of Stripe processing fees: the report says 17,641.65; not confirmed: euro payments are not a figure of the pinned calculation; summed directly from the balance export (August live charges with customer currency eur): gross 17,641.65, fees 1,117.64, net 16,524.01, so the report's figure is the gross, not net of fees
- Paid out to the bank: the report says 130,027.10, computed from your files 126,339.05: does not match
- Still in transit at month end (approx.): the report says 10.1k, computed from your files 10,085.69: matches
- Returned payout: the report says 3,688.05; not confirmed: the payout's amount is not a figure of the pinned calculation (it names the failed payout po_1y0KCu9fHvRz2kWb2JadhltI); payouts.csv shows it at 3,688.05, failed 2026-08-14 with invalid_account_number
- Stripe balance at month end: the report says 5,224.32, computed from your files 3,751.31: does not match
- Dispute cases open at month end: the report says 14; not confirmed: dispute case status at month end is not in these exports (they were taken on October 4 and show only current dispute status)
- Gridloft Pro MRR: the report says 48,759.34; not confirmed: MRR is not a figure of the owner's definitions, and the subscriptions export is an October 4 snapshot, not the state at August month end
- MRR growth on July: the report says 4.9%; not confirmed: needs July and August MRR, which these files do not give as of those month ends
- Renewals paid: the report says 2,221; not confirmed: not a figure of the pinned calculation; renewals are not defined in the owner's definitions
- Renewal invoices unpaid at month end: the report says 58; not confirmed: invoice status at August month end is not in the October 4 invoices export (it shows current status only)
- Bookkeeping hours: the report says 6.5; not confirmed: Ledgerline's own time, not in Stripe
- Google Ads invoice: the report says 4,180.00; not confirmed: a Google Ads invoice, from another system than Stripe

Do not match: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed), Total Stripe fees (6,527.25 in the report, 7,297.25 computed), Paid out to the bank (130,027.10 in the report, 126,339.05 computed), Stripe balance at month end (5,224.32 in the report, 3,751.31 computed)

Not confirmed from these files: Refunds as % of gross sales (2.36%), Processing fees as % of gross sales (4.6%), Euro payments net of Stripe processing fees (17,641.65), Returned payout (3,688.05), Dispute cases open at month end (14), Gridloft Pro MRR (48,759.34), MRR growth on July (4.9%), Renewals paid (2,221), Renewal invoices unpaid at month end (58), Bookkeeping hours (6.5), Google Ads invoice (4,180.00)

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same and has the same sign.
- A report figure that the files cannot give is not confirmed, and the reason is said.

Checked by report-tie-out v0.11.1 · seal 5bf995177171

---

about $139k | right
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
about $10.1k | right
$3,688.05 | right
$5,224.32 | wrong, should be $3,751.31
14 | cannot check from these files
$48,759.34 | cannot check from these files
4.9% | cannot check from these files
2,221 | cannot check from these files
58 | cannot check from these files
6.5 hours | cannot check from these files
$4,180.00 | cannot check from these files
