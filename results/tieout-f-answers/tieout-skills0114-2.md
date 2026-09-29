The report is partly right: some of its figures match your Stripe exports, some don't, and some can't be checked from these files. The full comparison is below, exactly as the check produced it. I used the saved Stripe month-end calculation, which follows your definitions, and all its checks passed.

- **Wrong figures:** each gap lines up with one item in your files. The fee total leaves out Stripe's Billing and Tax fees. The payout total includes the payout that failed. The month-end balance includes the reserve. The euro figure is before Stripe's fees, not after.
- **Figures that can't be checked:** these files hold status as of October 4, not August 31, and some of these figures have no agreed definition (MRR, renewals). A few don't come from Stripe at all (Ledgerline's hours, the Google Ads invoice).

Four figures aren't part of the saved calculation, so I worked them out separately in the same way: the refund rate, the processing-fee rate, the euro payments and the failed payout.

I saved two files in `files`:
- `report-tieout_2026-08.md` is the comparison below.
- `stripe-month-end_2026-08.md` is the full August calculation. It includes the long lists of test payments, disputes and payouts that were left out or flagged.

# Ledgerline's August 2026 report checked against your Stripe exports

- 6 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) ($265.14 in the report, $289.21 computed); Total Stripe fees (processing, dispute and Billing/Tax usage fees) ($6,527.25 in the report, $7,297.25 computed); Refunds as a share of gross sales (2.36% in the report, 2.30% computed); Payments in euros, net of Stripe's processing fees ($17,641.65 in the report, $16,524.01 computed); Paid out to the bank in August ($130,027.10 in the report, $126,339.05 computed); Stripe balance at month end ($5,224.32 in the report, $3,751.31 computed).

8 of 22 figures match, 6 do not, and 8 cannot be confirmed from these files.

## Figure by figure

- Sales (about): the report says $139k, computed from your files $139,409.16: matches
- Hours spent on the books: the report says 6.5 hours; not confirmed: Ledgerline's own time; not in any Stripe export.
- Gross sales: the report says $139,409.16, computed from your files $139,409.16: matches
- Refunds: the report says $3,204.12, computed from your files $3,204.12: matches
- Disputes (amounts withdrawn): the report says $265.14, computed from your files $289.21: does not match
- Disputes won back: the report says $53.45, computed from your files $53.45: matches
- Net sales after refunds and disputes: the report says $135,969.28, computed from your files $135,969.28: matches
- Total Stripe fees (processing, dispute and Billing/Tax usage fees): the report says $6,527.25, computed from your files $7,297.25: does not match
- Refunds as a share of gross sales: the report says 2.36%, computed from your files 2.30%: does not match
- Processing fees as a share of gross sales: the report says 4.6%, computed from your files 4.60%: matches
- Payments in euros, net of Stripe's processing fees: the report says $17,641.65, computed from your files $16,524.01: does not match
- Paid out to the bank in August: the report says $130,027.10, computed from your files $126,339.05: does not match
- Still in transit at month end (about): the report says $10.1k, computed from your files $10,085.69: matches
- Payout returned (failed) in mid-August: the report says $3,688.05, computed from your files $3,688.05: matches
- Stripe balance at month end: the report says $5,224.32, computed from your files $3,751.31: does not match
- Dispute cases still open at month end: the report says 14; not confirmed: The exports were taken on October 4 and show each dispute's status as of then, not as of August 31; no agreed definition of an open case (inquiries included or not) either.
- Gridloft Pro MRR at end of August: the report says $48,759.34; not confirmed: MRR is not one of your agreed definitions (currency conversion, annual plans, past_due/trialing subscriptions), and subscriptions.csv is a snapshot from October 4, not August 31.
- MRR growth on July: the report says 4.9%; not confirmed: Depends on the August and July MRR, which these files cannot give on an agreed definition (see MRR).
- Renewals paid during August: the report says 2,221; not confirmed: Not in your agreed definitions. For reference, invoices.csv has 2,364 subscription_cycle invoices paid in August UTC (2,365 created in August and now paid); which definition Ledgerline used is unknown.
- Renewal invoices unpaid at month end: the report says 58; not confirmed: Invoice status in invoices.csv is as of October 4, not August 31; the August renewal invoices created then are now 2,365 paid and 45 void, and the month-end unpaid count depends on a definition not agreed.
- August Google Ads invoice: the report says $4,180.00; not confirmed: Google Ads is billed outside Stripe; no file here has it.
- two of them need a response from you: not confirmed: written in words; the check reads figures written in digits

Do not match: Disputes (amounts withdrawn) ($265.14 in the report, $289.21 computed), Total Stripe fees (processing, dispute and Billing/Tax usage fees) ($6,527.25 in the report, $7,297.25 computed), Refunds as a share of gross sales (2.36% in the report, 2.30% computed), Payments in euros, net of Stripe's processing fees ($17,641.65 in the report, $16,524.01 computed), Paid out to the bank in August ($130,027.10 in the report, $126,339.05 computed), Stripe balance at month end ($5,224.32 in the report, $3,751.31 computed)

