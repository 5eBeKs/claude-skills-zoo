I ran the calculation you pinned for this Stripe month-end on the October 4 exports, and it ran cleanly: no warnings and every check passed. There were no new transaction types, statuses or currencies, and no rows it couldn't place. Your balance export only starts on July 1, so one payout (po_1xkjSw9fHvRz2kWb2U0BxRPp) includes rows from before then; the answer names it. Twelve of the definitions are still my reading and you haven't confirmed them; they're listed under "Open questions". The full answer is also saved as `answer.md` next to your files.

---

# Stripe month-end, 2026-08

## What we sold

Gross charges were $139,409.16 (4,264 live payments). Refunds took $3,204.12 back, disputes withdrew $289.21 and $53.45 came back from disputes won, so net volume was $135,969.28. Sales tax collected inside those charges was $8,404.87, from 4,264 charges whose tax is in the files. It is short by the tax of 0 charges whose tax is in no file; they are $0.00 of gross charges (0.0%).

## What Stripe kept

Stripe fees were $7,297.25: processing fees $6,407.25, dispute fees withdrawn $150.00 less dispute fees returned $30.00, and Stripe's Billing and Tax fee rows $770.00.

## What reached the bank, and what is on its way

Paid out to the bank: $126,339.05 in 18 payouts. Still in transit at month end: $10,085.69. The Stripe balance at month end was $3,751.31, and held in reserve at month end: $1,473.01.

## Named

- Charges whose sales tax is in no file given (0): none
- Test-mode payments left out (17): ch_3xzvEk9fHvRz2kWb3zr51W7N, ch_3xzvFe9fHvRz2kWb3tqq2aBc, ch_3xzvK19fHvRz2kWb3qU33NU4, ch_3xzvPA9fHvRz2kWb2lPqdMWi, ch_3xzvSI9fHvRz2kWb1NyLLKxi, ch_3xzvTx9fHvRz2kWb1jMeM6yE, ch_3xzvYR9fHvRz2kWb0JYqLYYZ, ch_3xzvec9fHvRz2kWb0GN2p3xs, ch_3xzvj09fHvRz2kWb3UJt2FuY, ch_3xzvjW9fHvRz2kWb3lmxEfyk, ch_3xzvpx9fHvRz2kWb0hbFzN38, ch_3xzvv19fHvRz2kWb1wVnUBHs, ch_3xzw0C9fHvRz2kWb25gierd9, ch_3xzw1F9fHvRz2kWb2MhtmL6c, ch_3xzw3z9fHvRz2kWb3R5iPIqH, ch_3xzwAO9fHvRz2kWb12TfNIBc, ch_3xzwET9fHvRz2kWb0KiMpUB1
- Refunds that failed and came back (0): none
- Disputes withdrawn (10): du_1xwCzJ9fHvRz2kWb2FBNqBws, du_1xwizc9fHvRz2kWb23FxPT6B, du_1xx4989fHvRz2kWb04rtOTY1, du_1xzSVE9fHvRz2kWb2B7UdjsM, du_1y3bWc9fHvRz2kWb2U5L7fCR, du_1y43Ju9fHvRz2kWb3md2aFCa, du_1y4RZ09fHvRz2kWb0OHeXpUW, du_1y5daG9fHvRz2kWb14ZkJIn1, du_1y64wi9fHvRz2kWb1Y5nOQ3u, du_1y6s4E9fHvRz2kWb0UnxgMv1
- Disputes won back (2): du_1xlGr79fHvRz2kWb0OOzug92, du_1xq0eP9fHvRz2kWb2BbyZlaq
- Payments that failed later (0): none
- Stripe credits and adjustments, in no line (0): none
- Payouts that failed or were canceled (1): po_1y0KCu9fHvRz2kWb2JadhltI
- Payouts with a status not known (0): none
- Payouts in transit at month end (1): po_1y6qln9fHvRz2kWb1nwUqJzF
- Payouts carrying rows from before the balance export began (1): po_1xkjSw9fHvRz2kWb2U0BxRPp
- Balance rows not placed (0): none

## How this was counted

