I checked the report against your Stripe exports, figure by figure. Some numbers are right and some are wrong, and the wrong ones each come from counting something differently from your rules. In words:

- **Stripe fees:** the report leaves out the Billing and Tax fees, although its label says they are included.
- **Refund rate:** the report divides refunds by net sales, not by gross sales.
- **Euro payments:** the report's figure is the euro charges before fees, not after them.
- **Paid out:** the report counts the payout that failed on August 14 and was returned to your balance. Your rule leaves failed payouts out.
- **Month-end balance:** the report adds in the money Stripe holds in reserve.
- **Disputes withdrawn:** the report's figure is lower than your files show. Its net sales figure only works with the higher amount, so its table doesn't add up by its own numbers.

Stripe fees and paid out are the two lines I'm sure about. For the refund rate, euro total and balance, the report's number is exactly what that other way of counting gives, but I can't be sure that's how Ledgerline worked. For disputes, I can't tell what Ledgerline counted. It's worth asking them about each one.

Your August month-end from Stripe is saved as `files/stripe-month-end_2026-08.md`. It lists every item left out or open by its ID, such as the 17 test-mode payments and the failed payout. It also gives sales tax and the reserve, which the report doesn't show. The check below is also saved as `files/report-tieout_2026-08.md`.

# Ledgerline's August 2026 report, checked against your Stripe exports

- 6 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed); Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed); Refunds as % of gross sales (2.36% in the report, 2.30 computed); Payments in euros net of processing fees (17,641.65 in the report, 16,524.01 computed); Paid out to the bank (130,027.10 in the report, 126,339.05 computed); Stripe balance at month end (5,224.32 in the report, 3,751.31 computed).

8 of 21 figures match, 6 do not, and 7 cannot be confirmed from these files.

## Every figure

- Sales (about): the report says 139k, computed from your files 139,409.16: matches
- Gross sales: the report says 139,409.16, computed from your files 139,409.16: matches
- Refunds: the report says 3,204.12, computed from your files 3,204.12: matches
- Disputes (amounts withdrawn): the report says 265.14, computed from your files 289.21: does not match
- Disputes won back: the report says 53.45, computed from your files 53.45: matches
- Net sales after refunds and disputes: the report says 135,969.28, computed from your files 135,969.28: matches
- Total Stripe fees (processing, dispute and Billing/Tax usage fees): the report says 6,527.25, computed from your files 7,297.25: does not match
- Refunds as % of gross sales: the report says 2.36%, computed from your files 2.30: does not match
- Processing fees as % of gross sales: the report says 4.6%, computed from your files 4.60: matches
- Payments in euros net of processing fees: the report says 17,641.65, computed from your files 16,524.01: does not match
- Paid out to the bank: the report says 130,027.10, computed from your files 126,339.05: does not match
- Still in transit at month end (about): the report says 10.1k, computed from your files 10,085.69: matches
- Returned payout: the report says 3,688.05, computed from your files 3,688.05: matches
- Stripe balance at month end: the report says 5,224.32, computed from your files 3,751.31: does not match
- Dispute cases open at month end: the report says 14; not confirmed: The balance export records money moving for disputes, not a dispute's open or closed status or inquiries that hold no money; no disputes export was given.
- Gridloft Pro MRR at end of August: the report says 48,759.34; not confirmed: MRR is not in the owner's agreed month-end definitions (which plans, discounts, currencies, trials count), so there is no agreed figure to compare it with.
- MRR growth on July: the report says 4.9%; not confirmed: Depends on MRR, which has no agreed definition; July's MRR is not agreed either.
- Renewals paid in the month: the report says 2,221; not confirmed: What counts as a renewal (billing reason, plan, date paid vs created) is not in the agreed definitions.
- Renewal invoices unpaid at month end: the report says 58; not confirmed: What counts as a renewal invoice unpaid at month end is not in the agreed definitions, and the invoices export shows statuses as of October 4, not as of August 31.
- August Google Ads invoice: the report says 4,180.00; not confirmed: Google Ads spend is billed outside Stripe; none of these files hold it.
- Bookkeeping hours: the report says 6.5; not confirmed: Ledgerline's own time; not in any Stripe file.

Do not match: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed), Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed), Refunds as % of gross sales (2.36% in the report, 2.30 computed), Payments in euros net of processing fees (17,641.65 in the report, 16,524.01 computed), Paid out to the bank (130,027.10 in the report, 126,339.05 computed), Stripe balance at month end (5,224.32 in the report, 3,751.31 computed)

Cannot be confirmed from these files: Dispute cases open at month end (14), Gridloft Pro MRR at end of August (48,759.34), MRR growth on July (4.9%), Renewals paid in the month (2,221), Renewal invoices unpaid at month end (58), August Google Ads invoice (4,180.00), Bookkeeping hours (6.5)

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same and has the same sign.
- A report figure that the files cannot give is not confirmed, and the reason is said.

Checked by report-tie-out v0.10.1 · seal 358226869cdd

The check has only 21 of the report's figures: it wouldn't take "two" (disputes needing a response) because it's written as a word, so I added that line to the list below myself. The refund rate, processing-fee share, euro total and returned payout were worked out by a small extra script (`.tieout/extras.py`), which isn't part of your saved month-end calculation.

$139k | right
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
6.5 hours | cannot check from these files
