<!-- numbers-0.6.0-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 2: passed -->

Here is the checked text for August 2026, exactly as rendered and verified:

# August 2026 payout reconciliation

**The gap: $471.77.** Card orders placed in August came to $4,185.63; $3,713.86 reached the bank in August. Nothing is missing: the bridge below closes to $0.00 unexplained. The biggest pieces are two disputes ($195.17 including fees), money still in transit on 31 August ($271.90, landing 1–2 September) and card fees ($141.44).

## The bridge

| | USD |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| − Refunds processed in August | 58.06 |
| − Card fees | 141.44 |
| − Disputes: amount and fees (165.17 + 30.00) | 195.17 |
| + Other payout transactions (adjustment, dispute_won) | 99.01 |
| − Still in transit at month end | 271.90 |
| **= Paid out for August's card transactions** | **3,618.07** |
| + Paid out in August for earlier months' transactions | 95.79 |
| **= Paid out to the bank in August** | **3,713.86** |

The last line is the figure to check against your bank statement.

## Disputes

- #2015: $83.66 held back, plus a $15.00 dispute fee
- #2027: $81.51 held back, plus a $15.00 dispute fee

The "dispute_won" line in the payouts is part of the $99.01 credited back under "other payout transactions".

## Still in transit on 31 August

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02): these reach the bank in September's payouts.

## July orders paid out in August

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03): sold on 31 July, paid out on 3 August, so they are in August's bank deposits but not in August's sales.

## Not in payouts at all

Order #2051 ($120.12) was paid partly by gift card: only the card part, $100.12, goes through Shopify Payments. The $20.00 gift card part will never appear in a payout.

## Unmatched items

- Orders without a card charge: none
- Charges without a counted order: none
- Charges that don't match their order's amount: none

## How this was counted

Definitions:
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

The exports:
- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Files and version:
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.6.0, scripts 2ba057087965

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

1. Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
2. The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
