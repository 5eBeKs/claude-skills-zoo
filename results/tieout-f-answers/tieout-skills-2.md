Of the report's 22 figures, 8 are right, 8 are wrong and 6 can't be checked from your exports. Gross sales, refunds, disputes won back, net sales and the returned mid-August payout all match your files.

I ran the saved month-end calculation built on your definitions over all five exports; all its data checks passed. The ratios, euro payments and renewal counts aren't part of it, so I worked those out separately from the same files. Its full August answer, with the 17 test-mode payments it left out and the 10 disputes, is saved as `files/stripe-month-end_2026-08.md`. The check below is also saved, as `files/report-tieout_2026-08.md`.

**What the wrong figures differ by (from the files, not guesses about why):**
- **Stripe fees:** the gap equals August's Billing and Tax usage fee rows, which the report's own label says are included.
- **Paid out:** the gap equals the payout that failed on 14 August. Your rule leaves failed payouts out.
- **Balance at month end:** the report's figure is your balance plus the reserve. Your rule shows the reserve separately.
- **Disputes withdrawn:** the report's net sales is right, but only with the disputed amount from your files. With its own disputes figure, the table doesn't add up.
- **Euro payments:** the report's figure is the gross of the euro charges, before fees.
- **Renewals paid and unpaid renewal invoices:** your definitions don't cover these, so I chose how to count them. Renewals paid = August charges on invoices Stripe marks as regular subscription renewals. Unpaid = renewal invoices issued before 1 September that weren't paid or voided by then. Ask Ledgerline how they counted.

**Why six can't be checked:**
- Your exports show subscription and dispute statuses as of 4 October, so MRR, MRR growth and open disputes at 31 August can't be rebuilt.
- The hours and the Google Ads invoice aren't in Stripe data.
- The checking tool couldn't take "two" (disputes needing a response) because it's written as a word. It can't be checked either way, for the same reason as open disputes.

I'd ask Ledgerline which definitions they used for the eight wrong figures.

The check, exactly as the tool wrote it:

# Ledgerline's August 2026 summary, checked against your Stripe exports

- 8 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed); Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed); Refunds as a share of gross sales (2.36% in the report, 2.30 computed); Payments in euros net of Stripe's processing fees (17,641.65 in the report, 16,524.01 computed); Stripe paid out to your bank in August (130,027.10 in the report, 126,339.05 computed); The Stripe balance at month end (5,224.32 in the report, 3,751.31 computed); renewals paid during the month (2,221 in the report, 2,362.00 computed); renewal invoices still unpaid at month end (58 in the report, 41.00 computed).

8 of 21 figures match, 8 do not, and 5 cannot be confirmed from these files.

## Figure by figure

- Sales were up on July at about: the report says 139k, computed from your files 139,409.16: matches
- hours spent on the books: the report says 6.5; not confirmed: Ledgerline's own time; not in any Stripe export.
- Gross sales: the report says 139,409.16, computed from your files 139,409.16: matches
- Refunds: the report says 3,204.12, computed from your files 3,204.12: matches
- Disputes (amounts withdrawn): the report says 265.14, computed from your files 289.21: does not match
- Disputes won back: the report says 53.45, computed from your files 53.45: matches
- Net sales after refunds and disputes: the report says 135,969.28, computed from your files 135,969.28: matches
- Total Stripe fees (processing, dispute and Billing/Tax usage fees): the report says 6,527.25, computed from your files 7,297.25: does not match
- Refunds as a share of gross sales: the report says 2.36%, computed from your files 2.30: does not match
- Processing fees as a share of gross sales: the report says 4.6%, computed from your files 4.60: matches
- Payments in euros net of Stripe's processing fees: the report says 17,641.65, computed from your files 16,524.01: does not match
- Stripe paid out to your bank in August: the report says 130,027.10, computed from your files 126,339.05: does not match
- still in transit at month end: the report says 10.1k, computed from your files 10,085.69: matches
- The payout returned in mid-August: the report says 3,688.05, computed from your files 3,688.05: matches
- The Stripe balance at month end: the report says 5,224.32, computed from your files 3,751.31: does not match
- dispute cases still open at month end: the report says 14; not confirmed: The payments export shows each dispute's status on the export day (4 October), and a lost dispute carries no closing date, so which cases were open at 31 August cannot be rebuilt.
- Gridloft Pro MRR at the close of August: the report says 48,759.34; not confirmed: The subscriptions export is the state on 4 October (current plans, amounts and statuses, in several currencies); MRR at 31 August cannot be rebuilt from it without guessing past plan changes and exchange rates.
- MRR growth on July: the report says 4.9%; not confirmed: Needs MRR at the end of July and August, which these exports (state on 4 October) cannot give.
- renewals paid during the month: the report says 2,221, computed from your files 2,362.00: does not match
- renewal invoices still unpaid at month end: the report says 58, computed from your files 41.00: does not match
- August Google Ads invoice: the report says 4,180.00; not confirmed: A Google Ads invoice; not in any Stripe export.

Do not match: Disputes (amounts withdrawn) (265.14 in the report, 289.21 computed), Total Stripe fees (processing, dispute and Billing/Tax usage fees) (6,527.25 in the report, 7,297.25 computed), Refunds as a share of gross sales (2.36% in the report, 2.30 computed), Payments in euros net of Stripe's processing fees (17,641.65 in the report, 16,524.01 computed), Stripe paid out to your bank in August (130,027.10 in the report, 126,339.05 computed), The Stripe balance at month end (5,224.32 in the report, 3,751.31 computed), renewals paid during the month (2,221 in the report, 2,362.00 computed), renewal invoices still unpaid at month end (58 in the report, 41.00 computed)

Cannot be confirmed from these files: hours spent on the books (6.5), dispute cases still open at month end (14), Gridloft Pro MRR at the close of August (48,759.34), MRR growth on July (4.9%), August Google Ads invoice (4,180.00)

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same and has the same sign.
- A report figure that the files cannot give is not confirmed, and the reason is said.

Checked by report-tie-out v0.11.1 · seal cca5d579571b

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
two | cannot check from these files
$48,759.34 | cannot check from these files
4.9% | cannot check from these files
2,221 | wrong, should be 2,362
58 | wrong, should be 41
$4,180.00 | cannot check from these files
