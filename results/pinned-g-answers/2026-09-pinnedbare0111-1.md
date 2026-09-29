I ran September through your saved Amazon month-end calculation (pin 1, set up in July), so the figures are counted the same way as July and August. No checks failed, and every line of the month was placed under one of your definitions.

- **Warnings at the top:** these are harmless. They're about `settlement_26988006297.txt`, a short settlement from 31 Aug to 1 Sep with no orders in it, so its shipment, quantity and promotion columns are empty. I checked the file itself.
- **Bank account changed:** from September, Amazon deposits go to account x8841 instead of x4417. If you didn't make that change, check it in Seller Central.
- **Six of my readings still need your OK:** none of them changes a September figure. They're listed under "Open questions" in the full answer.

The full answer, with how each figure was counted and every check, is saved as `files/amazon-month-end_2026-09.md`. Here is the main part exactly as the calculation produced it:

- settlement_26988006297.txt, column 'shipment-id': text, now empty on every row. The figures it feeds read as zero: check the export before using them.
- settlement_26988006297.txt, column 'quantity-purchased': number, now empty on every row. The figures it feeds read as zero: check the export before using them.
- settlement_26988006297.txt, column 'promotion-id': text, now empty on every row. The figures it feeds read as zero: check the export before using them.

# Amazon month-end, 2026-09 (US dollars)

## What we sold

| Sales | USD |
|---|---:|
| Product sales | 112,613.64 |
| Shipping credits | 4,378.50 |
| Gift wrap credits | 99.80 |
| Promotional rebates | -2,864.74 |
| Refunds | -5,011.24 |
| Net product sales | 109,215.96 |

| Refunds, by part | USD |
|---|---:|
| Principal refunded | -5,028.11 |
| Shipping refunded | -52.92 |
| Gift wrap refunded | -9.98 |
| Promotions that came back | 79.77 |

Orders purchased in the month: 3,005. Cancelled orders left out: 40.

## What Amazon kept

| Amazon fees | USD |
|---|---:|
| Referral fees | -16,538.22 |
| FBA fulfilment fees | -19,193.09 |
| Storage fees | -736.75 |
| Other fees | -6,388.43 |
| Amazon fees, total | -42,856.49 |

| Other fees, by kind | USD |
|---|---:|
| Shipping and gift wrap chargebacks | -2,246.22 |
| Subscription | -39.99 |
| Removal and disposal | -25.55 |
| Inbound placement | -189.00 |
| Coupon fees | -22.40 |
| Buy Shipping labels | -3,865.27 |

| Other lines | USD |
|---|---:|
| Advertising | -11,886.85 |
| Reimbursements | 161.32 |
| Lines no definition places, left out | 0.00 |

Marketplace facilitator tax, not our money: collected 7,995.89, paid over by Amazon -7,995.89, net 0.00.

Lines no definition places: none

## What reached the bank and what Amazon still owes

Deposited to the bank in the month: 67,891.70 in 2 deposit(s):
- 2026-09-01 settlement 26985759971 46,421.19
- 2026-09-17 settlement 27027934433 21,470.51

Owed by Amazon at month end: 55,376.53, made of:
- settlement 27066464770 closed, deposit in transit: 27,448.43
- settlement (not assigned yet) from the Date Range report: 10,251.30
- settlement 27108188183 from the Date Range report: 17,676.80
- reserve released into the open settlement: 4,502.62
- less the reserve held: -4,502.62

Reserve held at month end: 4,502.62, the Current Reserve Amount of settlement 27066464770.

Settlements closed before the month end that had not reached the bank by then:
- settlement 27066464770 (27,448.43): deposited 2026-10-01

How the money moved: Amazon held 73,136.91 for us at the start of the month, reserve included; the month's lines added 54,633.94; the bank received 67,891.70; Amazon held 59,879.15 at the end, reserve included.

Checks that failed: none

*(How this was counted, open questions, what pin.py counted again, and the broken-copy tests: see `files/amazon-month-end_2026-09.md`.)*

Counted by the pinned calculation ee1f712540ac ('amazon-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

Checked by pinned-calculation v0.11.1 · seal 29b3bbb6451b

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
