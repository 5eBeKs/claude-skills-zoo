# Stripe month-end, August 2026 (UTC)

**Sales.** 4,264 successful live charges came to **$139,409.16**. That matches the payments export exactly, and none of the test-mode payments are in the balance data. Against that:

- **Refunds:** 104 refunds totalling $3,204.12. One refund of $42.22 (order GL-109608, Aug 28) failed, but the money came back on Sep 2. That's in September, so it doesn't reduce August's refunds.
- **Disputes:** 10 chargebacks took $289.21. We won back two older disputes worth $53.45. One of those was taken in July at $32.80 and came back at $33.36 because the exchange rate had moved.
- **Net volume:** $135,969.28.
- **Sales tax:** $8,404.78 inside the charges. That's $3,481.52 on subscription invoices and $4,923.20 on shop orders, each converted at its charge's own exchange rate and rounded per charge. Without per-charge rounding the total is $8,404.72.

**What Stripe kept.** Fees were **$7,297.25**:

| Fee | Amount |
|---|---|
| Processing fees on August charges | $6,407.25 |
| Dispute fees ($150 withdrawn, $30 returned) | $120.00 |
| Billing and Tax usage fees (63 rows) | $770.00 |

The $770 includes a Billing usage fee for Aug 10 that was charged twice ($11.51). Stripe credited it back on Sep 9. Your rules say credits aren't netted against fees, so the duplicate stays in August's fees.

Stripe also started a 5% rolling reserve on Aug 25. It held $1,473.01 by Aug 31. None of it had been released by month end; releases start Sep 24.

**What reached the bank.** 18 payouts left Stripe in August for **$126,339.05**. Two payouts are left out:
- One for $3,688.05, sent Aug 13, failed with an invalid account number. The money returned to the balance on Aug 14 and went out again with the Aug 18 payout.
- The payout sent on Jul 31 ($3,552.26) arrived Aug 3, but it left Stripe in July, so it belongs to July.

The payout sent Aug 31 ($10,085.69) arrived Sep 1, so it was **in transit at month end**.

**Balance.** At 00:00 UTC on Sep 1, **$3,751.31** was still in Stripe and not yet paid out, not counting the reserve. I worked this out from which transactions each payout swept, and it ties out two ways:
- The July-end balance of $2,891.34 plus August's movement of $859.97 gives $3,751.31.
- Net volume less fees, reserve and payouts ($135,969.28 − $7,297.25 − $1,473.01 − $126,339.05) is also $859.97.

For your bookkeeper:

Gross charges: $139,409.16
Refunds: $3,204.12
Disputes withdrawn: $289.21
Disputes won back: $53.45
Net volume: $135,969.28
Sales tax collected: $8,404.78
Stripe fees: $7,297.25
Paid out to the bank: $126,339.05
Still in transit at month end: $10,085.69
Stripe balance at month end: $3,751.31
Held in reserve at month end: $1,473.01
