My last reply retyped the figures in my own words, and the plugin's check flagged that it didn't match the checked answer. Below is the checked answer exactly as the calculation produced it. The full version, with every ID list, all the checks and the break tests, is saved next to your exports as `files/saas-month-end_2026-09.md`.

The calculation used the month-end exchange rates already in your definitions (September EUR 1.171889, GBP 1.358762; August EUR 1.172596, GBP 1.340131). All the checks passed. The one warning is below.

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
Short lists are shown in full here; the file has every ID in the long ones.
- Customers lost: 43 (in the file)
- Customers churned: 43 (in the file)
- New customers: 199 (in the file)
- New customers migrated from legacy billing: cus_EHBYAWeJ88Njmi, cus_Xj1I3wCE1hqIlh, cus_twNMuCSBN4dU0S, cus_z2yz1va8AuDTCt
- Reactivated customers: cus_2PxssiOv2Hcdqh, cus_CV5m7KxN7R7zaI, cus_Eaqmu6zTKOgx1J, cus_XD3EJVgCH9JmaK
- Subscriptions unpaid at month end (zero MRR): none
- Subscriptions free (100% off) at month end: 15 (in the file)
- Subscriptions active with no recurring price found: none
- Subscriptions changed after their last invoice, before month end: 40 (in the file)
- Subscriptions whose rebuilt status differs from the export: none
- Billed invoices now uncollectible (in billings and revenue): in_1JXp9RN11bGju0S4ltjBFe0v, in_1JWXfXN11bGju0S4iUapVUu1, in_1JWTphN11bGju0S4gDwuO9Jt
- Invoices finalized this month and void now (not billed): 17 (in the file)
- Billed invoices paid outside Stripe (not cash): none
- Credit notes left out: none
- Failed payouts: none
- Failed refunds that came back: none
- Test-mode payments left out: ch_3JadoNN11bGju0S43DFwiMpe, ch_3JfoUAN11bGju0S47bxbbYpj
- Customers on subscriptions but not in the customers export: cus_T2IbgAqUjrz5rZ, cus_bNSP72gQ58uMNC, cus_fRiKFZjQkd96jR

**Open questions** (the full wording is in the file): where your definitions don't settle a point, I made a choice. You haven't confirmed these yet. The main ones:
- A plan or quantity change counts from the day it takes effect.
- Credit notes don't reduce billings. Money they send back counts as refunds when it's created.
- Disputes are kept separate from refunds.
- Tax on Stripe fees counts as part of the fee.

Counted by the pinned calculation 8d7af2bb1bf4 ('saas-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

For the bookkeeper (all amounts in US dollars):
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
