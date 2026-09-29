## Stripe month-end, September 2026 (UTC)

**Sales.** There were 4,092 successful live charges, totalling $135,375.92. Refunds came to $2,839.20 net. There were 13 new chargebacks for $438.95, and 2 disputes won back for $34.20. That leaves net volume of **$132,131.97**. Sales tax inside those charges was $8,410.74.

**What Stripe kept.** Fees came to **$7,175.00**:
- Processing fees on the charges: $6,253.02
- Dispute fees: $195.00 withdrawn less $30.00 returned
- Daily Billing and Tax usage fees: $756.98

Stripe also withheld a 5% rolling reserve from our balance: $5,229.09 net for the month.

**What reached the bank.** 21 payouts totalling $118,440.79 left Stripe in September, and none failed. The last one ($4,573.56, sent Sept 30) arrived on October 1, so it was still in transit at month end.

**Checks I ran:**
- Every charge ties to the payments export, amount and fee both.
- Every payout ties to the items listed under it, except the two earliest in July, whose items fall before the export window (it starts July 1).
- The month balances: net volume − fees + the fee credit − payouts − reserve = $1,298.60, which matches the actual change in our Stripe balance.

**How I applied the definitions:**
- **Test mode:** the 10 test payments ($516.94) are only in the payments export and aren't counted.
- **Refunds:** the $2,839.20 is $2,881.42 in refunds less a $42.22 refund that failed and came back on Sept 2.
- **Fee credit:** Stripe gave back $11.51 on Sept 9 for a duplicate Billing fee from August. It is not netted against fees.
- **Foreign-currency disputes:** the three EUR/GBP disputes are counted at the dollar amounts Stripe actually took.
- **Sales tax:** product orders use the tax figure stored on the payment, and subscriptions use the invoice's tax. Each is converted at its charge's own exchange rate. For EU/UK VAT invoices the tax is included in the price, and it's still counted.
- **Balance and reserve:** the month-end balance is the money that was in Stripe at 00:00 UTC on Oct 1 and was paid out on Oct 2 and Oct 5. The reserve is what was withheld and not yet released by then. It's the 30 daily withholdings made Sept 1–30, since everything withheld in August was released by Sept 30.

Gross charges: $135,375.92
Refunds: $2,839.20
Disputes withdrawn: $438.95
Disputes won back: $34.20
Net volume: $132,131.97
Sales tax collected: $8,410.74
Stripe fees: $7,175.00
Paid out to the bank: $118,440.79
Still in transit at month end: $4,573.56
Stripe balance at month end: $5,049.91
Held in reserve at month end: $6,702.10
