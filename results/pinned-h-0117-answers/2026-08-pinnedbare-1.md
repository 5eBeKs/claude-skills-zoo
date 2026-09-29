My earlier summary reworded the figures. The month-end check requires the verified text word for word, so here it is. The full answer is saved as `files/saas-month-end_2026-08.md`. That file also covers:

- how each figure was counted, and 9 judgement calls I made where your definitions don't say;
- 16 open questions for you to confirm;
- 40 checks, all passed;
- tests that damaged copies of your files to see what the calculation catches. One it misses: if the last days of `credit_notes.csv` were missing, revenue and refunds would change with no warning. This export runs to October 2, so August is complete.

I passed in the July and August exchange rates written in your pinned definitions. All amounts below are in US dollars.

# SaaS month-end 2026-08 (New York time, US dollars)

## MRR
- MRR at month end: 197,592.90 US dollars, at the month-end rates EUR 1.172596, GBP 1.340131
- MRR by customer currency, before conversion: EUR 28,768.14, GBP 10,979.41, USD 149,145.82
- MRR at last month end, as reported at last month's rates: 176,037.82; at this month's rates: 175,682.83; exchange-rate change: -354.99
- New MRR: 23,428.77 (199 customers; of it, customers migrated from legacy billing: 182.13)
- Expansion MRR: 3,977.25 (118 customers)
- Reactivation MRR: 99.21 (3 customers)
- Contraction MRR: 1,802.49 (49 customers)
- Churned MRR: 3,792.67
- Net new MRR: 21,910.07

## Customers
- Paying customers at month end: 1388 (at last month end: 1226)
- Customers lost: 40

## Billed and collected
- Billings: 294,271.41 on 1421 invoices (tax in it: 8,594.96; manual enterprise and one-off invoices: 52,368.00; invoices settled from a credit balance: 20)
- Billings by invoice currency, before conversion: EUR 30,880.09, GBP 9,240.73, USD 245,677.75
- Cash collected: 263,648.17 from 1239 successful payments (bank transfers in it: 20,742.00; failed attempts left out: 144)
- Refunds: 366.79 (10 refunds); failed refunds that came back, shown apart: 7.19
- Disputes, shown apart: taken back by card networks 248.93; won back 0.00

