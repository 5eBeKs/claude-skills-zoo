<!-- numbers-0.5.2-claude-opus-5-5 / numbers-payouts / with the plugin / run 3: passed -->

Nothing is missing. The whole difference is accounted for, and the reconciliation below comes out with nothing left unexplained. Here it is:

---

# August 2026: card sales vs. money in the bank

**The gap: €371.08.** Card orders placed in August came to €2,819.82; €2,448.74 reached the bank in August. The bridge below closes to zero (unexplained difference €0.00); nothing is missing, it is refunds, fees, one dispute and money still on its way.

## The bridge

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees (19.30 + 15.00) | 34.30 |
| − Still in transit at month end | 209.69 |
| **= Paid out for August's card transactions** | **2,448.74** |
| **= Paid out to the bank in August** | **2,448.74** |

The last line is the figure your bank statement should show for Shopify Payments in August; check it against the bank.

## Where the money went

- **Refunds:** €70.50, all on August orders.
- **Card fees:** €56.59 across 57 card orders.
- **Dispute:** order #1060, €19.30 taken back plus a €15.00 dispute fee.
- **Still in transit at 31 August:** €209.69, due in early September: #1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02). This should show up in your September bank statement.
- **Not in payouts at all:** €99.00 paid through PayPal (#1055 (PayPal Express Checkout)). It is not part of the card sales above; look for it in your PayPal account, not the payout report.

No earlier months' sales were paid out in August, and every card order matched its charge: there are no orders without a charge, charges without an order, or amount mismatches.

## Open questions

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.5.2, scripts 05e46938ecfc
