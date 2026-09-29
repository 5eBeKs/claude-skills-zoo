I ran the calculation you pinned in July (pin 1, `ee1f712540ac`) on the September files. It used the same code and definitions and found no problems: every check passed, no new kinds of line appeared, and no line was left out. The full answer, including every check and the open questions, is saved in `answer.md`.

**Please check one thing:** since the 2026-09-01 deposit, Amazon has been paying into bank account **x8841**. Before that it paid into **x4417**. This follows a failed deposit in August: settlement 26944784040 (21,849.95) never reached the bank, and Amazon added it back into the next payout, the 46,421.19 on Sept 1. Please confirm that x8841 is your account and that you meant to change it.

## What we sold (Pacific-time month, excluding tax)

| | USD |
|---|---:|
| Product sales | 112,613.64 |
| Shipping credits | 4,378.50 |
| Gift wrap credits | 99.80 |
| Promotional rebates | -2,864.74 |
| Refunds | -5,011.24 |
| **Net product sales** | **109,215.96** |

There were 3,005 orders placed in September. I left out 40 cancelled orders.

Amazon collected 7,995.89 of marketplace facilitator tax and paid all of it over itself, so it nets to 0.00 and isn't our money.

## What Amazon kept

| | USD |
|---|---:|
| Referral fees | -16,538.22 |
| FBA fulfilment fees | -19,193.09 |
| Storage fees | -736.75 |
| Other fees (including Buy Shipping labels -3,865.27 and shipping/gift wrap chargebacks -2,246.22) | -6,388.43 |
| **Amazon fees, total** | **-42,856.49** |
| Advertising | -11,886.85 |
| Reimbursements | 161.32 |

## What reached the bank and what Amazon still owes

**Deposited in September: 67,891.70**
- 2026-09-01: settlement 26985759971, 46,421.19
- 2026-09-17: settlement 27027934433, 21,470.51

**Owed by Amazon at month end: 55,376.53**
- **Settlement in transit, 27,448.43:** settlement 27066464770 closed on Sept 29 and was deposited on 2026-10-01.
- **Open settlement, 10,251.30:** lines Amazon had posted but not yet put into a settlement.
- **Held back for a later settlement, 17,676.80:** lines Amazon has already placed in settlement 27108188183.

**Reserve held at month end: 4,502.62.** This is the Current Reserve Amount of settlement 27066464770. It isn't part of the amount owed above.

**How the money moved:** Amazon held 73,136.91 for us on Sept 1, reserve included. September's lines added 54,633.94, the bank received 67,891.70, and Amazon held 59,879.15 at the end. These figures balance exactly.

The pin still has six readings I made that you haven't confirmed, for example that a repeated transaction id stops the calculation. None of them changed September's figures. They're listed under "Open questions" in `answer.md`.

For the bookkeeper (US dollars):

Product sales: 112,613.64 USD
Refunds: -5,011.24 USD
Net product sales: 109,215.96 USD
Amazon fees: -42,856.49 USD
Advertising: -11,886.85 USD
Reimbursements: 161.32 USD
Deposited to the bank: 67,891.70 USD
Owed by Amazon at month end: 55,376.53 USD
Reserve held at month end: 4,502.62 USD
Orders: 3,005
