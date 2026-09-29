I ran September through your saved `saas-month-end` calculation (pin 1). It raised no warnings and every check passed. One thing it needed was missing: your `month_end_rates.csv` wasn't in `files`. I rebuilt it from the June–September rates written in your own definitions and changed nothing else, so please put that file back in the folder next time. A copy of the answer below is saved as `files/saas-month-end_2026-09.md`.

In my earlier reply I had worked out one more figure myself: Stripe's balance summary shows more paid out than the bank-arrival total because one payout, created on 30 September, reached the bank on 1 October. Treat that as my own explanation, not as part of the checked answer.

---

# SaaS month-end for 2026-09

## MRR

MRR at the end of 2026-09: $220,394.85, from $197,582.35 at the end of 2026-08 (at 2026-08's rates).

Revalued at 2026-09's rates, last month end's MRR is $197,766.42; the exchange-rate change of $184.07 is not part of the movement.

| Movement (per customer, both month ends at 2026-09's rates) | Customers | MRR |
|---|---|---|
| New | 199 | $25,209.49 |
| Expansion | 99 | $3,912.30 |
| Reactivation | 4 | $520.74 |
| Contraction (subtracted) | 60 | $2,068.01 |
| Churned (subtracted) | 42 | $4,946.09 |
| Net new MRR | | $22,628.43 |

Reactivated customers: cus_2PxssiOv2Hcdqh, cus_CV5m7KxN7R7zaI, cus_Eaqmu6zTKOgx1J, cus_XD3EJVgCH9JmaK

Churned customers (42): cus_2VDeh3ijmzPPg7, cus_5iiEY4sGhS1rUy, cus_794LxnkHhZ41Zv, cus_DaehyjteTaTwX2, cus_G8GpgKWY5Oya7G, cus_HAuKLg7G8UJxO9, cus_Hy252UemMs5uJh, cus_Izl80nNXzI6SeL, cus_J9F93YWUhsXd4m, cus_OXXJI0kLsAciCX, cus_OkpwMyaGnN0inb, cus_PZYcLSHmcDTdWJ, cus_Pwlw5VLBcL0Vl4, cus_QX6ie2sXthxXnk, cus_SgvAYknmOlzHbA, cus_TxBr9dOrqSR5Xj, cus_X8lyWfYcpZ5AX3, cus_YFg4UkBKKwlV8k, cus_YN2wSgpt7cF8YQ, cus_YWU8G13hYHc4UK, cus_YXOfCoO5dg0F4q, cus_YjeIH06OWwjzvQ, cus_ZwrMwxlQftbunU, cus_aEZyqi7r0w8v2i, cus_arTjkOC3CADhDg, cus_b47C6nTr7dMRBL, cus_d8rLZWHFvtersV, cus_dsC3wsUWOGInw8, cus_gMRa13736wesh6, cus_kpnNIgXfsBG07k, cus_l7yqJbir8Xpy0f, cus_mompsRasqa8I4O, cus_mtf4u2rDGdQOsV, cus_nAaMg8Y58yHelK, cus_oJKIJDPg9aWm7Y, cus_qZfiQxciF3QOer, cus_rjTeGCw9pAKV0Y, cus_sHTsCccaUc9D9F, cus_tqshFmKDdVpTD8, cus_wMQrl6mmkxpVVe, cus_zZBwhNpUpNqqjF, cus_zf9uxVTzBlYWMk

## Customers

Paying customers at the end of 2026-09: 1,548 (at the end of 2026-08: 1,387). Customers lost: 42.

- Subscriptions unpaid at month end (Stripe stopped retrying; zero MRR): none
- Subscriptions whose collection was paused this month, still counted: none
- Subscriptions 100% off at month end (not paying): sub_1Iw7chN11bGju0S4cbZsXuBB, sub_1Ix7peN11bGju0S4P0DKvv0c, sub_1J2CWSN11bGju0S4KmhKCy5J, sub_1JAxBZN11bGju0S4bSkjgO6P, sub_1JBKRiN11bGju0S4iU1mPw9E, sub_1JCJtrN11bGju0S4lILLCVxI, sub_1JCs16N11bGju0S4Gdag8VEW, sub_1JGK8BN11bGju0S4iNKNPoCI, sub_1JIF4lN11bGju0S4gPtpFVrC, sub_1JQXmjN11bGju0S4tSUPPkVj, sub_1JRgggN11bGju0S4gXb4bgHj, sub_1JX4nlN11bGju0S4hMCLZC6o, sub_1JZZadN11bGju0S4vb7uMyPb, sub_1JcXSoN11bGju0S421WaMYlh, sub_1JcreiN11bGju0S4iWeM6PT6
- Customers deleted in Stripe, with old invoices only: cus_T2IbgAqUjrz5rZ, cus_bNSP72gQ58uMNC, cus_fRiKFZjQkd96jR

## Billed, collected, kept by Stripe, paid out

- Billings: $341,477.31 (invoices finalized in 2026-09, not void now, totals with tax). Enterprise invoices among them: in_1JVYVUN11bGju0S4u6nUrsD7, in_1JYULgN11bGju0S4COJcpK9y, in_1JaCUKN11bGju0S4K2jQas5F
- Invoices finalized in 2026-09 and void now, left out of billings: in_1JWFj3N11bGju0S4OWEFLn45, in_1JXS3DN11bGju0S47OVit1iW, in_1JXjwlN11bGju0S4hbCWkq0E, in_1JYXkLN11bGju0S46U2NZ2Hk, in_1JYyRYN11bGju0S4G2zKxkjR, in_1JYyr5N11bGju0S4i0FUkXwt, in_1JZEsFN11bGju0S48a2IU2DU, in_1JZHw2N11bGju0S4uE4zhmMs, in_1JaK7FN11bGju0S4AtAZaWFO, in_1JaMzNN11bGju0S4HcM7uO23, in_1JbGnEN11bGju0S4mau1SOcA, in_1JbJoeN11bGju0S4azgwjVYT, in_1Jdqf1N11bGju0S4DHi0WBi0, in_1JeDPxN11bGju0S4W89da8ur, in_1JeTeoN11bGju0S4oMiosnrN, in_1JeaQRN11bGju0S4xKJqZ1Um, in_1JfpuCN11bGju0S4kDRduxzP
- Uncollectible invoices, kept in billings: in_1JWTphN11bGju0S4gDwuO9Jt, in_1JWXfXN11bGju0S4iUapVUu1, in_1JXp9RN11bGju0S4ltjBFe0v
- Invoices settled from the customer's credit balance (billed, no cash): in_1JVUqLN11bGju0S4raWg3fPT, in_1JYHNkN11bGju0S4GMKWFK5V, in_1JZ8goN11bGju0S42bOTiam3, in_1JZXdXN11bGju0S4hSi16pIo, in_1Ja1QsN11bGju0S4qbOI4sRr, in_1Jb1v1N11bGju0S4qVhUutoF, in_1Jb4XSN11bGju0S4pZ97OP28, in_1JbgYzN11bGju0S4cTf4ADCV, in_1JbzoRN11bGju0S4d1PbDROA, in_1JcmAwN11bGju0S4DPC1WZ4s, in_1JdyvFN11bGju0S4PwhtKBUN, in_1Jdz9lN11bGju0S4dSvPdu8z, in_1JeaK7N11bGju0S41o3ehElm, in_1JewsGN11bGju0S4MmejiKZb, in_1JfsxIN11bGju0S49WtFCN12, in_1Jg97sN11bGju0S4CP1ECu84, in_1JgDh2N11bGju0S45qESO0Gf, in_1JgDh2N11bGju0S4KJt6RJNm
- Invoices paid outside Stripe this month (no cash): in_1Ifp18N11bGju0S4lOnaNDA9
- Cash collected: $330,573.95 from 1,363 successful payments, in settled US dollars. Test-mode payments left out: ch_3JadoNN11bGju0S43DFwiMpe, ch_3JfoUAN11bGju0S47bxbbYpj
- Refunds: $338.88. Refunds that failed and came back: $0.00 (none)
- Disputes, not in refunds or cash: $323.50 taken by chargebacks, $134.73 returned on disputes won.
- Stripe fees: $12,802.04, of which $10,186.15 on the month's transactions and $2,615.89 in Stripe's separate fee rows (Billing and Tax usage fees, dispute fees, less dispute fees refunded).
- Paid out to the bank: $277,424.98 (payouts arriving in 2026-09 by their arrival date). Failed payouts left out: none. Stripe's balance summary, which dates payouts in New York time, shows payouts of $349,930.72 for the month.

## Revenue

- Revenue recognised in 2026-09: $228,760.10
- Deferred revenue at the end of 2026-09: $593,812.15

## How this was counted

- A month is the calendar month in New York time: 2026-09 runs from 2026-09-01 04:00:00 to 2026-10-01 04:00:00 UTC.
- MRR at a month end: at its last second, every subscription that is active or past_due, at price x quantity per month (an annual price / 12), less repeating and forever coupons still running; trialing, unpaid, paused, incomplete and canceled count zero; one set to cancel at period end counts until it ends; one with collection paused still counts.
- Each subscription's price, quantity and coupon at the month end are rebuilt from its invoice lines (renewals and prorations, the date a change takes effect), not read from the export day's status.
- Unpaid: from the 5th failed attempt of an invoice (Stripe stops retrying) until the subscription ends or its latest invoice is paid; a subscription canceled at that attempt churns once.
- A repeating coupon runs its months from the subscription's start when it was on the first billed invoice, otherwise from the first period it discounted.
- Each customer's MRR is rounded to the cent in its currency, then converted at the month-end rate; movements are per customer with both month ends at this month's rates.
- Billings: invoices finalized in the month and not void now, at their total with tax.
- Cash collected: successful live payments created in the month, in settled US dollars; refunds are refunds created in the month; Stripe fees are the fee on every balance transaction of the month plus Stripe's separate fee rows.
- Paid out: payouts not failed whose arrival date (the bank date Stripe gives) is in the month.
- Revenue: invoice lines after discounts, without tax, spread by the second over their periods from finalization; credit notes as negative lines over the invoice's periods from their date.
- Is MRR counted after the customer's recurring discounts (coupons, promotion codes), or at the list price? After discounts that repeat (forever, or repeating while they last); a once-only discount does not change MRR (your answer)
- Does a subscription in its free trial count in MRR? No: a trial counts from its first paid invoice (your answer)
- Does a subscription on a 100%-off coupon or a free plan count in MRR and as a paying customer? No: it adds nothing to MRR and is not a paying customer (your answer)
- Does a past_due subscription (a failed renewal the provider is still retrying) count in MRR? Yes, until it is canceled or marked unpaid (your answer)
- Does a subscription set to cancel at the end of its period still count in MRR before that date? Yes, until the period ends (your answer)
- How does a plan billed every year (or quarter, or several months) count in MRR? Its recurring price divided by the months it covers (your answer)
- How do per-seat quantities and metered usage count in MRR? Seats at their quantity on the month's last day; metered usage kept out of MRR (your answer)
- Are setup fees, one-off invoice items and taxes kept out of MRR? Yes: MRR is the recurring price only, without tax (your answer)
- How is MRR in other currencies (EUR, GBP) counted in the reporting currency? Converted at one rate per currency on the month's last day (your answer)
- Is the month's MRR movement worked out per customer or per subscription? Per customer: all of a customer's subscriptions together (your answer)
- When a customer who had left comes back, is that reactivation or new MRR? Reactivation, however long they were gone (your answer)
- When is a change of plan or quantity counted in the month's movement? On the day the new price takes effect (Claude's reading, not yet confirmed by you)
- Who is a paying customer at a month's end? A customer with MRR above zero on the month's last day (per the MRR definitions above) (your answer)
- How are the month's churn rates measured? Not applicable here: no churn rate is published; the answer gives churned MRR and customers lost
- Which invoices are the month's billings? Invoices finalised in the month (your answer)
- Are billings stated with the tax on invoices, or without? With tax, as the customer paid (your answer)
- How do voided and uncollectible invoices count? Voided: out of billings. Uncollectible: in billings, and shown as written off (your answer)
- An invoice paid from the customer's credit balance: is that cash collected? No: billed, not collected; the credit balance falls (your answer)
- Is the month's revenue what was billed or collected, or what was earned over the service period? Earned: each invoice line spread over its service period, day by day (your answer)
- How is a proration (an upgrade's or downgrade's credit and charge) recognised? Over the period the proration line covers (your answer)
- Which month does a refund or credit note on a subscription invoice reduce? The month the refund or credit note is issued (your answer)
- How does a credit note count: against billings, or as a refund? Not applicable here: billings are invoice totals and are never reduced by a credit note; refunds are money returned; a credit note only lowers recognised revenue
- The subscriptions export gives each subscription's status and quantity as of the export day. How is the month-end state found? Rebuilt for the month's last day from start, trial, cancel and end dates and the invoices (Claude's reading, not yet confirmed by you)
- Which transaction categories count as customer payments (sales) in the report? Customer payments only: the charge category in the provider's report (the charge and payment types in the API) (your answer)
- How are delayed payments counted when they later fail (for example, a bank transfer or a direct debit)? A failed payment is removed from the period where it was created (your answer)
- What should be done with test mode rows or internal test payments if they end up in the export? Exclude rows marked as a test in the description or metadata (your answer)
- If the account is a platform, how are platform transactions (transfers to connected accounts, platform fees) counted? Not applicable here: the account is not a platform: no transfers or application fees in the exports
- Is the sales amount in the report gross (what the customer paid) or net (after the provider's fees)? Gross: what the customer paid, with fees as a separate line (your answer)
- Which fees count as "provider fees"? All provider fees: processing, disputes, conversion, services, tax on fees (your answer)
- How is tax charged on provider fees handled? Tax on the fee counts as part of the fee (Claude's reading, not yet confirmed by you)
- Does the provider give back its fee when a payment is refunded, and how is that shown? As recorded in the export: if a refund has a negative fee, that fee was given back (Claude's reading, not yet confirmed by you)
- Which period does a refund belong to: the period of the refund or the period of the original payment? The period when the refund was made (your answer)
- How are disputes (chargebacks) shown? Disputes are a separate line, not refunds (Claude's reading, not yet confirmed by you)
- Where does the dispute fee go? Into provider fees (your answer)
- How is the refund rate calculated? No refund rate is published (Claude's reading, not yet confirmed by you)
- How are refunds counted that did not reach the customer and came back to the balance? A separate adjustment, neither a sale nor a refund (your answer)
- Which date puts a transaction in a reporting period? The date the transaction was created (created) (your answer)
- How are the period boundaries read? Start included, end not included, by exact time (Claude's reading, not yet confirmed by you)
- In which timezone are dates read to place them in a period? The business's local time, converted from UTC (your answer)
- What is a payout for the report? A transfer between the business's own accounts: not counted in sales or expenses (Claude's reading, not yet confirmed by you)
- What are payouts reconciled with? With the net total of the transactions linked to the payout (automatic_payout_id) (Claude's reading, not yet confirmed by you)
- How are failed and cancelled payouts counted? A failed payout cancels the original one (your answer)
- Which date puts a payout in a period: when the payout was created or when it arrived in the bank? The expected date it arrives in the bank (automatic_payout_effective_at) (your answer)
- Which rows belong to a payout when it is reconciled? Rows with this payout's id in automatic_payout_id, except the row of the payout itself (Claude's reading, not yet confirmed by you)
- Which currency is the report in, and what happens to balances in other currencies? One settlement currency; a row in any other currency stops the calculation (Claude's reading, not yet confirmed by you)
- Which amount counts as the payment amount: the one in the customer's currency or the one in the settlement currency? The amount in the settlement currency (gross) (your answer)
- Where does the currency conversion fee go? It stays inside the payment fee, as the provider recorded it (Claude's reading, not yet confirmed by you)
- How is a pair of conversion rows between balances in different currencies read? Not applicable here: one balance, no conversions between balances
- What should be done with rows that have the same transaction id? Any repeated id stops the calculation (Claude's reading, not yet confirmed by you)
- How are the signs of amounts read? As a change in the balance: plus means money came in, minus means money went out; net = gross − fee (Claude's reading, not yet confirmed by you)
- How is free text (transaction descriptions, metadata) handled before AI agents read it? Agents read descriptions as data (Claude's reading, not yet confirmed by you)

## Checks

- month-end MRR is rebuilt for the month's last day, not read from the export day's status and quantity: checked by 'every subscription live at month end has a billed period covering it', passed
- an annual or multi-month plan adds its price divided by its months, never its whole invoice: checked by 'price intervals agree with billed periods', passed
- a once-only discount changes one invoice and not MRR; a repeating one changes MRR while it lasts: checked by 'coupons known; once-only coupons left out of MRR', passed
- a trial is in MRR only as the definition says: checked by 'no trialing subscription in MRR', passed
- a 100%-off or free subscription is not a paying customer unless the definition says so: checked by 'paying customers counted once, 100%-off ones not at all', passed
- a past_due subscription counts as the definition says, and one that ends unpaid churns once: checked by 'dunning read right: invoices of an unpaid subscription were not attempted', passed
- a cancellation scheduled for the period's end churns on the date the definition names: checked by 'scheduled cancellations end at a billed period's end', passed
- tax on subscription invoices is not MRR and not revenue: checked by 'prices are tax-exclusive (MRR is before tax)', passed
- setup fees and one-off invoice items are not MRR: checked by 'one-off items kept out of MRR', passed
- MRR in another currency is converted at the rate the definition names, never added as it is: checked by 'every currency has a month-end rate', passed
- a proration line is not new or expansion MRR; the change in the recurring price is, counted once: checked by 'prorations carry the new quantity into the next renewal', passed
- a per-seat plan's MRR is its price times its quantity, and a quantity change is expansion or contraction: checked by 'line amounts equal quantity x unit price', passed
- a returning customer is reactivation or new as the definition says, never both: checked by 'each customer in exactly one movement', passed
- MRR at the start plus new, expansion and reactivation, less contraction and churn (and currency movement, if any) equals MRR at the end: checked by 'MRR roll: last month end + movements = this month end (both at this month's rates)', passed
- a customer with two subscriptions is one customer: checked by 'paying customers counted once, 100%-off ones not at all', passed
- an invoice paid from the customer's credit balance brings no cash: checked by 'payments agree with Stripe's balance (settled US dollars)', passed
- a voided invoice and an uncollectible invoice count as the definition says, and differently: checked by 'invoices agree with their lines', passed
- deferred revenue at the start plus billings without tax, less revenue recognised and credits, equals deferred revenue at the end: checked by 'deferred revenue roll: start + billed without tax - credit notes - recognised = end (per currency)', passed
- a refund or credit note reduces the month the definition names, once: checked by 'credit notes agree with their refunds and with the invoices' amounts due', passed
- gross payment volume is not net of provider fees and the headline says which one it is: checked by 'balance rows: net = gross - fee', passed
- a payout is a transfer to the business's own bank account and is neither income nor expense: checked by 'balance roll: start + activity + payouts = end', passed
- the fee column is positive and is subtracted, so net equals gross minus fee on every row: checked by 'balance rows: net = gross - fee', passed
- a refund does not give back the fee of the payment it refunds unless the export records it: checked by 'balance rows: net = gross - fee', passed
- a transaction belongs to the period of the date the spec names and not to the period of another date column: checked by 'activity equals Stripe's balance summary', passed
- dates are read in the timezone the spec names before a transaction is put in a month: checked by 'New York dates agree with Stripe's own', passed
- a dispute costs the disputed amount and a dispute fee, and a won dispute returns only the amount: checked by 'activity equals Stripe's balance summary', passed
- disputes are counted in refunds only when the spec says so: checked by 'every balance category placed', passed
- a refund that failed and came back to the balance is not a new sale: checked by 'every balance category placed', passed
- a delayed payment that later failed is treated as the spec says and never counted twice: checked by 'payments agree with Stripe's balance (settled US dollars)', passed
- sales are selected by the category the spec names and every other category is accounted for: checked by 'every balance category placed', passed
- money passed on to connected sellers is not the platform's revenue: checked by 'every balance category placed', passed
- every payout equals the sum of the net of the transactions it paid out: checked by 'each payout equals its transactions', passed
- a failed or cancelled payout is netted against the payout it reverses: checked by 'failed payouts came back to the balance', passed
- amounts in different currencies are never added without a rate the spec names: checked by 'every currency has a month-end rate', passed
- the customer's currency amount and the settlement amount are different numbers: checked by 'payments agree with Stripe's balance (settled US dollars)', passed
- a currency conversion fee is shown where the spec puts it and not hidden in the rate: not applicable here: the exports carry no separate conversion fee; fees are taken as Stripe recorded them
- one transaction id is one row after deduplication: checked by 'recount: rows', passed
- amounts are read with the decimal separator the export declares: checked by 'recount: sums', passed
- amounts are in major currency units unless the export says cents: checked by 'prices agree with billed unit amounts', passed
- transaction descriptions are quarantined before any agent reads the export: not applicable here: the pinned calculation reads no description or free text; rows count by their status, category and type columns only
- the export covers the whole period with no missing days: checked by 'exports cover the whole month', passed

What was counted again from the files:

- month_end_rates.csv: all 8 rows are in exactly one of the calculation's 2 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- prices.csv: all 32 rows are in exactly one of the calculation's 2 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- prices.csv: the groups' 'Amount' add up to the file's own 'Amount' total (added up again)
- coupons.csv: all 10 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- promotion_codes.csv: all 9 rows are in exactly one of the calculation's 1 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- disputes.csv: all 13 rows are in exactly one of the calculation's 4 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- disputes.csv: the groups' 'Amount' add up to the file's own 'Amount' total (added up again)
- subscriptions.csv: all 2,703 rows are in exactly one of the calculation's 6 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- subscriptions.csv: the groups' 'Amount' add up to the file's own 'Amount' total (added up again)
- customers.csv: all 2,338 rows are in exactly one of the calculation's 2 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- customers.csv: the groups' 'Balance' add up to the file's own 'Balance' total (added up again)
- invoices.csv: all 8,728 rows are in exactly one of the calculation's 4 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- invoices.csv: the groups' 'Subtotal' add up to the file's own 'Subtotal' total (added up again)
- invoices.csv: the groups' 'Total' add up to the file's own 'Total' total (added up again)
- invoice_line_items.csv: all 11,258 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- invoice_line_items.csv: the groups' 'Amount' add up to the file's own 'Amount' total (added up again)
- invoice_line_items.csv: the groups' 'Discount Amount' add up to the file's own 'Discount Amount' total (added up again)
- invoice_line_items.csv: the groups' 'Tax Amount' add up to the file's own 'Tax Amount' total (added up again)
- credit_notes.csv: all 56 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- credit_notes.csv: the groups' 'Subtotal' add up to the file's own 'Subtotal' total (added up again)
- credit_notes.csv: the groups' 'Total' add up to the file's own 'Total' total (added up again)
- balance_change_from_activity_itemized.csv: all 7,036 rows are in exactly one of the calculation's 11 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- balance_change_from_activity_itemized.csv: the groups' 'fee' add up to the file's own 'fee' total (added up again)
- balance_change_from_activity_itemized.csv: the groups' 'gross' add up to the file's own 'gross' total (added up again)
- balance_change_from_activity_itemized.csv: the groups' 'net' add up to the file's own 'net' total (added up again)
- payments.csv: all 7,744 rows are in exactly one of the calculation's 4 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- payments.csv: the groups' 'Amount' add up to the file's own 'Amount' total (added up again)
- payments.csv: the groups' 'Converted Amount' add up to the file's own 'Converted Amount' total (added up again)
- payments.csv: the groups' 'Fee' add up to the file's own 'Fee' total (added up again)
- payouts.csv: all 119 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- payouts.csv: the groups' 'Amount' add up to the file's own 'Amount' total (added up again)
- payouts_itemized.csv: all 120 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- payouts_itemized.csv: the groups' 'net' add up to the file's own 'net' total (added up again)
- balance_summary_2026-07.csv: all 4 rows are in exactly one of the calculation's 1 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- balance_summary_2026-07.csv: the groups' 'net_amount' add up to the file's own 'net_amount' total (added up again)
- balance_summary_2026-08.csv: all 4 rows are in exactly one of the calculation's 1 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- balance_summary_2026-08.csv: the groups' 'net_amount' add up to the file's own 'net_amount' total (added up again)
- balance_summary_2026-09.csv: all 4 rows are in exactly one of the calculation's 1 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- balance_summary_2026-09.csv: the groups' 'net_amount' add up to the file's own 'net_amount' total (added up again)

What each break of a copy of the files did:

- rows exported twice (every 50th) in balance_change_from_activity_itemized.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in balance_change_from_activity_itemized.csv: caught (warned: Control failed: credit notes agree with their refunds and with the invoices' amounts due: 13 refunded credit note(s) that differ from their refund in the balanc)
- amounts in cents (x100) in balance_change_from_activity_itemized.csv: caught (warned: Control failed: payments agree with Stripe's balance (settled US dollars): payments export 237990.42 vs balance charges 23799042.00; 0 charge(s) in one and not )
- amounts with a decimal comma in balance_change_from_activity_itemized.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in balance_change_from_activity_itemized.csv: caught (warned: Control failed: credit notes agree with their refunds and with the invoices' amounts due: 41 refunded credit note(s) that differ from their refund in the balanc)
- a kind of row the calculation never saw (every 50th row) in balance_change_from_activity_itemized.csv: caught (warned: New in balance_change_from_activity_itemized.csv, column 'reporting_category': 'zz_new_kind' on 141 row(s). The calculation was pinned without it; check how it )
- amounts a cent off (every 50th row) in balance_change_from_activity_itemized.csv: caught (warned: Control failed: balance rows: net = gross - fee: 141 row(s): txn_3IQvtTN11bGju0S41POQ7S3n, txn_3IT2fMN11bGju0S41sTLijfN, txn_3IUIGcN11bGju0S49Vtr7K2x, txn_3IVdn)
- rows exported twice (every 50th) in balance_summary_2026-07.csv: no effect (the figures stay the same)
- amounts in cents (x100) in balance_summary_2026-07.csv: caught (warned: Control failed: activity equals Stripe's balance summary: balance rows of the month add up to 225345.56, the summary says 22534556.00)
- amounts with a decimal comma in balance_summary_2026-07.csv: caught (the answer stops: calc.py stopped (exit 2):)
- a kind of row the calculation never saw (every 50th row) in balance_summary_2026-07.csv: caught (warned: New in balance_summary_2026-07.csv, column 'category': 'zz_new_kind' on 1 row(s). The calculation was pinned without it; check how it counts before using these )
- amounts a cent off (every 50th row) in balance_summary_2026-07.csv: caught (warned: Control failed: balance roll: start + activity + payouts = end: summary payouts -218954.63 vs payouts in New York time -218954.63)
- rows exported twice (every 50th) in coupons.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in coupons.csv: caught (warned: coupons.csv, column 'Redeem By (UTC)': date (YYYY-MM-DD), now empty on every row. Check the export before using these figures.)
- times written eight hours later (another time zone) in coupons.csv: no effect (the figures stay the same)
- a kind of row the calculation never saw (every 50th row) in coupons.csv: caught (warned: New in coupons.csv, column 'Duration': 'zz_new_kind' on 1 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- rows exported twice (every 50th) in credit_notes.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in credit_notes.csv: caught (warned: Control failed: credit notes agree with their refunds and with the invoices' amounts due: 0 refunded credit note(s) that differ from their refund in the balance)
- amounts in cents (x100) in credit_notes.csv: caught (warned: Control failed: credit notes agree with their refunds and with the invoices' amounts due: 56 refunded credit note(s) that differ from their refund in the balanc)
- amounts with a decimal comma in credit_notes.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in credit_notes.csv: caught (warned: Control failed: credit notes agree with their refunds and with the invoices' amounts due: 41 refunded credit note(s) that differ from their refund in the balanc)
- a kind of row the calculation never saw (every 50th row) in credit_notes.csv: caught (warned: New in credit_notes.csv, column 'Status': 'zz_new_kind' on 2 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in credit_notes.csv: caught (warned: Control failed: credit notes agree with their refunds and with the invoices' amounts due: 2 refunded credit note(s) that differ from their refund in the balance)
- rows exported twice (every 50th) in customers.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in customers.csv: caught (warned: Control failed: every subscription and customer is in its export: 0 subscription(s) billed but missing from the subscriptions export (); 149 customer(s) with a )
- amounts in cents (x100) in customers.csv: no effect (the figures stay the same)
- amounts with a decimal comma in customers.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in customers.csv: no effect (the figures stay the same)
- amounts a cent off (every 50th row) in customers.csv: no effect (the figures stay the same)
- rows exported twice (every 50th) in disputes.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in disputes.csv: no effect (the figures stay the same)
- amounts in cents (x100) in disputes.csv: no effect (the figures stay the same)
- amounts with a decimal comma in disputes.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in disputes.csv: no effect (the figures stay the same)
- a kind of row the calculation never saw (every 50th row) in disputes.csv: caught (warned: New in disputes.csv, column 'Status': 'zz_new_kind' on 1 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in disputes.csv: no effect (the figures stay the same)
- rows exported twice (every 50th) in invoice_line_items.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in invoice_line_items.csv: caught (the answer stops: calc.py stopped (exit 1):)
- amounts in cents (x100) in invoice_line_items.csv: caught (warned: Control failed: invoices agree with their lines: 7261 invoice(s) whose lines do not add up to their subtotal, discount, tax and total (in_1Jh9jwN11bGju0S49a0D6u)
- amounts with a decimal comma in invoice_line_items.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in invoice_line_items.csv: caught (warned: Control failed: invoice dates agree with their lines' periods: 8229 renewal or signup invoice(s) dated apart from the period they bill: in_1Jh89ZN11bGju0S4vW6SH)
- a kind of row the calculation never saw (every 50th row) in invoice_line_items.csv: caught (warned: New in invoice_line_items.csv, column 'Type': 'zz_new_kind' on 226 row(s). The calculation was pinned without it; check how it counts before using these figures)
- amounts a cent off (every 50th row) in invoice_line_items.csv: caught (warned: Control failed: invoices agree with their lines: 226 invoice(s) whose lines do not add up to their subtotal, discount, tax and total (in_1Jh9jwN11bGju0S49a0D6uO)
- rows exported twice (every 50th) in invoices.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in invoices.csv: caught (the answer stops: calc.py stopped (exit 1):)
- amounts in cents (x100) in invoices.csv: caught (warned: Control failed: invoices agree with their lines: 7261 invoice(s) whose lines do not add up to their subtotal, discount, tax and total (in_1Jh9jwN11bGju0S49a0D6u)
- amounts with a decimal comma in invoices.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in invoices.csv: caught (warned: Control failed: invoice dates agree with their lines' periods: 8229 renewal or signup invoice(s) dated apart from the period they bill: in_1Jh89ZN11bGju0S4vW6SH)
- a kind of row the calculation never saw (every 50th row) in invoices.csv: caught (warned: New in invoices.csv, column 'Status': 'zz_new_kind' on 175 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in invoices.csv: caught (warned: Control failed: invoices agree with their lines: 175 invoice(s) whose lines do not add up to their subtotal, discount, tax and total (in_1Jh9jwN11bGju0S49a0D6uO)
- rows exported twice (every 50th) in payments.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in payments.csv: caught (warned: Control failed: payments agree with Stripe's balance (settled US dollars): payments export 212563.25 vs balance charges 237990.42; 108 charge(s) in one and not )
- amounts in cents (x100) in payments.csv: caught (warned: Control failed: payments agree with Stripe's balance (settled US dollars): payments export 23799042.00 vs balance charges 237990.42; 0 charge(s) in one and not )
- amounts with a decimal comma in payments.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in payments.csv: caught (warned: Control failed: payments agree with Stripe's balance (settled US dollars): payments export 236687.77 vs balance charges 237990.42; 211 charge(s) in one and not )
- a kind of row the calculation never saw (every 50th row) in payments.csv: caught (warned: New in payments.csv, column 'Status': 'zz_new_kind' on 155 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in payments.csv: caught (warned: Control failed: payments agree with Stripe's balance (settled US dollars): payments export 237990.42 vs balance charges 237990.42; 0 charge(s) in one and not th)
- rows exported twice (every 50th) in payouts.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in payouts.csv: caught (warned: Control failed: every payout Stripe itemized is in the payouts export: 17 payout(s) in the itemized payouts or balance export missing from the payouts export: p)
- amounts in cents (x100) in payouts.csv: caught (warned: Control failed: each payout equals its transactions: 119 payout(s) that differ from the itemized payouts export; 118 payout(s) that differ from the balance rows)
- amounts with a decimal comma in payouts.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in payouts.csv: caught (warned: Control failed: each payout equals its transactions: 119 payout(s) that differ from the itemized payouts export; 0 payout(s) that differ from the balance rows p)
- a kind of row the calculation never saw (every 50th row) in payouts.csv: caught (warned: New in payouts.csv, column 'Status': 'zz_new_kind' on 3 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in payouts.csv: caught (warned: Control failed: each payout equals its transactions: 3 payout(s) that differ from the itemized payouts export; 3 payout(s) that differ from the balance rows pai)
- rows exported twice (every 50th) in payouts_itemized.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in payouts_itemized.csv: caught (warned: Control failed: each payout equals its transactions: 16 payout(s) that differ from the itemized payouts export; 0 payout(s) that differ from the balance rows pa)
- amounts in cents (x100) in payouts_itemized.csv: caught (warned: Control failed: each payout equals its transactions: 119 payout(s) that differ from the itemized payouts export; 0 payout(s) that differ from the balance rows p)
- amounts with a decimal comma in payouts_itemized.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in payouts_itemized.csv: caught (warned: Control failed: each payout equals its transactions: 119 payout(s) that differ from the itemized payouts export; 0 payout(s) that differ from the balance rows p)
- a kind of row the calculation never saw (every 50th row) in payouts_itemized.csv: caught (warned: New in payouts_itemized.csv, column 'reporting_category': 'zz_new_kind' on 3 row(s). The calculation was pinned without it; check how it counts before using the)
- amounts a cent off (every 50th row) in payouts_itemized.csv: caught (warned: Control failed: each payout equals its transactions: 3 payout(s) that differ from the itemized payouts export; 0 payout(s) that differ from the balance rows pai)
- rows exported twice (every 50th) in prices.csv: caught (the answer stops: calc.py stopped (exit 2):)
- amounts in cents (x100) in prices.csv: caught (warned: Control failed: prices agree with billed unit amounts: 9735 subscription line(s) whose price is missing from the prices export or billed at another unit amount:)
- amounts with a decimal comma in prices.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in prices.csv: no effect (the figures stay the same)
- a kind of row the calculation never saw (every 50th row) in prices.csv: caught (warned: New in prices.csv, column 'Type': 'zz_new_kind' on 1 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in prices.csv: caught (warned: Control failed: prices agree with billed unit amounts: 245 subscription line(s) whose price is missing from the prices export or billed at another unit amount: )
- rows exported twice (every 50th) in promotion_codes.csv: no effect (the figures stay the same)
- the last three days of every month missing in promotion_codes.csv: caught (warned: promotion_codes.csv, column 'Expires At (UTC)': date (YYYY-MM-DD), now empty on every row. Check the export before using these figures.)
- times written eight hours later (another time zone) in promotion_codes.csv: no effect (the figures stay the same)
- rows exported twice (every 50th) in subscriptions.csv: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in subscriptions.csv: caught (warned: Control failed: every subscription and customer is in its export: 437 subscription(s) billed but missing from the subscriptions export (sub_1IREELN11bGju0S4fohk)
- amounts in cents (x100) in subscriptions.csv: no effect (the figures stay the same)
- amounts with a decimal comma in subscriptions.csv: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in subscriptions.csv: caught (warned: Control failed: subscription start dates agree with their signup invoices: 2335 subscription(s) whose start date is not their signup invoice's date: sub_1JguNON)
- a kind of row the calculation never saw (every 50th row) in subscriptions.csv: caught (warned: New in subscriptions.csv, column 'Status': 'zz_new_kind' on 55 row(s). The calculation was pinned without it; check how it counts before using these figures.)
- amounts a cent off (every 50th row) in subscriptions.csv: no effect (the figures stay the same)
- rows exported twice (every 50th) in month_end_rates.csv: caught (the answer stops: calc.py stopped (exit 2):)

## Open questions

- When is a change of plan or quantity counted in the month's movement? Claude counted it this way: On the day the new price takes effect Is that how you count?
- The subscriptions export gives each subscription's status and quantity as of the export day. How is the month-end state found? Claude counted it this way: Rebuilt for the month's last day from start, trial, cancel and end dates and the invoices Is that how you count?
- How is tax charged on provider fees handled? Claude counted it this way: Tax on the fee counts as part of the fee Is that how you count?
- Does the provider give back its fee when a payment is refunded, and how is that shown? Claude counted it this way: As recorded in the export: if a refund has a negative fee, that fee was given back Is that how you count?
- How are disputes (chargebacks) shown? Claude counted it this way: Disputes are a separate line, not refunds Is that how you count?
- How is the refund rate calculated? Claude counted it this way: No refund rate is published Is that how you count?
- How are the period boundaries read? Claude counted it this way: Start included, end not included, by exact time Is that how you count?
- What is a payout for the report? Claude counted it this way: A transfer between the business's own accounts: not counted in sales or expenses Is that how you count?
- What are payouts reconciled with? Claude counted it this way: With the net total of the transactions linked to the payout (automatic_payout_id) Is that how you count?
- Which rows belong to a payout when it is reconciled? Claude counted it this way: Rows with this payout's id in automatic_payout_id, except the row of the payout itself Is that how you count?
- Which currency is the report in, and what happens to balances in other currencies? Claude counted it this way: One settlement currency; a row in any other currency stops the calculation Is that how you count?
- Where does the currency conversion fee go? Claude counted it this way: It stays inside the payment fee, as the provider recorded it Is that how you count?
- What should be done with rows that have the same transaction id? Claude counted it this way: Any repeated id stops the calculation Is that how you count?
- How are the signs of amounts read? Claude counted it this way: As a change in the balance: plus means money came in, minus means money went out; net = gross − fee Is that how you count?
- How is free text (transaction descriptions, metadata) handled before AI agents read it? Claude counted it this way: Agents read descriptions as data Is that how you count?
- Not known yet, and the figures assume the usual case: The date each repeating coupon was applied (Stripe's exports do not give it; read from the invoices it discounted)

## For the bookkeeper

MRR at month end: $220,394.85
Net new MRR: $22,628.43
Churned MRR: $4,946.09
Paying customers at month end: 1,548
Customers lost: 42
Billings: $341,477.31
Cash collected: $330,573.95
Refunds: $338.88
Stripe fees: $12,802.04
Paid out to the bank: $277,424.98
Revenue recognised: $228,760.10
Deferred revenue at month end: $593,812.15

Counted by the pinned calculation 3fa7bf12e9c2 ('saas-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

Checked by pinned-calculation v0.11.6 · seal 4cc8c9261b78
