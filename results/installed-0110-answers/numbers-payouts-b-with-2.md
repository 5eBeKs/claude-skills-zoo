None of the money is missing. The gap between your August card orders and what reached the bank is fully explained: part of August's sales pay out in early September, and the rest went on card fees, two chargebacks, and refunds. Here is the checked reconciliation:

---

# August 2026: card sales vs. payouts

**Warning, read first:**

- The bank figure is not checked: the payouts export was not given, so what reached the bank is taken from the transactions export alone.

The gap between August's card orders and what reached the bank in August is **$471.77**. The bridge below closes: nothing is unexplained (0.00).

## The bridge

| | USD |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| minus Refunds processed in August | 58.06 |
| minus Card fees | 141.44 |
| minus Disputes: amount and fees | 165.17 and 30.00 |
| plus Disputes won back | 83.66 |
| plus Dispute fees returned | 15.00 |
| Shopify adjustments | 0.35 |
| minus Still in transit at month end | 271.90 |
| **= Paid out for August's card transactions** | **3,618.07** |
| plus Paid out in August for earlier months' transactions | 95.79 |
| **= Paid out to the bank in August** | **3,713.86** |

"Paid out to the bank in August" is the figure to find on your bank statement. No reserve was held or released and no payout failed.

## Where the gap goes

- **Card fees** are the steady cost of taking cards.
- **Disputes (chargebacks)**: two in August. Their net cost after what was won back is 96.51.
  - Order #2015: amount 83.66, fee 15.00
  - Order #2027: amount 81.51, fee 15.00
- **Refunds**: all of them were on August's own orders.
- **Timing, not lost money**: some August sales pay out in early September, and some late-July sales paid out in August.

### Still in transit at month end (arrives in September)

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

### July orders paid out in August

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

### Orders paid partly another way

Only the card part of these reaches the payouts:

#2051 (Gift card, Shopify Payments)

No orders were paid entirely outside Shopify Payments, and every card order matched its charge: nothing unmatched.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.11.0, scripts a07884a2bdbf

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by payout-reconciliation v0.11.0 · seal 173f4c9208cd

---

- **Checking the bank figure:** send the payouts export too (Finances > Payouts > Export). I'll then check the bank figure against each payout that reached the bank.
- **Order #2051:** it was paid partly with a gift card, and only the card part reaches the payouts.
