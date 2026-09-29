I made two mistakes in my last reply: I typed one figure myself in my opening note, and I miscopied one line of the file checks. The full answer, exactly as the calculation produced it, is now saved at `files/amazon-month-end_2026-09.md`. It includes the 40 cancelled order ids, every check, and every test run on altered copies of your files.

All the checks passed. There is one warning and there are two open questions:

- **The warning is expected.** On October 6, when the reports were taken, the last September settlement was still open, so Amazon doesn't offer it as a download yet. Its September lines are counted in "owed" from the monthly transaction report instead.
- **Two open questions still need your yes:** how orders are counted, and which report each figure comes from.

Here are the main parts of the saved answer:

---

- No settlement file is open at the month end or later: lines posted at the month end may be missing from what is owed.

# Amazon month-end, 2026-09

**What we sold.** Product sales were 112,613.64. With shipping credits of 4,378.50, gift wrap credits of 99.80, promotional rebates of -2,864.74 and refunds of -5,011.24, net product sales were 109,215.96. Orders placed in the month: 3,005; 40 fully cancelled orders are left out.

**What Amazon kept.** Amazon fees were -42,856.49: referral fees -16,538.22, FBA fulfilment fees -19,193.09, storage fees -736.75 and other fees -6,388.43. Advertising was -11,886.85. Reimbursements paid to us were 161.32.

Storage fees counted this month, as they posted: FBA storage fee -618.55 posted 2026-09-09 (Pacific), FBA Long-Term Storage Fee -118.20 posted 2026-09-16 (Pacific).

Marketplace facilitator tax collected from buyers was 7,995.89; Amazon withheld and paid it over, so it nets to 0.00 and is in none of the figures above.

**What reached the bank.** Deposited to the bank: 67,891.70 in 2 deposits: settlement 26985759971: 46,421.19 on 2026-09-01 to account x8841, settlement 27027934433: 21,470.51 on 2026-09-17 to account x8841.

Amazon's transfers posted this month: To account ending in 8841 -21,470.51 (settlement 27027934433), To account ending in 8841 -27,448.43 (settlement 27066464770).

**What Amazon still owes us.** Owed by Amazon at month end: 55,376.53, made of settlement 27066464770: 27,448.43 (closed, deposited after month end), settlement no settlement yet: 10,251.30 (posted, settlement not among the files), settlement 27108188183: 17,676.80 (posted, settlement not among the files). Of these, closed settlements not in the bank (in transit, failed or negative): settlement 27066464770 (closed, deposited after month end): 27,448.43. The reserve held at month end, apart from what is owed, was 4,502.62, from settlement 27066464770.

**Roll-forward.** Owed at the start of the month 69,067.66 plus the reserve at the start 4,069.25, plus everything posted to us in the month 54,633.94 (tax excluded, transfers and reserve lines excluded), less deposits 67,891.70, gives owed at month end 55,376.53 plus reserve at month end 4,502.62.

## Open questions
- What counts as an order in a period? Claude counted it this way: Orders placed in the period, fully cancelled ones left out Is that how you count?
- What happens when two reports cover the same lines? Claude counted it this way: Each figure from one report; the others only check it Is that how you count?

For the bookkeeper:
Product sales: 112,613.64
Refunds: -5,011.24
Net product sales: 109,215.96
Amazon fees: -42,856.49
Advertising: -11,886.85
Reimbursements: 161.32
Deposited to the bank: 67,891.70
Owed by Amazon at month end: 55,376.53
Reserve held at month end: 4,502.62
Orders: 3,005

Counted by the pinned calculation 935eb0dd68d9 ('amazon-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

Checked by pinned-calculation v0.11.6 · seal 3ec8d00c7404

---

For your bookkeeper (all amounts in US dollars; Orders is a count of orders):
Product sales: 112,613.64
Refunds: -5,011.24
Net product sales: 109,215.96
Amazon fees: -42,856.49
Advertising: -11,886.85
Reimbursements: 161.32
Deposited to the bank: 67,891.70
Owed by Amazon at month end: 55,376.53
Reserve held at month end: 4,502.62
Orders: 3,005
