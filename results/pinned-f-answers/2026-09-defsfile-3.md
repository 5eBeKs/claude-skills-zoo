I've reconciled September 2026 (UTC) from the balance-transaction export and checked it against the payments, invoices and payouts exports.

**What we sold.** There were 4,092 successful live charges, totalling $135,375.92. Refunds came to $2,839.20: $2,881.42 refunded across 77 refunds, less one $42.22 refund that failed and came back on Sep 2. Disputes took $438.95 across 13 chargebacks, and we won back $34.20 on two disputes. That leaves net volume of $132,131.97. The charges included $8,410.74 of sales tax.

**What Stripe kept.** Fees were $7,175.00:
- $6,253.02 in processing fees on the charges.
- $165.00 in dispute fees: 13 × $15 withdrawn, less 2 × $15 returned.
- $756.98 in daily Billing and Tax usage fees.

On Sep 9 Stripe credited back $11.51 because it had charged the Aug 10 Billing fee twice. Your rules say not to net such credits against fees. It still counts in the balance.

**What reached the bank.** 21 automatic payouts left Stripe in September, totalling $118,440.79, and none failed. The last one ($4,573.56, created Sep 30) arrived Oct 1, so it was in transit at month end.

**What's still at Stripe.** At 00:00 UTC on Oct 1 the balance was $5,049.91. That figure matches two ways: the running balance, and the transactions later swept into the Oct 1 payout. Separately, $6,702.10 was held in the 5% rolling reserve. That covers what was withheld Sep 1–30, which Stripe releases after 30 days.

Things the bookkeeper should know:
- **Test payments:** 10 test-mode payments dated Sep 22 appear in the payments export. I left them out, and they never touched the balance.
- **Charges in other currencies:** EUR, GBP and CAD charges and their tax are in dollars at each charge's own rate. I converted and rounded the tax charge by charge. Converting without rounding each one would give $8,410.56, which is 18¢ less.
- **Invoices paid partly by credit:** 8 subscription invoices were paid partly from the customer's credit balance, so the charge was smaller than the invoice. I counted the full tax on each of those invoices.
- **Payments export dates:** the payments export runs from 05:17 UTC on Jul 1 to 04:47 UTC on Oct 1, not exact UTC calendar months. That's why I used the balance transactions as the source; every September charge in it matches the payments export.

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
