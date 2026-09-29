I've pinned July's calculation. Every check passed on July, and the same calculation also runs cleanly on August and September. For those months, and any after, run:

`python <skill>/scripts/pin.py answer .pinned/amazon-month-end.pin.json -- --month 2026-08 files/*`

It counts each month exactly the way July was counted. If Amazon adds a new kind of line or changes its export, the answer warns you or stops instead of guessing. The pinned file is `.pinned/amazon-month-end.pin.json` (id ee1f712540ac, pin 1). July's full answer, including the list of what was counted twice and the deliberately broken files, is in `.pinned/amazon-month-end-2026-07-answer.md`.

## Amazon month-end, July 2026 (US dollars)

**What we sold**
| | USD |
|---|---:|
| Product sales | 112,818.17 |
| Shipping credits | 4,760.87 |
| Gift wrap credits | 139.72 |
| Promotional rebates | -3,467.27 |
| Refunds (principal -4,398.43, shipping -87.87, gift wrap 0.00, promotions returned 97.17) | -4,389.13 |
| **Net product sales** | **109,862.36** |

- **Orders:** 3,208 were purchased in July; 27 cancelled orders are left out.

**What Amazon kept**
| | USD |
|---|---:|
| Referral fees | -16,617.62 |
| FBA fulfilment fees | -19,422.42 |
| Storage fees | -683.23 |
| Other fees* | -6,750.81 |
| **Amazon fees, total** | **-43,474.08** |
| Advertising | -13,275.33 |
| Reimbursements | 208.75 |

\*Other fees are:
- shipping and gift wrap chargebacks: -2,463.84
- Buy Shipping labels: -4,017.28
- inbound placement: -100.80
- coupons: -67.70
- removal: -61.20
- subscription: -39.99

**Tax:** Amazon collected 8,063.67 in marketplace facilitator tax and paid over -8,063.67, so it nets to 0.00. Every line of the month has a place; nothing was left out.

**What reached the bank and what Amazon still owes**
- **Deposited in July: 37,361.77**
  - 2026-07-09: settlement 26821949902, 22,879.57
  - 2026-07-23: settlement 26860307225, 14,482.20
- **Owed by Amazon at month end: 49,054.47**
  - The open settlement 26900538638 held 33,922.76 of lines posted by July 31.
  - Its reserve release adds 4,380.22.
  - Deferred lines add 15,131.71. These were posted in July but sit in settlement 26944784040, which opens August 4.
  - The reserve held is taken off: -4,380.22.
- **Reserve held: 4,380.22**, the Current Reserve Amount of settlement 26860307225.
- **Balance check:** Amazon held 37,474.76 for us on July 1, reserve included. The month's lines added 53,321.70 and the bank received 37,361.77, which leaves 53,434.69 held on July 31.

**Checks that passed:**
- All 8 settlements add up to their totals.
- The reserve carries over correctly from one settlement to the next.
- All 3,790 July postings in the Date Range report match the settlement files line by line.
- Each bank deposit equals its settlement's total.
- No row appears twice.
- The reports cover every day of July.
- No order line posted before its purchase.

## Where your definitions left something open
- **Where the month's lines come from:** I used the Date Range report, placed by its posted time in Pacific time. I used the settlement files to see which settlement each line belongs to, to read the reserve, and to check the two reports against each other.
- **Orders:** distinct order ids from the All Orders report purchased in the month, Pacific time. Fully cancelled orders are left out; an order with only some items cancelled still counts.
- **Deferred lines:** a line posted in the month that belongs to a settlement opening later is counted as owed. This is the 15,131.71 above.
- **Failed deposit:** it stays owed until Amazon credits it back, and after that it counts only in the settlement that received it. This matters for August: settlement 26944784040 (21,849.95) never reached the bank and was credited back on August 25.
- **A negative settlement:** it's counted as owed (negative) until the next settlement takes it over as Payable to Amazon.
- **Storage and removal:** "FBA storage fee" is the monthly storage fee and "FBA Long-Term Storage Fee" is the aged-inventory fee. Removal Order Return and Disposal fees count as removal and disposal.
- **New kinds of line:** a kind of line your definitions don't name is left out of every figure and named, and a check fails until you tell me how it counts.
- **Smaller readings:**
  - A line at exactly midnight belongs to the new month.
  - Each deposit is matched to its settlement by settlement id.
  - The only adjustments counted are FBA Inventory Reimbursements.
  - Descriptions are matched only as exact names.
  - No refund rate is shown.

The saved answer lists these under "Open questions" using the generic payments-checklist wording (the checklist's names for the options). I can't change that wording, so please read the list above as what they mean for Amazon.

## Things to know
- **Repeated lines:** a line repeated word for word makes the answer warn you but doesn't stop it. The saved answer says "stops the calculation", which is wrong.
- **Bank account change:** deposits changed from the account ending 4417 to the one ending 8841 from September 1. Your bank list covers both.

For the bookkeeper (US dollars):

Product sales: 112,818.17 USD
Refunds: -4,389.13 USD
Net product sales: 109,862.36 USD
Amazon fees: -43,474.08 USD
Advertising: -13,275.33 USD
Reimbursements: 208.75 USD
Deposited to the bank: 37,361.77 USD
Owed by Amazon at month end: 49,054.47 USD
Reserve held at month end: 4,380.22 USD
Orders: 3,208
