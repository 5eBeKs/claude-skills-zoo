<!-- numbers-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 1: passed -->

No money is missing from August. Card sales were $471.77 higher than what reached the bank, and that whole gap is explained by refunds, card fees, two disputes, and money that was still on its way at month end. After those items the difference comes to $0.00.

# August payout reconciliation

**Card sales exceeded what reached the bank in August by $471.77.** The bridge below closes: the unexplained difference is $0.00. Nothing is missing. The gap is refunds, card fees, two disputes, and money still in transit at month end.

## Bridge: card sales to bank

| | USD |
|---|---:|
| Card orders (67 orders) | 4,185.63 |
| − Refunds | 58.06 |
| − Card processing fees | 141.44 |
| − Disputed amounts | 165.17 |
| − Dispute fees | 30.00 |
| + Other transactions (adjustment, dispute_won) | 99.01 |
| − In transit at month end (paid out in September) | 271.90 |
| **= Paid out for August sales** | **3,618.07** |
| + July sales paid out in early August | 95.79 |
| **= Paid out in August (should match the bank statement)** | **3,713.86** |

## Where the gap comes from

**Disputes** cost $195.17 in total:
- Order #2015: $83.66 disputed, plus a $15.00 fee
- Order #2027: $81.51 disputed, plus a $15.00 fee

The "other transactions" line includes a `dispute_won` entry, so some disputed money came back.

**In transit at month end**: $271.90 from late-August orders. This money isn't lost. It lands in September:
#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

**July sales paid out in August**: $95.79. This partly offsets the in-transit amount:
#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

**Split payment**: order #2051 was paid partly by gift card. Only its card portion of $100.12 goes through Shopify Payments. The $20.00 gift card part won't appear in any payout.

**Unmatched items**: none. Every counted order has a matching charge, and every charge has a counted order at the same amount.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

## Question for you

The figures above use the usual answer below. A different answer would change them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
