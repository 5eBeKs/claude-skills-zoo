I ran your saved Stripe month-end calculation (pin 1, `d8c663a3d3cd`) on the September 2026 exports. The rules for what counts are the ones you agreed on [run date], and nothing was worked out differently this time. All checks passed and there were no warnings: the exports have no new kinds of transactions, statuses or currencies, and every payout matches the transactions it paid out.

Below is the answer as the calculation produced it, minus two long sections: how each figure was counted, and every check and deliberately broken copy of the files. The full text is in `stripe-month-end_2026-09.md` next to the `files` folder.

# Stripe month-end, 2026-09

## What we sold

Gross charges were $135,375.92 (4,092 live payments). Refunds took $2,839.20 back, disputes withdrew $438.95 and $34.20 came back from disputes won, so net volume was $132,131.97. Sales tax collected inside those charges was $8,410.83, from 4,092 charges whose tax is in the files. It is short by the tax of 0 charges whose tax is in no file; they are $0.00 of gross charges (0.0%).

## What Stripe kept

Stripe fees were $7,175.00: processing fees $6,253.02, dispute fees withdrawn $195.00 less dispute fees returned $30.00, and Stripe's Billing and Tax fee rows $756.98.

## What reached the bank, and what is on its way

Paid out to the bank: $118,440.79 in 21 payouts. Still in transit at month end: $4,573.56. The Stripe balance at month end was $5,049.91, and held in reserve at month end: $6,702.10.

## Named

- Charges whose sales tax is in no file given (0): none
- Test-mode payments left out (12): ch_3yEmmZ9fHvRz2kWb2VJ6IsCp, ch_3yEmpf9fHvRz2kWb1omexxR2, ch_3yEmur9fHvRz2kWb3GUaTsag, ch_3yEmz89fHvRz2kWb02I99EjB, ch_3yEn4f9fHvRz2kWb07dJSx4J, ch_3yEn9c9fHvRz2kWb2qRvbz5m, ch_3yEnFf9fHvRz2kWb1G6IGMFX, ch_3yEnKl9fHvRz2kWb0yyAQCK9, ch_3yEnMu9fHvRz2kWb2H3wVlmC, ch_3yEnQW9fHvRz2kWb2im4hpiE, ch_3yEnTQ9fHvRz2kWb0kN9XkL5, ch_3yEnV69fHvRz2kWb2TcqQ8qC
- Refunds that failed and came back (1): re_3y5f5S9fHvRz2kWb3xUCGwwb
- Disputes withdrawn (13): du_1y75XC9fHvRz2kWb0CX7sqCo, du_1y7Bh49fHvRz2kWb3896IMBd, du_1y8blt9fHvRz2kWb3UAkJeGx, du_1y8tcB9fHvRz2kWb2WUJKFX7, du_1y9ZgG9fHvRz2kWb134wIcBH, du_1yAvSO9fHvRz2kWb1TYETFK6, du_1yBNYe9fHvRz2kWb110bulpN, du_1yBjQR9fHvRz2kWb2ciMJaoI, du_1yC7n49fHvRz2kWb0qVQk5g8, du_1yCmeQ9fHvRz2kWb27xBl1wY, du_1yDTSf9fHvRz2kWb0ieRD9Ix, du_1yEKaF9fHvRz2kWb2FcZWCBz, du_1yHF1p9fHvRz2kWb2ggpRAOC
- Disputes won back (2): du_1xmNyT9fHvRz2kWb0HBibtF5, du_1xuyHq9fHvRz2kWb1L2zqbA7
- Payments that failed later (0): none
- Stripe credits and adjustments, in no line (1): txn_1yA2jX9fHvRz2kWb1f8CouZX
- Payouts that failed or were canceled (0): none
- Payouts with a status not known (0): none
- Payouts in transit at month end (1): po_1yHj1a9fHvRz2kWb1GBVat3x
- Payouts carrying rows from before the balance export began (1): po_1xkjSw9fHvRz2kWb2U0BxRPp
- Balance rows not placed (0): none

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

Counted by the pinned calculation d8c663a3d3cd ('stripe-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

Checked by pinned-calculation v0.11.6 · seal 5fe3454a7375

## For the bookkeeper

Gross charges: $135,375.92
Refunds: $2,839.20
Disputes withdrawn: $438.95
Disputes won back: $34.20
Net volume: $132,131.97
Sales tax collected: $8,410.83
Stripe fees: $7,175.00
Paid out to the bank: $118,440.79
Still in transit at month end: $4,573.56
Stripe balance at month end: $5,049.91
Held in reserve at month end: $6,702.10
