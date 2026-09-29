I ran your saved Stripe month-end calculation on the August exports and checked each figure in Ledgerline's report against it. Six figures match, four are wrong, and twelve can't be checked from these files. The four wrong ones are disputes withdrawn, total Stripe fees, paid out to the bank and the month-end balance. What each difference lines up with in your exports, without guessing Ledgerline's reasons:

- **Paid out:** the report includes the mid-August payout that failed. Your definition leaves failed payouts out.
- **Month-end balance:** the report includes the money held in reserve. Your definition shows the reserve separately.
- **Stripe fees:** the gap equals Stripe's Billing and Tax fee rows, even though the report's label says those fees are included.
- **Disputes withdrawn:** the report's own table doesn't add up with its disputes figure. Its net sales figure agrees with the calculation's.

Ask Ledgerline which definitions they used for these four. The full check follows as the scripts produced it.

---

# Ledgerline's August 2026 summary, checked against your Stripe exports

- 4 figure(s) in the report do not match what your files give: Disputes (amounts withdrawn) ($265.14 in the report, $289.21 computed); Total Stripe fees (processing, dispute and Billing/Tax usage fees) ($6,527.25 in the report, $7,297.25 computed); Paid out to the bank ($130,027.10 in the report, $126,339.05 computed); Stripe balance at month end ($5,224.32 in the report, $3,751.31 computed).

6 of 22 figures match, 4 do not, and 12 cannot be confirmed from these files.

## Figure by figure

- Sales (rounded): the report says $139k, computed from your files $139,409.16: matches
- Hours spent on the books: the report says 6.5 hours; not confirmed: Ledgerline's own time; not in any Stripe export.
- Gross sales: the report says $139,409.16, computed from your files $139,409.16: matches
- Refunds: the report says $3,204.12, computed from your files $3,204.12: matches
- Disputes (amounts withdrawn): the report says $265.14, computed from your files $289.21: does not match
- Disputes won back: the report says $53.45, computed from your files $53.45: matches
- Net sales after refunds and disputes: the report says $135,969.28, computed from your files $135,969.28: matches
- Total Stripe fees (processing, dispute and Billing/Tax usage fees): the report says $6,527.25, computed from your files $7,297.25: does not match
- Refunds as a share of gross sales: the report says 2.36%; not confirmed: The pinned calculation publishes no refund rate; its refunds and gross charges would put it at about 2.30%, not 2.36%, but no pinned figure states a rate.
- Processing fees as a share of gross sales: the report says 4.6%; not confirmed: The pinned calculation publishes no processing-fee rate; its processing fees ($6,407.25) over gross charges come to about 4.60%, but no pinned figure states a rate.
- Euro payments net of processing fees: the report says $17,641.65; not confirmed: The pinned calculation does not split charges by the customer's currency.
- Paid out to the bank: the report says $130,027.10, computed from your files $126,339.05: does not match
- Still in transit at month end: the report says $10.1k, computed from your files $10,085.69: matches
- Returned payout: the report says $3,688.05; not confirmed: The pinned calculation names the failed payout (po_1y0KCu9fHvRz2kWb2JadhltI) but gives no amount for it.
- Stripe balance at month end: the report says $5,224.32, computed from your files $3,751.31: does not match
- Dispute cases open at month end: the report says 14; not confirmed: The pinned calculation counts dispute money moved in the month, not cases open at month end; the exports carry no dispute status list.
- Gridloft Pro MRR: the report says $48,759.34; not confirmed: MRR is not part of the pinned Stripe month-end calculation.
- MRR growth on July: the report says 4.9%; not confirmed: MRR is not part of the pinned calculation, and July's MRR is not computed.
- Renewals paid: the report says 2,221; not confirmed: Renewal counts are not part of the pinned calculation.
- Renewal invoices unpaid at month end: the report says 58; not confirmed: Unpaid renewal invoices are not part of the pinned calculation.
- August Google Ads invoice: the report says $4,180.00; not confirmed: Google Ads spend is from another system; not in the Stripe exports.
- two of them need a response from you: not confirmed: written in words; the check reads figures written in digits

Do not match: Disputes (amounts withdrawn) ($265.14 in the report, $289.21 computed), Total Stripe fees (processing, dispute and Billing/Tax usage fees) ($6,527.25 in the report, $7,297.25 computed), Paid out to the bank ($130,027.10 in the report, $126,339.05 computed), Stripe balance at month end ($5,224.32 in the report, $3,751.31 computed)

Cannot be confirmed from these files: Hours spent on the books (6.5 hours), Refunds as a share of gross sales (2.36%), Processing fees as a share of gross sales (4.6%), Euro payments net of processing fees ($17,641.65), Returned payout ($3,688.05), Dispute cases open at month end (14), Gridloft Pro MRR ($48,759.34), MRR growth on July (4.9%), Renewals paid (2,221), Renewal invoices unpaid at month end (58), August Google Ads invoice ($4,180.00), two of them need a response from you

Set aside as not figures: # August 2026 month-end summary (the number of a heading or a list item), **Sent:** 4 September 2026 (a date or a time), | Stripe activity, August 2026 | USD | (the number of a heading or a list item)

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
- 2.36% | cannot check from these files (The pinned calculation publishes no refund rate; its refunds and gross charges would put it at about 2.30%, not 2.36%, but no pinned figure states a rate.)
- 4.6% | cannot check from these files (The pinned calculation publishes no processing-fee rate; its processing fees ($6,407.25) over gross charges come to about 4.60%, but no pinned figure states a rate.)
- $17,641.65 | cannot check from these files (The pinned calculation does not split charges by the customer's currency.)
- $130,027.10 | wrong, should be $126,339.05
- $10.1k | right
- $3,688.05 | cannot check from these files (The pinned calculation names the failed payout (po_1y0KCu9fHvRz2kWb2JadhltI) but gives no amount for it.)
- $5,224.32 | wrong, should be $3,751.31
- 14 | cannot check from these files (The pinned calculation counts dispute money moved in the month, not cases open at month end; the exports carry no dispute status list.)
- $48,759.34 | cannot check from these files (MRR is not part of the pinned Stripe month-end calculation.)
- 4.9% | cannot check from these files (MRR is not part of the pinned calculation, and July's MRR is not computed.)
- 2,221 | cannot check from these files (Renewal counts are not part of the pinned calculation.)
- 58 | cannot check from these files (Unpaid renewal invoices are not part of the pinned calculation.)
- $4,180.00 | cannot check from these files (Google Ads spend is from another system; not in the Stripe exports.)
- two of them need a response from you | cannot check (written in words; the check reads figures written in digits)

Checked by report-tie-out v0.11.5 · seal be3b33c32837