- A month is the UTC calendar month, by the time each balance transaction was created (from 00:00:00 on the 1st, up to but not including 00:00:00 on the next 1st).
- All amounts are US dollars as they moved the Stripe balance: the balance export's own gross, fee and net, so a charge is at its own exchange rate and a refund or dispute at the rate of its day.
- Gross charges: balance rows of category charge created in the month; a payment the payments export marks as test mode never counts.
- Refunds: refund rows created in the month (earlier months' payments included), less refund_failure rows (refunds that failed and came back) created in the month.
- Disputes withdrawn: the amount of dispute rows created in the month, without the $15 fee. Disputes won back: the amount of dispute_reversal rows created in the month.
- Net volume: gross charges less refunds, less disputes withdrawn, plus disputes won back.
- Sales tax collected: the Stripe Tax of each counted charge, from its invoice (subscriptions and invoices) or from the payment's tax_amount (orders), in the charge's currency, turned into dollars at that charge's own rate (its dollar gross over its customer amount) and rounded to the cent per charge; not reduced by refunds. A charge whose tax is in no file because the payments or invoices export starts after it (a payment before the payments export's first row; an invoice missing while the invoices export starts after the month began) adds no tax: the owner accepts the line is short by it, and those charges and their share of gross charges are named in every answer. A charge the exports do reach but whose tax is not found fails a check.
- Stripe fees: the fee column of the month's charges, plus dispute fees withdrawn less those returned, plus Stripe fee rows (Billing, Tax) created in the month. Credits Stripe gives back (a fee row with a positive amount, other_adjustment) are not netted: they are named apart.
- Paid out to the bank: payouts created in the month whose status is paid or in_transit (failed and canceled payouts are left out), whether they arrived that month or the next. Still in transit at month end: those of them whose arrival date is on or after the next month's 1st.
- Stripe balance at month end: available plus pending at 00:00 UTC on the next 1st, without reserve: the net of every balance row created before then that no payout created before then has paid out (reserve holds and releases included, so the reserve is not in it).
- Held in reserve at month end: rolling reserve withheld less released, by rows created before the next 1st (nothing was held before the export began: no release in it lacks its hold).
- Which transaction categories count as customer payments (sales) in the report? Customer payments only: the charge category in the provider's report (the charge and payment types in the API) (your answer)
- How are delayed payments counted when they later fail (for example, a bank transfer or a direct debit)? The payment stays in the period it was created in; its cancellation is subtracted in the period when it arrives (Claude's reading, not yet confirmed by you)
- What should be done with test mode rows or internal test payments if they end up in the export? Exclude rows marked as a test in the description or metadata (your answer)
- If the account is a platform, how are platform transactions (transfers to connected accounts, platform fees) counted? Not applicable here: Not a platform: no transfers or application fees in the balance; such a category would not be placed and the answer would say so.
- Is the sales amount in the report gross (what the customer paid) or net (after the provider's fees)? Gross: what the customer paid, with fees as a separate line (your answer)
- Which fees count as "provider fees"? All provider fees: processing, disputes, conversion, services, tax on fees (your answer)
- How is tax charged on provider fees handled? Tax on the fee counts as part of the fee (Claude's reading, not yet confirmed by you)
- Does the provider give back its fee when a payment is refunded, and how is that shown? The fee is not given back: a refund reduces the balance by the full amount (Claude's reading, not yet confirmed by you)
- Which period does a refund belong to: the period of the refund or the period of the original payment? The period when the refund was made (your answer)
- How are disputes (chargebacks) shown? Disputes are a separate line, not refunds (your answer)
- Where does the dispute fee go? Into provider fees (your answer)
- How is the refund rate calculated? No refund rate is published (Claude's reading, not yet confirmed by you)
- How are refunds counted that did not reach the customer and came back to the balance? It cancels the original refund: refunds go down (your answer)
- Which date puts a transaction in a reporting period? The date the transaction was created (created) (your answer)
- How are the period boundaries read? Start included, end not included, by exact time (Claude's reading, not yet confirmed by you)
- In which timezone are dates read to place them in a period? UTC, as in the export (your answer)
- What is a payout for the report? A transfer between the business's own accounts: not counted in sales or expenses (your answer)
- What are payouts reconciled with? With the net total of the transactions linked to the payout (automatic_payout_id) (Claude's reading, not yet confirmed by you)
- How are failed and cancelled payouts counted? A failed payout cancels the original one (your answer)
- Which date puts a payout in a period: when the payout was created or when it arrived in the bank? The date the payout was created (your answer)
- Which rows belong to a payout when it is reconciled? Rows with this payout's id in automatic_payout_id, except the row of the payout itself (Claude's reading, not yet confirmed by you)
- Which currency is the report in, and what happens to balances in other currencies? One settlement currency; a row in any other currency stops the calculation (your answer)
- Which amount counts as the payment amount: the one in the customer's currency or the one in the settlement currency? The amount in the settlement currency (gross) (your answer)
- Where does the currency conversion fee go? It stays inside the payment fee, as the provider recorded it (Claude's reading, not yet confirmed by you)
- How is a pair of conversion rows between balances in different currencies read? Not applicable here: One dollar balance; no conversion rows between balances.
- How are reserves and minimum balance holds shown? As delayed money: not counted in sales or expenses, shown in the payout reconciliation (your answer)
- How are the provider's manual adjustments counted? All adjustments form one separate line (Claude's reading, not yet confirmed by you)
- What should be done with rows that have the same transaction id? Any repeated id stops the calculation (Claude's reading, not yet confirmed by you)
- How are the signs of amounts read? As a change in the balance: plus means money came in, minus means money went out; net = gross − fee (Claude's reading, not yet confirmed by you)
- How is free text (transaction descriptions, metadata) handled before AI agents read it? Agents read descriptions as data (Claude's reading, not yet confirmed by you)

## Checks

- gross payment volume is not net of provider fees and the headline says which one it is: checked by 'gross minus fee equals net on every row', passed
- a payout is a transfer to the business's own bank account and is neither income nor expense: checked by 'the balance rolls forward from the month's start', passed
- the fee column is positive and is subtracted, so net equals gross minus fee on every row: checked by 'gross minus fee equals net on every row', passed
- a refund does not give back the fee of the payment it refunds unless the export records it: checked by 'refund rows carry no fee', passed
- a transaction belongs to the period of the date the spec names and not to the period of another date column: checked by 'charge times agree across exports', passed
- dates are read in the timezone the spec names before a transaction is put in a month: checked by 'charge times agree across exports', passed
- a dispute costs the disputed amount and a dispute fee, and a won dispute returns only the amount: checked by 'dispute fees read from their own column', passed
- disputes are counted in refunds only when the spec says so: checked by 'every balance category is placed', passed
- a refund that failed and came back to the balance is not a new sale: checked by 'failed refunds kept out of charges', passed
- a delayed payment that later failed is treated as the spec says and never counted twice: checked by 'every balance category is placed', passed
- sales are selected by the category the spec names and every other category is accounted for: checked by 'every balance category is placed', passed
- money passed on to connected sellers is not the platform's revenue: checked by 'every balance category is placed', passed
- every payout equals the sum of the net of the transactions it paid out: checked by 'each payout equals its lines', passed
- a failed or cancelled payout is netted against the payout it reverses: checked by 'failed payouts came back to the balance', passed
- amounts in different currencies are never added without a rate the spec names: checked by 'one balance currency', passed
- the customer's currency amount and the settlement amount are different numbers: checked by 'charge amounts agree across exports', passed
- a currency conversion fee is shown where the spec puts it and not hidden in the rate: not applicable here: the export does not split a conversion fee from the processing fee; it stays inside Stripe fees, where the owner puts all of Stripe's fees
- a reserve hold is money delayed and not money spent: checked by 'reserve held from holds in the export', passed
- every adjustment is placed in a line of the report or named as unplaced: checked by 'every balance category is placed', passed
- one transaction id is one row after deduplication: checked by 'no id appears twice', passed
- amounts are read with the decimal separator the export declares: checked by 'every amount reads as a number', passed
- amounts are in major currency units unless the export says cents: checked by 'charge amounts agree across exports', passed
- transaction descriptions are quarantined before any agent reads the export: not applicable here: no agent reads the exports when the pin runs; the calculation decides every row by category and status codes, never by a description
- the export covers the whole period with no missing days: checked by 'the export covers the whole month', passed

Counted again from the files:

- balance_transactions_itemized.csv: all 13,247 rows are in exactly one of the calculation's 9 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- balance_transactions_itemized.csv: the groups' 'fee' add up to the file's own 'fee' total (added up again)
- balance_transactions_itemized.csv: the groups' 'gross' add up to the file's own 'gross' total (added up again)
- balance_transactions_itemized.csv: the groups' 'net' add up to the file's own 'net' total (added up again)
- invoices.csv: all 8,625 rows are in exactly one of the calculation's 2 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- invoices.csv: the groups' 'Amount Paid' add up to the file's own 'Amount Paid' total (added up again)
- invoices.csv: the groups' 'Tax' add up to the file's own 'Tax' total (added up again)
- payouts.csv: all 65 rows are in exactly one of the calculation's 4 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- payouts.csv: the groups' 'Amount' add up to the file's own 'Amount' total (added up again)
- subscriptions.csv: all 3,617 rows are in exactly one of the calculation's 1 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- unified_payments.csv: all 13,967 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- unified_payments.csv: the groups' 'Amount' add up to the file's own 'Amount' total (added up again)
- unified_payments.csv: the groups' 'Converted Amount' add up to the file's own 'Converted Amount' total (added up again)

What each break of a copy of the files did:

- rows exported twice (every 50th) in balance_transactions_itemized.csv: caught (warned: Control failed: no id appears twice: balance: txn_1xpWUI9fHvRz2kWb3IRlC6P4, txn_1xrzA59fHvRz2kWb0l4yX0Iv, txn_1xt8vv9fHvRz2kWb17LG8sqO, txn_1xwhB09fHvRz2kWb2SpM)
- the last three days missing in balance_transactions_itemized.csv: no effect (the figures stay the same)
- amounts in cents (x100) in balance_transactions_itemized.csv: caught (warned: Control failed: charge amounts agree across exports: 12226 charges, e.g. ch_3xkUDB9fHvRz2kWb00XQPt2I, ch_3xkUX59fHvRz2kWb1KBTUGfz, ch_3xkV0t9fHvRz2kWb1v0u8thf)
- amounts with a decimal comma in balance_transactions_itemized.csv: caught (warned: balance_transactions_itemized.csv, column 'gross': number, now number with a decimal comma. The calculation may read it wrongly; check before using these figure)
- times written eight hours later (another time zone) in balance_transactions_itemized.csv: caught (warned: Control failed: charge times agree across exports: 12226 charges, e.g. ch_3xkUDB9fHvRz2kWb00XQPt2I, ch_3xkUX59fHvRz2kWb1KBTUGfz, ch_3xkV0t9fHvRz2kWb1v0u8thf)
- a kind of row the calculation never saw (every 50th row) in balance_transactions_itemized.csv: caught (warned: New in balance_transactions_itemized.csv, column 'reporting_category': 'zz_new_kind' on 265 row(s). The calculation was pinned without it; check how it counts b)
- amounts a cent off (every 50th row) in balance_transactions_itemized.csv: caught (warned: Control failed: gross minus fee equals net on every row: txn_3xkPHV9fHvRz2kWb3TzqfyHy, txn_3xkbEI9fHvRz2kWb15SAin0l, txn_3xkjQl9fHvRz2kWb1RN2jOW2, txn_3xkr409fH)
- rows exported twice (every 50th) in invoices.csv: caught (warned: Control failed: no id appears twice: invoices: in_1xkfSJ9fHvRz2kWb0jeIU2W2, in_1xksDf9fHvRz2kWb1wZqCPgt, in_1xl3w09fHvRz2kWb1YekMzEs, in_1xlIkN9fHvRz2kWb3aNQyJs)
- the last three days missing in invoices.csv: no effect (the figures stay the same)
- amounts in cents (x100) in invoices.csv: caught (warned: Control failed: sales tax found for every charge the payments and invoices exports reach: 2366 charges have no tax though the exports reach them: ch_3xkVBK9fHvR)
- amounts with a decimal comma in invoices.csv: caught (warned: invoices.csv, column 'Tax': number, now number with a decimal comma. The calculation may read it wrongly; check before using these figures.)
- times written eight hours later (another time zone) in invoices.csv: caught (warned: Sales tax collected is short by the tax of 43 charges of the month ($1,176.69 of gross charges): the payments export starts at 2026-07-01 05:17:29 UTC and the i)
- a kind of row the calculation never saw (every 50th row) in invoices.csv: caught (warned: New in invoices.csv, column 'Status': 'zz_new_kind' on 173 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in invoices.csv: caught (warned: Control failed: sales tax found for every charge the payments and invoices exports reach: 48 charges have no tax though the exports reach them: ch_3xkgON9fHvRz2)
- rows exported twice (every 50th) in payouts.csv: caught (warned: Control failed: no id appears twice: payouts: po_1xrzA59fHvRz2kWb2wOEa0LI, po_1yIRL99fHvRz2kWb0M99bczD)
- the last three days missing in payouts.csv: caught (warned: Control failed: payouts match their balance rows: po_1yIRL99fHvRz2kWb0M99bczD)
- amounts in cents (x100) in payouts.csv: caught (warned: Control failed: payouts match their balance rows: po_1xkjSw9fHvRz2kWb2U0BxRPp, po_1xl5fh9fHvRz2kWb208Bev2w, po_1xmXrD9fHvRz2kWb3GR2cwKS, po_1xmuXF9fHvRz2kWb2ftW)
- amounts with a decimal comma in payouts.csv: caught (warned: payouts.csv, column 'Amount': number, now number with a decimal comma. The calculation may read it wrongly; check before using these figures.)
- times written eight hours later (another time zone) in payouts.csv: no effect (the figures stay the same)
- a kind of row the calculation never saw (every 50th row) in payouts.csv: caught (warned: New in payouts.csv, column 'Status': 'zz_new_kind' on 2 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in payouts.csv: caught (warned: Control failed: payouts match their balance rows: po_1xrzA59fHvRz2kWb2wOEa0LI, po_1yIRL99fHvRz2kWb0M99bczD)
- rows exported twice (every 50th) in subscriptions.csv: no effect (the figures stay the same)
- the last three days missing in subscriptions.csv: no effect (the figures stay the same)
- times written eight hours later (another time zone) in subscriptions.csv: no effect (the figures stay the same)
- a kind of row the calculation never saw (every 50th row) in subscriptions.csv: caught (warned: New in subscriptions.csv, column 'Status': 'zz_new_kind' on 73 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- rows exported twice (every 50th) in unified_payments.csv: caught (warned: Control failed: no id appears twice: payments: ch_3xkccY9fHvRz2kWb0mxTTPT5, ch_3xkiwK9fHvRz2kWb3Kz5S2QN, ch_3xkqDq9fHvRz2kWb1IVLFLcM, ch_3xkzNI9fHvRz2kWb1o6Msie)
- the last three days missing in unified_payments.csv: no effect (the figures stay the same)
- amounts in cents (x100) in unified_payments.csv: caught (warned: Control failed: charge amounts agree across exports: 12226 charges, e.g. ch_3xkUDB9fHvRz2kWb00XQPt2I, ch_3xkUX59fHvRz2kWb1KBTUGfz, ch_3xkV0t9fHvRz2kWb1v0u8thf)
- amounts with a decimal comma in unified_payments.csv: caught (warned: unified_payments.csv, column 'Amount': number, now number with a decimal comma. The calculation may read it wrongly; check before using these figures.)
- times written eight hours later (another time zone) in unified_payments.csv: caught (warned: Control failed: charge times agree across exports: 12226 charges, e.g. ch_3xkUDB9fHvRz2kWb00XQPt2I, ch_3xkUX59fHvRz2kWb1KBTUGfz, ch_3xkV0t9fHvRz2kWb1v0u8thf)
- a kind of row the calculation never saw (every 50th row) in unified_payments.csv: caught (warned: New in unified_payments.csv, column 'Mode': 'zz_new_kind' on 280 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in unified_payments.csv: caught (warned: Control failed: charge amounts agree across exports: 247 charges, e.g. ch_3xkccY9fHvRz2kWb0mxTTPT5, ch_3xkqDq9fHvRz2kWb1IVLFLcM, ch_3xkzNI9fHvRz2kWb1o6MsieK)

## Open questions

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

## For the bookkeeper

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

Counted by the pinned calculation d8c663a3d3cd ('stripe-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

Checked by pinned-calculation v0.11.1 · seal 3d1f1e6427c4
