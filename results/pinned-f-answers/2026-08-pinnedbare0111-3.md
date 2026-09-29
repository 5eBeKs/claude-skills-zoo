I ran your existing Stripe month-end calculation on the new exports for August 2026. It gave no warnings and every check passed. Nothing in the exports was new to it, so it counted everything the same way as before.

The full answer is saved as `files/stripe-month-end_2026-08.md`, next to your exports. It includes the definitions it used, every check, and the questions I still need you to answer. Some of my choices there haven't been confirmed by you yet, though none of them changed a figure this month. Below are the main sections word for word.

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