## What Stripe kept and what reached the bank
- Stripe fees: 11,065.32 (payment processing 8,927.47, Billing and Tax usage fees 2,062.85, dispute fees 75.00, other 0.00)
- Paid out to the bank: 195,967.18 in 13 payouts
- Stripe balance activity of the month (matches Stripe's balance summary): 251,974.32

## Revenue
- Revenue recognised: 203,130.57
- Deferred revenue at month end: 497,047.01

## Named for you
- Customers lost: cus_0ZcNUvPyNc1QZ4, cus_4Ai60xGfIinEsN, cus_52FXUSKgoSzFWW, cus_55N7TjtyG39c1B, cus_6TYFCDSZO5RqYk, cus_7Y6ywg2750Wfxa, cus_AUGGnfwq5cuShE, cus_BtrRU9jmdib0Ko, cus_C4ZzZIz0WBRNTL, cus_FH8ngEkzI6fE7N, cus_FPBxFJo5xOhwSZ, cus_Fa6kOfPHnEzrhp, cus_GSNJk0sTc5HhEi, cus_IamQ9184nudnfG, cus_Jm6Olq5IQYEmbR, cus_JvvGcuS4wy3q6t, cus_KgDoZgUExr99Ga, cus_L8YmgykA03s8cd, cus_MG49llcCRa4JGK, cus_MqkeMbF3TyP3l3, cus_TQc3L2MTDt6BAn, cus_UEJmFk3dbXcB5z, cus_WeDwykp3uusQ1q, cus_XTvTf5RBaOF9Mw, cus_XqRoPR8dT8I4ct, cus_Xt72ilUinOAMVK, cus_XuZmswUNWFd7eO, cus_XwubIqvRQTxoB7, cus_ZuCxw4cZ3GkobH, cus_aRVtNdkPaxDftb, cus_c2H2yE367n5Mkt, cus_hw9tgEwPpCDRru, cus_keMh3Px02r7FVP, cus_lClh0GKXcWChCf, cus_piZi4aHqWEsOUP, cus_rDvU9UTuizjQ9m, cus_rqCkITVKtyGh1x, cus_vWB4EaNON0VmC1, cus_yTTQV8pJcqdSFi, cus_yZOqZnP8rf7fKx
- Customers churned: cus_0ZcNUvPyNc1QZ4, cus_4Ai60xGfIinEsN, cus_52FXUSKgoSzFWW, cus_55N7TjtyG39c1B, cus_6TYFCDSZO5RqYk, cus_7Y6ywg2750Wfxa, cus_AUGGnfwq5cuShE, cus_BtrRU9jmdib0Ko, cus_C4ZzZIz0WBRNTL, cus_FH8ngEkzI6fE7N, cus_FPBxFJo5xOhwSZ, cus_Fa6kOfPHnEzrhp, cus_GSNJk0sTc5HhEi, cus_IamQ9184nudnfG, cus_Jm6Olq5IQYEmbR, cus_JvvGcuS4wy3q6t, cus_KgDoZgUExr99Ga, cus_L8YmgykA03s8cd, cus_MG49llcCRa4JGK, cus_MqkeMbF3TyP3l3, cus_TQc3L2MTDt6BAn, cus_UEJmFk3dbXcB5z, cus_WeDwykp3uusQ1q, cus_XTvTf5RBaOF9Mw, cus_XqRoPR8dT8I4ct, cus_Xt72ilUinOAMVK, cus_XuZmswUNWFd7eO, cus_XwubIqvRQTxoB7, cus_ZuCxw4cZ3GkobH, cus_aRVtNdkPaxDftb, cus_c2H2yE367n5Mkt, cus_hw9tgEwPpCDRru, cus_keMh3Px02r7FVP, cus_lClh0GKXcWChCf, cus_piZi4aHqWEsOUP, cus_rDvU9UTuizjQ9m, cus_rqCkITVKtyGh1x, cus_vWB4EaNON0VmC1, cus_yTTQV8pJcqdSFi, cus_yZOqZnP8rf7fKx
- New customers: 199 customers, all listed in `files/saas-month-end_2026-08.md`
- New customers migrated from legacy billing: cus_0fbQbonGfXVXrU, cus_76HDVJVaNlymfn, cus_7xHymFtW1tR0EB, cus_jbQrAtSsfcFiP9, cus_jxYK4J9PaFqqlW
- Reactivated customers: cus_cjnDnDrKBtywr9, cus_l7yqJbir8Xpy0f, cus_mODtP9gImT1BmZ
- Subscriptions unpaid at month end (zero MRR): sub_1IREb0N11bGju0S40nv7Evy2, sub_1IREmLN11bGju0S47tlgc4g7, sub_1IRF4UN11bGju0S4ZhzMRdJQ, sub_1IRFecN11bGju0S4RcD6BEwP, sub_1IRFndN11bGju0S40Fol2LoD, sub_1IRGKHN11bGju0S4INYtZgaK, sub_1IRH9LN11bGju0S4MFZbVooM, sub_1IRHBVN11bGju0S4htD1ckhG, sub_1IUGkeN11bGju0S4567ebKCN, sub_1IUXBLN11bGju0S4CVaFzrJh, sub_1IUaF8N11bGju0S4TuZyHqTw, sub_1IaRGVN11bGju0S4iMZcseM9, sub_1IfJ4RN11bGju0S4mW5cj09Y, sub_1IiaQvN11bGju0S4xsbEI1Yz, sub_1ImMzIN11bGju0S4HjK6eRAj
- Subscriptions free (100% off) at month end: sub_1Iw7chN11bGju0S4cbZsXuBB, sub_1Ix7peN11bGju0S4P0DKvv0c, sub_1IzRzUN11bGju0S4vFl5mE3r, sub_1J2CWSN11bGju0S4KmhKCy5J, sub_1J3g4ZN11bGju0S4XJWV5yXP, sub_1J6x2zN11bGju0S4SfWHhxQZ, sub_1JAxBZN11bGju0S4bSkjgO6P, sub_1JBKRiN11bGju0S4iU1mPw9E, sub_1JCJtrN11bGju0S4lILLCVxI, sub_1JCs16N11bGju0S4Gdag8VEW, sub_1JGK8BN11bGju0S4iNKNPoCI, sub_1JIF4lN11bGju0S4gPtpFVrC, sub_1JM9PNN11bGju0S4t389oUS8, sub_1JQXmjN11bGju0S4tSUPPkVj
- Subscriptions active with no recurring price found: none
- Subscriptions changed after their last invoice, before month end: none
- Subscriptions whose rebuilt status differs from the export: none
- Billed invoices now uncollectible (in billings and revenue): in_1JVLOaN11bGju0S4832B6QXN, in_1JVLOaN11bGju0S4Cp7vZJsg, in_1JUWflN11bGju0S4zxgpaYL0, in_1JTOzlN11bGju0S444gtrUzp, in_1JT7CWN11bGju0S4MMrgmhDQ, in_1JSIdUN11bGju0S4Dq2r1ZUl, in_1JPvrLN11bGju0S4hvwLtA9L, in_1JKfMiN11bGju0S4Rh2D9tNF
- Invoices finalized this month and void now (not billed): in_1JVLOaN11bGju0S4HWmPDPlH, in_1JVLOaN11bGju0S4bSpG2Jub, in_1JVLOaN11bGju0S4mIO13wgM, in_1JUb8CN11bGju0S4YSOrk0qE, in_1JTnKRN11bGju0S4LSRItiBt, in_1JTEsoN11bGju0S4KTx5j0ay, in_1JT3HkN11bGju0S4eSnYCQP7, in_1JSydxN11bGju0S4VKJFJEXm, in_1JSbt1N11bGju0S4A8zzXIkw, in_1JQ6ZQN11bGju0S4ueXubY5w, in_1JQ52eN11bGju0S4AS8T5Irw, in_1JQ21EN11bGju0S4N3RrzhKr, in_1JP8DNN11bGju0S4kYdL432G, in_1JP5LFN11bGju0S4w9or3dAT, in_1JO3A2N11bGju0S4oBj2dQGc, in_1JO06FN11bGju0S4tSyukLia, in_1JNk5DN11bGju0S4iJmfBnkP, in_1JNk55N11bGju0S4m9vKPpZc, in_1JNjfYN11bGju0S4O9i0P0xj, in_1JNZLQN11bGju0S4kFcVRpQC, in_1JMVAlN11bGju0S4IVrBU5au, in_1JL3ceN11bGju0S4gLSJPOwQ, in_1JL0x3N11bGju0S4TZaVXVPJ, in_1JKSdGN11bGju0S4N3t2bSZc
- Billed invoices paid outside Stripe (not cash): none
- Credit notes left out: none
- Failed payouts: none
- Failed refunds that came back: re_3JHx52N11bGju0S40c86735C
- Test-mode payments left out: ch_3JLQ7sN11bGju0S480qKehLI, ch_3JTpwrN11bGju0S45GuC6L2k
- Customers on subscriptions but not in the customers export: cus_T2IbgAqUjrz5rZ, cus_bNSP72gQ58uMNC, cus_fRiKFZjQkd96jR

Counted by the pinned calculation 8d7af2bb1bf4 ('saas-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

## For the bookkeeper (all amounts in US dollars)
MRR at month end: 197,592.90
Net new MRR: 21,910.07
Churned MRR: 3,792.67
Paying customers at month end: 1388
Customers lost: 40
Billings: 294,271.41
Cash collected: 263,648.17
Refunds: 366.79
Stripe fees: 11,065.32
Paid out to the bank: 195,967.18
Revenue recognised: 203,130.57
Deferred revenue at month end: 497,047.01
