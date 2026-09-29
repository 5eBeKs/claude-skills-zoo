I ran September through the month-end calculation you pinned in July. There were no warnings and every control passed.

One input was missing: `files` has no `month_end_rates.csv`. I rebuilt it from the September and August rates written in your pinned definitions. If your actual rates differ, the MRR, revenue and deferred revenue figures will change, so please add the real file next month.

The full answer below is also saved as `saas-month-end_2026-09.md`, next to the `files` folder. It includes the list of open questions where I made a counting choice you haven't confirmed yet.

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
- The remaining definitions, the checks, what was counted again from the files and what each break of a copy did are in `saas-month-end_2026-09.md`, exactly as the calculation rendered them.

## Open questions

- When is a change of plan or quantity counted in the month's movement? Claude counted it this way: On the day the new price takes effect Is that how you count?
- The subscriptions export gives each subscription's status and quantity as of the export day. How is the month-end state found? Claude counted it this way: Rebuilt for the month's last day from start, trial, cancel and end dates and the invoices Is that how you count?
- How is tax charged on provider fees handled? Claude counted it this way: Tax on the fee counts as part of the fee Is that how you count?
- Does the provider give back its fee when a payment is refunded, and how is that shown? Claude counted it this way: As recorded in the export: if a refund has a negative fee, that fee was given back Is that how you count?
- How are disputes (chargebacks) shown? Claude counted it this way: Disputes are a separate line, not refunds Is that how you count?
- How are the period boundaries read? Claude counted it this way: Start included, end not included, by exact time Is that how you count?
- The rest of the open questions are in `saas-month-end_2026-09.md`.

## For the bookkeeper

Counted by the pinned calculation 3fa7bf12e9c2 ('saas-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

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
