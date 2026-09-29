I ran your pinned month-end calculation for August 2026. It gave no warnings and every check passed. The full answer is saved next to your exports as `files/saas-month-end_2026-08.md`, and the main sections are below exactly as the calculation wrote them.

The first run stopped because `month_end_rates.csv` isn't in `files`. I rebuilt it in my scratchpad from the August rates in your pinned definitions (EUR 1.172596, GBP 1.340131) and didn't change the calculation. Please put that file back in `files`, or send me the rates if those aren't the ones you want.

The calculation's text ("the owner" in its last line) is below:

# SaaS month-end for 2026-08

## MRR

MRR at the end of 2026-08: $197,582.35, from $176,027.01 at the end of 2026-07 (at 2026-07's rates).

Revalued at 2026-08's rates, last month end's MRR is $175,672.20; the exchange-rate change of $-354.80 is not part of the movement.

| Movement (per customer, both month ends at 2026-08's rates) | Customers | MRR |
|---|---|---|
| New | 199 | $23,428.79 |
| Expansion | 118 | $3,977.29 |
| Reactivation | 3 | $99.21 |
| Contraction (subtracted) | 49 | $1,802.46 |
| Churned (subtracted) | 40 | $3,792.68 |
| Net new MRR | | $21,910.15 |

Reactivated customers: cus_cjnDnDrKBtywr9, cus_l7yqJbir8Xpy0f, cus_mODtP9gImT1BmZ

Churned customers (40): cus_0ZcNUvPyNc1QZ4, cus_4Ai60xGfIinEsN, cus_52FXUSKgoSzFWW, cus_55N7TjtyG39c1B, cus_6TYFCDSZO5RqYk, cus_7Y6ywg2750Wfxa, cus_AUGGnfwq5cuShE, cus_BtrRU9jmdib0Ko, cus_C4ZzZIz0WBRNTL, cus_FH8ngEkzI6fE7N, cus_FPBxFJo5xOhwSZ, cus_Fa6kOfPHnEzrhp, cus_GSNJk0sTc5HhEi, cus_IamQ9184nudnfG, cus_Jm6Olq5IQYEmbR, cus_JvvGcuS4wy3q6t, cus_KgDoZgUExr99Ga, cus_L8YmgykA03s8cd, cus_MG49llcCRa4JGK, cus_MqkeMbF3TyP3l3, cus_TQc3L2MTDt6BAn, cus_UEJmFk3dbXcB5z, cus_WeDwykp3uusQ1q, cus_XTvTf5RBaOF9Mw, cus_XqRoPR8dT8I4ct, cus_Xt72ilUinOAMVK, cus_XuZmswUNWFd7eO, cus_XwubIqvRQTxoB7, cus_ZuCxw4cZ3GkobH, cus_aRVtNdkPaxDftb, cus_c2H2yE367n5Mkt, cus_hw9tgEwPpCDRru, cus_keMh3Px02r7FVP, cus_lClh0GKXcWChCf, cus_piZi4aHqWEsOUP, cus_rDvU9UTuizjQ9m, cus_rqCkITVKtyGh1x, cus_vWB4EaNON0VmC1, cus_yTTQV8pJcqdSFi, cus_yZOqZnP8rf7fKx

## Customers

Paying customers at the end of 2026-08: 1,387 (at the end of 2026-07: 1,225). Customers lost: 40.

- Subscriptions unpaid at month end (Stripe stopped retrying; zero MRR): sub_1IREb0N11bGju0S40nv7Evy2, sub_1IREmLN11bGju0S47tlgc4g7, sub_1IRF4UN11bGju0S4ZhzMRdJQ, sub_1IRFecN11bGju0S4RcD6BEwP, sub_1IRFndN11bGju0S40Fol2LoD, sub_1IRGKHN11bGju0S4INYtZgaK, sub_1IRGk3N11bGju0S4W6RKaXyq, sub_1IRH9LN11bGju0S4MFZbVooM, sub_1IRHBVN11bGju0S4htD1ckhG, sub_1IUGkeN11bGju0S4567ebKCN, sub_1IUXBLN11bGju0S4CVaFzrJh, sub_1IUaF8N11bGju0S4TuZyHqTw, sub_1IaRGVN11bGju0S4iMZcseM9, sub_1IfJ4RN11bGju0S4mW5cj09Y, sub_1IiaQvN11bGju0S4xsbEI1Yz, sub_1ImMzIN11bGju0S4HjK6eRAj
- Subscriptions whose collection was paused this month, still counted: sub_1IREgqN11bGju0S4PbfihIrS, sub_1IRG79N11bGju0S4vFC5m6qY, sub_1Ii278N11bGju0S4oqkrEfgL
- Subscriptions 100% off at month end (not paying): sub_1Iw7chN11bGju0S4cbZsXuBB, sub_1Ix7peN11bGju0S4P0DKvv0c, sub_1IzRzUN11bGju0S4vFl5mE3r, sub_1J2CWSN11bGju0S4KmhKCy5J, sub_1J3g4ZN11bGju0S4XJWV5yXP, sub_1J6x2zN11bGju0S4SfWHhxQZ, sub_1JAxBZN11bGju0S4bSkjgO6P, sub_1JBKRiN11bGju0S4iU1mPw9E, sub_1JCJtrN11bGju0S4lILLCVxI, sub_1JCs16N11bGju0S4Gdag8VEW, sub_1JGK8BN11bGju0S4iNKNPoCI, sub_1JIF4lN11bGju0S4gPtpFVrC, sub_1JM9PNN11bGju0S4t389oUS8, sub_1JQXmjN11bGju0S4tSUPPkVj
- Customers deleted in Stripe, with old invoices only: cus_T2IbgAqUjrz5rZ, cus_bNSP72gQ58uMNC, cus_fRiKFZjQkd96jR

## Billed, collected, kept by Stripe, paid out

- Billings: $294,271.41 (invoices finalized in 2026-08, not void now, totals with tax). Enterprise invoices among them: in_1JKJGSN11bGju0S4HMQYOgPV, in_1JL6CKN11bGju0S4gdhqiakP, in_1JOMFkN11bGju0S4eev8lDjg
- Invoices finalized in 2026-08 and void now, left out of billings: in_1JKSdGN11bGju0S4N3t2bSZc, in_1JL0x3N11bGju0S4TZaVXVPJ, in_1JL3ceN11bGju0S4gLSJPOwQ, in_1JMVAlN11bGju0S4IVrBU5au, in_1JNZLQN11bGju0S4kFcVRpQC, in_1JNjfYN11bGju0S4O9i0P0xj, in_1JNk55N11bGju0S4m9vKPpZc, in_1JNk5DN11bGju0S4iJmfBnkP, in_1JO06FN11bGju0S4tSyukLia, in_1JO3A2N11bGju0S4oBj2dQGc, in_1JP5LFN11bGju0S4w9or3dAT, in_1JP8DNN11bGju0S4kYdL432G, in_1JQ21EN11bGju0S4N3RrzhKr, in_1JQ52eN11bGju0S4AS8T5Irw, in_1JQ6ZQN11bGju0S4ueXubY5w, in_1JSbt1N11bGju0S4A8zzXIkw, in_1JSydxN11bGju0S4VKJFJEXm, in_1JT3HkN11bGju0S4eSnYCQP7, in_1JTEsoN11bGju0S4KTx5j0ay, in_1JTnKRN11bGju0S4LSRItiBt, in_1JUb8CN11bGju0S4YSOrk0qE, in_1JVLOaN11bGju0S4HWmPDPlH, in_1JVLOaN11bGju0S4bSpG2Jub, in_1JVLOaN11bGju0S4mIO13wgM
- Uncollectible invoices, kept in billings: in_1JKfMiN11bGju0S4Rh2D9tNF, in_1JPvrLN11bGju0S4hvwLtA9L, in_1JSIdUN11bGju0S4Dq2r1ZUl, in_1JT7CWN11bGju0S4MMrgmhDQ, in_1JTOzlN11bGju0S444gtrUzp, in_1JUWflN11bGju0S4zxgpaYL0, in_1JVLOaN11bGju0S4832B6QXN, in_1JVLOaN11bGju0S4Cp7vZJsg
- Invoices settled from the customer's credit balance (billed, no cash): in_1JM1l1N11bGju0S42m5IHqQv, in_1JMnZAN11bGju0S4pCrMP0Rr, in_1JMqJRN11bGju0S4pwVvsZpK, in_1JO4nRN11bGju0S4BDHfRAQB, in_1JOIrXN11bGju0S4EKou7g4x, in_1JOjZhN11bGju0S4GZK5nM6F, in_1JOmesN11bGju0S4dg0fbOjF, in_1JQArLN11bGju0S4wGx1GPGl, in_1JQRmzN11bGju0S4EbC2Ukob, in_1JQl2RN11bGju0S4Fg64iHaG, in_1JR0A4N11bGju0S4peNtOs9J, in_1JRKiFN11bGju0S4EryfXArL, in_1JRXOwN11bGju0S4gxbboqGu, in_1JRbxHN11bGju0S4V7gKBtmr, in_1JT4mON11bGju0S4dPhxe0Qr, in_1JUXWvN11bGju0S4YzviS92o, in_1JUbBWN11bGju0S4ujnPieA3, in_1JUuLsN11bGju0S4xCdmRrAc, in_1JVLOaN11bGju0S4WChiJ2vs, in_1JVLOaN11bGju0S4kqds2DhP
- Invoices paid outside Stripe this month (no cash): in_1JAuHIN11bGju0S4GQXzLy8E
- Cash collected: $263,648.17 from 1,239 successful payments, in settled US dollars. Test-mode payments left out: ch_3JLQ7sN11bGju0S480qKehLI, ch_3JTpwrN11bGju0S45GuC6L2k
- Refunds: $366.79. Refunds that failed and came back: $7.19 (re_3JHx52N11bGju0S40c86735C)
- Disputes, not in refunds or cash: $248.93 taken by chargebacks, $0.00 returned on disputes won.
- Stripe fees: $11,065.32, of which $8,972.47 on the month's transactions and $2,092.85 in Stripe's separate fee rows (Billing and Tax usage fees, dispute fees, less dispute fees refunded).
- Paid out to the bank: $195,967.18 (payouts arriving in 2026-08 by their arrival date). Failed payouts left out: none. Stripe's balance summary, which dates payouts in New York time, shows payouts of $195,967.18 for the month.

## Revenue

- Revenue recognised in 2026-08: $203,130.57
- Deferred revenue at the end of 2026-08: $497,047.01

---

The saved file also covers how each figure was counted, the checks run, and 15 open questions. Those are assumptions the calculation made where your definitions don't say, and they still need your OK. The main ones:
- A plan or quantity change counts on the day it takes effect.
- Each subscription's month-end state is rebuilt from its invoices.
- Disputes are shown separately, not as refunds.
- The tax Stripe charges on its fees counts as part of the fees.

## For the bookkeeper

MRR at month end: $197,582.35
Net new MRR: $21,910.15
Churned MRR: $3,792.68
Paying customers at month end: 1,387
Customers lost: 40
Billings: $294,271.41
Cash collected: $263,648.17
Refunds: $366.79
Stripe fees: $11,065.32
Paid out to the bank: $195,967.18
Revenue recognised: $203,130.57
Deferred revenue at month end: $497,047.01

Counted by the pinned calculation 3fa7bf12e9c2 ('saas-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.
