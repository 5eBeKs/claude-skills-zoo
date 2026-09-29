I checked the report figure by figure against your exports. **8 of its 21 numeric figures match, 8 are wrong and 5 can't be checked from these files.**

The core Stripe numbers come from your pinned month-end calculation, run on August with all its checks passing. For the figures that calculation doesn't cover (the refund rate, the processing-fee share, the euro payments, the returned payout and the two renewal counts), I wrote a small extra calculation. How it counts is set out below. The full result is saved as `files/tieout_2026-08.md`, and here it is as the check produced it:

---

# Ledgerline August 2026 report, figure by figure

- 8 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed); Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed); Refunds as a share of gross sales (2.36% in the report, 2.30 computed); Payments in euros, net of processing fees (17,641.65 in the report, 16,524.01 computed); Paid out to the bank (130,027.10 in the report, 126,339.05 computed); Stripe balance at month end (5,224.32 in the report, 3,751.31 computed); Renewals paid in the month (2,221 in the report, 2,364.00 computed); Renewal invoices unpaid at month end (58 in the report, 41.00 computed).

8 of 21 figures match, 8 do not, and 5 cannot be confirmed from these files.

- Sales (approximate): the report says 139k, computed from your files 139,409.16: matches
- Hours spent on the books: the report says 6.5; not confirmed: Ledgerline's own time sheet; not in any Stripe export.
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
- Still in transit at month end: the report says 10.1k, computed from your files 10,085.69: matches
- Returned payout: the report says 3,688.05, computed from your files 3,688.05: matches
- Stripe balance at month end: the report says 5,224.32, computed from your files 3,751.31: does not match
- Dispute cases open at month end: the report says 14; not confirmed: The exports were taken on October 4 and give each dispute's status as of then; they do not record when a dispute closed as lost or when an inquiry (which moves no money) opened or closed, so the cases open at 00:00 UTC on 1 September cannot be rebuilt.
- Gridloft Pro MRR at month end: the report says 48,759.34; not confirmed: The subscriptions export shows each subscription as of October 4 (current amount, plan and status); it has no history of price, quantity or status changes, and MRR's exchange rate for eur/gbp/cad subscriptions is not defined, so MRR at 31 August cannot be rebuilt.
- MRR change on July: the report says 4.9%; not confirmed: Needs MRR at end of July and end of August, which the October 4 subscriptions export cannot give (see MRR).
- Renewals paid in the month: the report says 2,221, computed from your files 2,364.00: does not match
- Renewal invoices unpaid at month end: the report says 58, computed from your files 41.00: does not match
- August Google Ads invoice: the report says 4,180.00; not confirmed: A Google Ads invoice; not in any Stripe export.

Do not match: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed), Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed), Refunds as a share of gross sales (2.36% in the report, 2.30 computed), Payments in euros, net of processing fees (17,641.65 in the report, 16,524.01 computed), Paid out to the bank (130,027.10 in the report, 126,339.05 computed), Stripe balance at month end (5,224.32 in the report, 3,751.31 computed), Renewals paid in the month (2,221 in the report, 2,364.00 computed), Renewal invoices unpaid at month end (58 in the report, 41.00 computed)

Cannot be confirmed from these files: Hours spent on the books (6.5), Dispute cases open at month end (14), Gridloft Pro MRR at month end (48,759.34), MRR change on July (4.9%), August Google Ads invoice (4,180.00)

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same and has the same sign.
- A report figure that the files cannot give is not confirmed, and the reason is said.

Checked by report-tie-out v0.11.1 · seal 3a278599064f

---

**What the files show about the gaps:**
- **Stripe fees:** our total adds Stripe's daily Billing and Tax usage fee rows. The report's label says it includes them, but its total is lower than ours.
- **Paid out:** we leave out the payout that failed in mid-August and came back, as your rules say. The report seems to count it.
- **Month-end balance:** we leave out the $1,473.01 held in reserve and show it separately. The report never shows the reserve.
- **Euro payments:** the report's figure is what the euro charges came to before Stripe's processing fees, not after them as it says.
- **Disputes withdrawn:** the report's net sales figure only adds up with our disputes amount, not with its own.
- **Renewal counts:** your standing definitions don't cover these, so I read them as:
  - **Paid:** renewal invoices marked paid in August.
  - **Unpaid at month end:** renewal invoices issued by 31 August and neither paid nor cancelled by then.
  
  Ask Ledgerline how they count these two.
- **"Two need a response":** this is written in words, so the check didn't count it as a figure. The October 4 exports can't show where the disputes stood at month end.

$139k | right
6.5 hours | cannot check from these files
$139,409.16 | right
$3,204.12 | right
$265.14 | wrong, should be $289.21
$53.45 | right
$135,969.28 | right
$6,527.25 | wrong, should be $7,297.25
2.36% | wrong, should be 2.30 percent
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
2,221 | wrong, should be 2,364
58 | wrong, should be 41
$4,180.00 | cannot check from these files
