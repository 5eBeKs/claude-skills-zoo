In August 2026 you sold **$139,409.16**, and after refunds and disputes net volume was **$135,969.28**. Stripe kept **$7,297.25** in fees. **$126,339.05** was paid out to the bank, and **$10,085.69** of that was still on its way at month end. The Stripe balance at month end was **$3,751.31**, with another **$1,473.01** held in reserve.

**How the figures were built**
- **Sales:** 4,264 successful live charges, converted at each charge's own exchange rate (2,983 in USD, 562 in EUR, 423 in GBP, 296 in CAD). The 38 test-mode payments are not included.
- **Refunds:** 104 refunds, $3,204.12. One refund of $42.22, made on Aug 28, failed and the money came back on Sep 2. Following your rules it stays in August's refunds and belongs to September's figures.
- **Disputes:** 10 disputes took $289.21 from the balance. Two were won back for $53.45 (one CAD, one USD).
- **Stripe fees:**
  - Processing fees on the charges: $6,407.25.
  - Dispute fees: $150 charged ($15 × 10), less $30 returned on the two disputes you won.
  - Billing and Tax fee rows: $770.00. This includes a duplicate Billing fee of $11.51 charged on Aug 11. Stripe credited it back on Sep 9, and under your rules the credit is not netted against fees.
- **Sales tax:** $8,404.72 in total: $3,481.52 on subscription invoices and $4,923.20 on one-off orders. The order tax comes from each payment's `tax_amount` field. Stripe's daily Tax fee moves with order volume, which suggests Stripe Tax calculates those orders too. Your bookkeeper should confirm this, because without the orders the figure would be $3,481.52. Foreign-currency tax was converted at each charge's own rate. It is the full invoice tax even where a customer credit reduced the amount charged (9 invoices).
- **Payouts:** 19 payouts were created in August, totalling $130,027.10. One of them, $3,688.05 on Aug 13, failed because of an invalid bank account number. The money came back to the balance on Aug 14, so it is left out. Payouts then resumed on Aug 18. The Aug 31 payout of $10,085.69 arrived on Sep 1, so it counts as still in transit.
- **Month-end balance and reserve:** I worked out the balance two ways and both give $3,751.31, which does not include the reserve. It is August's charges and dispute rows that no payout created before Sep 1 had yet covered. It also matches the running total of every balance movement since July 1. The reserve started on Aug 25 as a daily 5% hold, with $1,473.01 withheld by month end. The first release came on Sep 24.

Gross charges: $139,409.16
Refunds: $3,204.12
Disputes withdrawn: $289.21
Disputes won back: $53.45
Net volume: $135,969.28
Sales tax collected: $8,404.72
Stripe fees: $7,297.25
Paid out to the bank: $126,339.05
Still in transit at month end: $10,085.69
Stripe balance at month end: $3,751.31
Held in reserve at month end: $1,473.01
