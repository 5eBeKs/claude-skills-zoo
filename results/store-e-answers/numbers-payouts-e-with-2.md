My earlier summary had some figures typed by hand, so here is the same answer generated straight from the reconciliation results. The full answer, with every order listed, is saved as `files/reconciliation_2026-08.md`.

# Shopify Payments payout reconciliation: August 2026

**The gap: €84,898.63.** Card orders placed in August came to €436,193.70, and €351,295.07 was paid out to the bank in August. The bridge below closes with an unexplained difference of €0.00. The August total also matches the payouts export (€351,295.07).

Orders paid outside Shopify Payments (PayPal, Klarna, bank deposit and others) came to €240,650.52. They never go through Shopify payouts, so that money is not part of this gap. It arrives through PayPal, Klarna or the bank directly.

## The bridge

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 436,193.70 |
| − Refunds processed in August | 21,753.94 |
| &nbsp;&nbsp;of which on orders from earlier months | 11,769.23 |
| − Card fees | 9,559.62 |
| − Disputes: amount and fees | 811.49 + 45.00 |
| Reserve held (-) or released (+) by Shopify | -7,500.00 |
| − Still in transit at month end | 87,828.85 |
| **= Paid out for August's card transactions** | **313,784.04** |
| + Paid out in August for earlier months' transactions | 37,511.03 |
| **= Paid out to the bank in August** | **351,295.07** |

Where the rest went:

- **Refunds:** €21,753.94 was refunded in August, and €11,769.23 of that was on orders from earlier months.
- **Card fees:** €9,559.62.
- **Disputes:** the net cost was €856.49.
- **Reserve:** Shopify is holding €7,500.00. It was still held at month end.
- **In transit:** €87,828.85 from late-August sales was paid out in September.
- **Coming the other way:** €37,511.03 paid out in August was for July transactions.

## Disputes

| Order | Amount | Fee |
|---|---:|---:|
| #54410 | -69.90 | -15.00 |
| #59420 | 189.70 | 15.00 |
| #47732 | -44.85 | -15.00 |
| #56944 | 298.00 | 15.00 |
| #55843 | 32.77 | 15.00 |
| #57176 | 107.77 | 15.00 |
| #55031 | 298.00 | 15.00 |

## Failed payout

2026-08-28 (14,902.03)

The bank figure was checked against the payouts export.

## Still in transit at month end (paid out in September)

1,021 orders. The full list, with payout dates, is in `files/reconciliation_2026-08.md`.

## July orders paid out in August

434 transactions. The full list is in `files/reconciliation_2026-08.md`.

## Unmatched items

Card orders with no charge in the transactions export:

#66633, #65713, #64777, #63765, #63758, #63757

Charges with no counted August order (for example, test, cancelled or excluded orders, or orders from another month):

73 charges. The full list is in `files/reconciliation_2026-08.md`.

Orders where the amount charged differs from the order total:

#66587, #65607, #65290, #65125, #64246, #63920, #63249, #63194, #62844, #62770, #62729, #62643, #62317, #61764, #61581, #61533, #61128, #60414, #60345

Orders where the rest was charged after August ended:

#66416

## Split payments (gift card + card)

Only the card part reaches the payouts.

50 orders. The full list, with each card part and the rest, is in `files/reconciliation_2026-08.md`.

## Orders paid outside Shopify Payments (not in payouts)

2,058 orders. The full list is in `files/reconciliation_2026-08.md`.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: authorized, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: EUR; payment method: Bank Deposit, Cash, Klarna, PayPal Express Checkout, Shopify Payments, bogus, gift_card, manual; tags: b2b, duplicate, horeca, replacement, telefonisch, test)
- the payout export has records on 31 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund, reserve; payout status: failed, paid, pending, scheduled; currency: EUR)
- checked against the payouts export: 19 payouts paid in August 2026, 351295.07
- paid out in month: matches the figure in the payouts export (351295.07; computed 351295.07)

- orders_export.csv: 37,159 rows, SHA-256 9183e83aad61ad26
- payment_transactions_export.csv: 20,718 rows, SHA-256 512dca5b13bca0d2
- payouts_export.csv: 89 rows, SHA-256 db235a9ab3596b27
- computed by shopify-month-end v0.10.1, scripts f8813207140f

## Questions for you

The figures above use the usual answer to each of these questions until you confirm it. A different answer would change them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
