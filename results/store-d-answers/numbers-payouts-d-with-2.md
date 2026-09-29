**$572,456.23 reached your bank from Shopify Payments in June**, across 20 payouts. That matches your payouts export exactly. Card orders placed in June came to $691,562.27, so **the gap is $119,106.04**. Every dollar of it is accounted for: the unexplained difference is $0.00.

The full answer, with every order listed, is saved at `files/reconciliation_2026-06.md`. It passed the number check. Below is the same answer with the long lists shown as counts; that short version was not number-checked on its own.

## The bridge

| | USD |
|---|---:|
| Card orders placed in June (Shopify Payments, shipped yet or not) | 691,562.27 |
| − Refunds processed in June | 82,726.47 |
|   of which on orders from earlier months | 45,616.95 |
| − Card fees | 25,967.07 |
| − Disputes: amount and fees | 1,212.93 + 240.00 |
| Reserve held (-) or released (+) by Shopify | 0.00 |
| Failed payout paid again | 0.00 |
| Shopify adjustments | 0.00 |
| − Still in transit at month end | 117,366.90 |
| **= Paid out for June's card transactions** | **467,444.55** |
| + Paid out in June for transactions before the transactions export starts | 105,011.68 |
| **= Paid out to the bank in June** | **572,456.23** |

The last line is the figure to look for on your bank statement.

## Where the rest of June's sales went

- **Still in transit: $117,366.90.** This is the biggest part. It is 1,512 transactions that were paid out in early July.
  - It includes the **payout of 30 June for $18,132.40, which failed** and did not reach the bank in June.
  - The payouts export shows it was retried in the payout of 7 July.
  - It's worth asking your bank why that payout bounced.
- **Refunds: $82,726.47.** $37,109.52 was on June orders and $45,616.95 was on orders from earlier months.
- **Card fees: $25,967.07.** These are Shopify Payments' processing fees. The check confirms the figures are consistent with each other, not that they match your contracted rates.
- **Disputes: $1,452.93 in total.** There were 16 chargebacks, all on orders from before June. None were won back in June:
  - #45476 82.80 + fee 15.00; #43139 202.09 + 15.00; #42339 19.60 + 15.00; #46132 99.94 + 15.00
  - #48748 34.95 + 15.00; #50960 85.00 + 15.00; #46564 34.95 + 15.00; #46016 85.96 + 15.00
  - #47881 32.15 + 15.00; #48462 191.89 + 15.00; #43365 70.95 + 15.00; #47863 71.86 + 15.00
  - #42377 32.81 + 15.00; #46314 52.58 + 15.00; #43148 45.39 + 15.00; #43258 70.01 + 15.00
- **Partly offset by earlier sales: $105,011.68.** The payouts of 1 to 4 June carried transactions from before 1 June, which is when the transactions export starts. They reached the bank in June, so they are added back:
  - 2026-06-01: 17,678.53
  - 2026-06-02: 21,209.54
  - 2026-06-03: 60,256.61
  - 2026-06-04: 5,867.00

## Not in Shopify payouts at all

- **610 orders ($82,635.67) were paid outside Shopify Payments:** PayPal, bank deposit, cash, COD, manual payment or gift card. They are not part of the $691,562.27 above, and they will never appear in Shopify payouts. PayPal money arrives through PayPal, and the rest reaches you directly.
- **87 orders were split between a gift card and a card.** Only the card part is counted in the bridge.

## Items to look at

- **Orders without a card charge:** 0.
- **135 card charges in June with no counted June order.** The money is in the payouts, but the order doesn't count as a June card sale. For example, it may be from another month, excluded, or not marked as Shopify Payments.
- **179 orders where the amount charged differs from the order total.** Typical causes are gift card parts, edited orders or partial captures.
- **5 orders whose balance was charged after June ended:**
  - #55864 75.52 on 2026-07-01
  - #55838 52.85 on 2026-07-01
  - #55835 82.80 on 2026-07-02
  - #55667 196.73 on 2026-07-03
  - #55378 98.00 on 2026-07-01

## Questions for you

The figures above use the usual answer to each question until you confirm it. A different answer would change them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet. Are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and any new value next month will be flagged.

## How this was counted

- **Definitions:** orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales. This is the usual answer; please confirm it.
- **Coverage:** both the orders export and the transactions export have records on all 30 days of June 2026.
- **Checked against:** the payouts export, which shows 20 payouts paid in June totalling 572,456.23. Nothing from outside the exports was used as a check.
- **Files:**
  - orders_export.csv: 58,166 rows, SHA-256 4c14bc07ab3d150c
  - payment_transactions_export.csv: 32,249 rows, SHA-256 a6932219963161c3
  - payouts_export.csv: 68 rows, SHA-256 cc95fc92640b4c98
- **Computed by:** shopify-month-end v0.7.0, scripts fdccef760565