Cannot be confirmed from these files: Hours spent on the books (6.5 hours), Dispute cases still open at month end (14), Gridloft Pro MRR at end of August ($48,759.34), MRR growth on July (4.9%), Renewals paid during August (2,221), Renewal invoices unpaid at month end (58), August Google Ads invoice ($4,180.00), two of them need a response from you

Set aside as not figures: # August 2026 month-end summary (the number of a heading or a list item), **Sent:** 4 September 2026 (a date or a time), | Stripe activity, August 2026 | USD | (the number of a heading or a list item), Stripe's deadlines fall in the first half of September (a date or a time)

## What the figures still depend on

- How are delayed payments counted when they later fail (for example, a bank transfer or a direct debit)? Claude counted it this way: The payment stays in the period it was created in; its cancellation is subtracted in the period when it arrives Is that how you count?
- How is tax charged on provider fees handled? Claude counted it this way: Tax on the fee counts as part of the fee Is that how you count?
- Does the provider give back its fee when a payment is refunded, and how is that shown? Claude counted it this way: The fee is not given back: a refund reduces the balance by the full amount Is that how you count?
- How is the refund rate calculated? Claude counted it this way: No refund rate is published Is that how you count?
- How are the period boundaries read? Claude counted it this way: Start included, end not included, by exact time Is that how you count?
- What are payouts reconciled with? Claude counted it this way: With the net total of the transactions linked to the payout (automatic_payout_id) Is that how you count?
- Which rows belong to a payout when it is reconciled? Claude counted it this way: Rows with this payout's id in automatic_payout_id, except the row of the payout itself Is that how you count?
- Where does the currency conversion fee go? Claude counted it this way: It stays inside the payment fee, as the provider recorded it Is that how you count?
- How are the provider's manual adjustments counted? Claude counted it this way: All adjustments form one separate line Is that how you count?
- What should be done with rows that have the same transaction id? Claude counted it this way: Any repeated id stops the calculation Is that how you count?
- How are the signs of amounts read? Claude counted it this way: As a change in the balance: plus means money came in, minus means money went out; net = gross − fee Is that how you count?
- How is free text (transaction descriptions, metadata) handled before AI agents read it? Claude counted it this way: Agents read descriptions as data Is that how you count?

## How this was checked

- A report figure matches when the figure computed from your files, rounded to the digits the report shows, is the same. A figure the report writes with a minus (or a plus) must also have that sign; one written without a sign, or in brackets, is compared by its size, since refunds and fees are often listed without their minus.
- A percentage in the report is compared with a figure kept as a percentage as it is, and with a share (0.0485) as that share times 100.
- A report figure that the files cannot give is not confirmed, and the reason is said; a figure written in words is not confirmed either, and what was set aside as not a figure (page numbers, dates, references) is listed.

## Closing lines

- $139k | right
- 6.5 hours | cannot check from these files (Ledgerline's own time; not in any Stripe export.)
- $139,409.16 | right
- $3,204.12 | right
- $265.14 | wrong, should be $289.21
- $53.45 | right
- $135,969.28 | right
- $6,527.25 | wrong, should be $7,297.25
- 2.36% | wrong, should be 2.30%
- 4.6% | right
- $17,641.65 | wrong, should be $16,524.01
- $130,027.10 | wrong, should be $126,339.05
- $10.1k | right
- $3,688.05 | right
- $5,224.32 | wrong, should be $3,751.31
- 14 | cannot check from these files (The exports were taken on October 4 and show each dispute's status as of then, not as of August 31; no agreed definition of an open case (inquiries included or not) either.)
- $48,759.34 | cannot check from these files (MRR is not one of your agreed definitions (currency conversion, annual plans, past_due/trialing subscriptions), and subscriptions.csv is a snapshot from October 4, not August 31.)
- 4.9% | cannot check from these files (Depends on the August and July MRR, which these files cannot give on an agreed definition (see MRR).)
- 2,221 | cannot check from these files (Not in your agreed definitions. For reference, invoices.csv has 2,364 subscription_cycle invoices paid in August UTC (2,365 created in August and now paid); which definition Ledgerline used is unknown.)
- 58 | cannot check from these files (Invoice status in invoices.csv is as of October 4, not August 31; the August renewal invoices created then are now 2,365 paid and 45 void, and the month-end unpaid count depends on a definition not agreed.)
- $4,180.00 | cannot check from these files (Google Ads is billed outside Stripe; no file here has it.)
- two of them need a response from you | cannot check (written in words; the check reads figures written in digits)

Checked by report-tie-out v0.11.4 · seal 58992c559cd7
