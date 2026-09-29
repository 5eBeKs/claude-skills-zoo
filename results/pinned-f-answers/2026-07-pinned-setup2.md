July 2026 passed every check, so I've pinned it: pin `d8c663a3d3cd`, pin 1, in `.pinned/stripe-month-end.pin.json`. The full answer is saved in `.pinned/stripe-month-end/answer-2026-07.md`. For August, September and later months, the pin runs the same code with the same definitions. If a file changes shape, or a new transaction type or status appears, it warns you by name.

**Sales tax is short, as you accepted.** 43 July charges have their tax in no file. Together they are **$1,176.69 of gross charges (0.94%)**. The sales tax line leaves out their tax, and every answer names these charges.
- 26 order payments were made before the payments export begins at 2026-07-01 05:17:29 UTC.
- 17 subscription charges come from invoices older than the invoices export, which begins at 2026-07-01 05:23:19 UTC. Most were charged later in July.
- If any other charge has no tax that the files can find, the check still fails.

The 43 charges are:
ch_3xkPHV9fHvRz2kWb0GIZdcWL, ch_3xkPR19fHvRz2kWb2Jk3Tk7B, ch_3xkPWm9fHvRz2kWb3PYmZWCK, ch_3xkPX99fHvRz2kWb1N7vOHWJ, ch_3xkPav9fHvRz2kWb2gE5YHsS, ch_3xkPoT9fHvRz2kWb0c4kjHqL, ch_3xkPqf9fHvRz2kWb2V8UnBIp, ch_3xkPyq9fHvRz2kWb0ns6HP2K, ch_3xkQKn9fHvRz2kWb3zjWxhcR, ch_3xkQUJ9fHvRz2kWb3VVx4XJE, ch_3xkQcM9fHvRz2kWb0vfLx7v1, ch_3xkQi69fHvRz2kWb12Kw0mm3, ch_3xkQxM9fHvRz2kWb1CbqvfNp, ch_3xkR5q9fHvRz2kWb2BEKu2wU, ch_3xkR729fHvRz2kWb1vyBWSvz, ch_3xkR7w9fHvRz2kWb1oNdFf9J, ch_3xkRdN9fHvRz2kWb2CaNLPge, ch_3xkSAt9fHvRz2kWb3Ptg6Z65, ch_3xkSEP9fHvRz2kWb0ie3af3z, ch_3xkSL79fHvRz2kWb3JhC4qJF, ch_3xkTM49fHvRz2kWb06Y7xiaJ, ch_3xkTQc9fHvRz2kWb1foQ8PpG, ch_3xkTSn9fHvRz2kWb2yaRa4Rd, ch_3xkTUt9fHvRz2kWb2Q3C0lRF, ch_3xkTcH9fHvRz2kWb2flIycup, ch_3xkTm99fHvRz2kWb0klNwYIK, ch_3xkUDB9fHvRz2kWb00XQPt2I, ch_3xkdUo9fHvRz2kWb1MLDcs8w, ch_3xkhfz9fHvRz2kWb2W9PxbwJ, ch_3xkmCy9fHvRz2kWb2pXiAgfH, ch_3xkoHk9fHvRz2kWb1eNKjnx6, ch_3xl4Hg9fHvRz2kWb1dIcm6E2, ch_3xl5ap9fHvRz2kWb10I34zqZ, ch_3xl8NU9fHvRz2kWb3NU7990Y, ch_3xlAKW9fHvRz2kWb2EEZ35Sx, ch_3xlQev9fHvRz2kWb1cTbks3w, ch_3xm1TI9fHvRz2kWb0dSPivQD, ch_3xmPaN9fHvRz2kWb0hcHN5SQ, ch_3xmlGi9fHvRz2kWb1sBuKns3, ch_3xmoc99fHvRz2kWb2ejNRdUo, ch_3xncZL9fHvRz2kWb2iKpr4R0, ch_3xp87x9fHvRz2kWb3vB7Q2zD, ch_3xpx9y9fHvRz2kWb22o0JFJa

**July in short:**
- **Sales:** 3,863 live payments. 9 test-mode payments were left out.
- **Disputes:** 11 disputes were withdrawn. One dispute from June was won back in July (du_1xVCGp9fHvRz2kWb2qc1BET2).
- **Stripe fees:** processing fees $5,880.24, plus dispute fees $165.00 less $15.00 returned, plus Billing and Tax usage fees of $724.91.
- **Payouts:** 22 payouts, none failed. One payout (po_1xvc079fHvRz2kWb2Te3R2Rs) left Stripe on July 31 and arrived on August 3. Nothing was held in reserve at the end of July.

**Where your definitions left something open, I took these readings:**
- A month starts at 00:00:00 UTC on the 1st and ends just before 00:00:00 UTC on the next 1st.
- Sales tax in dollars is each charge's tax in its own currency, converted at that charge's own rate and rounded to the cent per charge.
- A payout "did not fail" when its status is paid or in_transit. It is "still in transit" when it arrives on or after the next 1st.
- Credits Stripe gives back (a fee row with a positive amount, or an adjustment) go in no line and are named. There were none in July.
- A bank-debit payment that fails later comes off gross charges in the month it fails. There were none in July.
- A repeated transaction ID, a new transaction type, or a second currency makes the check fail.
- Stripe's fee on a refund is not given back, which is what the files show.
- The balance at month end is every balance row created before the next 1st that no payout created before then has paid out.

The saved answer lists these readings as open questions every month until you confirm them.

Counted by the pinned calculation d8c663a3d3cd ('stripe-month-end', pin 1).

Gross charges: $125,344.26
Refunds: $3,027.18
Disputes withdrawn: $265.14
Disputes won back: $16.09
Net volume: $122,068.03
Sales tax collected: $7,991.58
Stripe fees: $6,755.15
Paid out to the bank: $116,434.78
Still in transit at month end: $3,552.26
Stripe balance at month end: $2,891.34
Held in reserve at month end: $0.00
