My last message reworded some figures from the checked answer, so this replaces it. Below is the pinned calculation's September answer as the script printed it. I passed in the September and August month-end exchange rates from your definitions, because the calculation needs them as inputs.

The full answer, including every ID, every check and every open question waiting for your yes, is saved at `files/saas-month-end_2026-09.md`.

One thing to check: my system date is [run date], but you said the exports were taken on October 3. If they were actually taken before the month ended, the last days of September would be missing.

---

- 40 subscription(s) changed plan or quantity after their last invoice, which is before this month's end: the exports do not say when, so their month-end MRR is the invoiced one (named below)

# SaaS month-end 2026-09 (New York time, US dollars)

## MRR
- MRR at month end: 220,395.07 US dollars, at the month-end rates EUR 1.171889, GBP 1.358762
- MRR by customer currency, before conversion: EUR 29,395.70, GBP 11,706.60, USD 170,039.87
- MRR at last month end, as reported at last month's rates: 197,592.90; at this month's rates: 197,777.46; exchange-rate change: 184.56
- New MRR: 25,209.53 (199 customers; of it, customers migrated from legacy billing: 156.73)
- Expansion MRR: 3,912.32 (99 customers)
- Reactivation MRR: 520.74 (4 customers)
- Contraction MRR: 2,068.01 (60 customers)
- Churned MRR: 4,956.97
- Net new MRR: 22,617.61

## Customers
- Paying customers at month end: 1548 (at last month end: 1388)
- Customers lost: 43

## Billed and collected
- Billings: 341,477.31 on 1574 invoices (tax in it: 11,032.75; manual enterprise and one-off invoices: 79,968.24; invoices settled from a credit balance: 17)
- Billings by invoice currency, before conversion: EUR 37,150.43, GBP 30,238.81, USD 256,853.78
- Cash collected: 330,573.95 from 1363 successful payments (bank transfers in it: 65,480.04; failed attempts left out: 180)
- Refunds: 338.88 (10 refunds); failed refunds that came back, shown apart: 0.00
- Disputes, shown apart: taken back by card networks 323.50; won back 134.73

## What Stripe kept and what reached the bank
- Stripe fees: 12,802.04 (payment processing 10,126.15, Billing and Tax usage fees 2,600.89, dispute fees 75.00, other 0.00)
- Paid out to the bank: 349,930.72 in 5 payouts
- Stripe balance activity of the month (matches Stripe's balance summary): 317,244.26

## Revenue
- Revenue recognised: 228,760.10
- Deferred revenue at month end: 593,812.15

## Named for you
Long lists, all in full in `files/saas-month-end_2026-09.md`:
- Customers lost: 43
- Customers churned: 43
- New customers: 199
- Subscriptions changed after their last invoice, before month end: 40

Short lists:
- New customers migrated from legacy billing: cus_EHBYAWeJ88Njmi, cus_Xj1I3wCE1hqIlh, cus_twNMuCSBN4dU0S, cus_z2yz1va8AuDTCt
- Reactivated customers: cus_2PxssiOv2Hcdqh, cus_CV5m7KxN7R7zaI, cus_Eaqmu6zTKOgx1J, cus_XD3EJVgCH9JmaK
- Subscriptions unpaid at month end (zero MRR): none
- Subscriptions free (100% off) at month end: sub_1Iw7chN11bGju0S4cbZsXuBB, sub_1Ix7peN11bGju0S4P0DKvv0c, sub_1J2CWSN11bGju0S4KmhKCy5J, sub_1JAxBZN11bGju0S4bSkjgO6P, sub_1JBKRiN11bGju0S4iU1mPw9E, sub_1JCJtrN11bGju0S4lILLCVxI, sub_1JCs16N11bGju0S4Gdag8VEW, sub_1JGK8BN11bGju0S4iNKNPoCI, sub_1JIF4lN11bGju0S4gPtpFVrC, sub_1JQXmjN11bGju0S4tSUPPkVj, sub_1JRgggN11bGju0S4gXb4bgHj, sub_1JX4nlN11bGju0S4hMCLZC6o, sub_1JZZadN11bGju0S4vb7uMyPb, sub_1JcXSoN11bGju0S421WaMYlh, sub_1JcreiN11bGju0S4iWeM6PT6
- Subscriptions active with no recurring price found: none
- Subscriptions whose rebuilt status differs from the export: none
- Billed invoices now uncollectible (in billings and revenue): in_1JXp9RN11bGju0S4ltjBFe0v, in_1JWXfXN11bGju0S4iUapVUu1, in_1JWTphN11bGju0S4gDwuO9Jt
- Invoices finalized this month and void now (not billed): in_1JfpuCN11bGju0S4kDRduxzP, in_1JeaQRN11bGju0S4xKJqZ1Um, in_1JeTeoN11bGju0S4oMiosnrN, in_1JeDPxN11bGju0S4W89da8ur, in_1Jdqf1N11bGju0S4DHi0WBi0, in_1JbJoeN11bGju0S4azgwjVYT, in_1JbGnEN11bGju0S4mau1SOcA, in_1JaMzNN11bGju0S4HcM7uO23, in_1JaK7FN11bGju0S4AtAZaWFO, in_1JZHw2N11bGju0S4uE4zhmMs, in_1JZEsFN11bGju0S48a2IU2DU, in_1JYyr5N11bGju0S4i0FUkXwt, in_1JYyRYN11bGju0S4G2zKxkjR, in_1JYXkLN11bGju0S46U2NZ2Hk, in_1JXjwlN11bGju0S4hbCWkq0E, in_1JXS3DN11bGju0S47OVit1iW, in_1JWFj3N11bGju0S4OWEFLn45
- Billed invoices paid outside Stripe (not cash): none
- Credit notes left out: none
- Failed payouts: none
- Failed refunds that came back: none
- Test-mode payments left out: ch_3JadoNN11bGju0S43DFwiMpe, ch_3JfoUAN11bGju0S47bxbbYpj
- Customers on subscriptions but not in the customers export: cus_T2IbgAqUjrz5rZ, cus_bNSP72gQ58uMNC, cus_fRiKFZjQkd96jR

All checks passed. One test break was not caught: if the last three days were missing from `credit_notes.csv`, the figures would change with no warning.

## For the bookkeeper
MRR at month end: 220,395.07
Net new MRR: 22,617.61
Churned MRR: 4,956.97
Paying customers at month end: 1548
Customers lost: 43
Billings: 341,477.31
Cash collected: 330,573.95
Refunds: 338.88
Stripe fees: 12,802.04
Paid out to the bank: 349,930.72
Revenue recognised: 228,760.10
Deferred revenue at month end: 593,812.15

Counted by the pinned calculation 8d7af2bb1bf4 ('saas-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

Checked by pinned-calculation v0.11.7 · seal c9cd6a81f5b6
