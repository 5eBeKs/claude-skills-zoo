I reconciled the two exports and every euro of the gap is accounted for. There's one caveat first: I couldn't check the bank figure below against Shopify's payout totals, because you didn't include the payouts export. The full answer, which is also saved as `reconciliation.md`:

---

# Where August's card sales went

**Warning first:**

- The bank figure is not checked: the transactions export starts on 2026-08-01 and the payouts export was not given.

Card orders placed in August came to €2,819.82, but only €2,448.74 was paid out to the bank in August: a gap of **€371.08**. The bridge below explains all of it; the unexplained difference is €0.00.

## The bridge

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees | 19.30 |
| − Disputes: amount and fees | 15.00 |
| − Still in transit at month end | 209.69 |
| **= Paid out for August's card transactions** | **2,448.74** |
| **= Paid out to the bank in August** | **2,448.74** |

No reserve, adjustments, failed payouts or earlier months' transactions affected August. The last line is the figure to match against your bank statement.

## The pieces

- **Refunds:** all on August's own orders.
- **Card fees:** Shopify Payments' processing fees on each charge.
- **Dispute:** order #1060, amount €19.30, dispute fee €15.00; the dispute's total cost is €34.30. Nothing was won back yet.
- **Still in transit at month end** (these land in September, with payout dates):

#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)

## Not in the payouts at all

Orders paid outside Shopify Payments never show up in the payout report, so don't look for this money there; it went to PayPal:

#1055 (PayPal Express Checkout)

Every card order matched its charge: no orders without a charge, no charges without an order, no amount mismatches and no split payments.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- the transactions export starts on 2026-08-01: payouts early in August 2026 may carry earlier transactions it does not have, so the bank figure is not checked; add the payouts export (Finances > Payouts > Export)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.11.6, scripts 6e9e71a410d0

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
- The transactions export starts on 2026-08-01, so the payouts of the first days of August 2026 may be short of what the bank received. Can you add the payouts export (Finances > Payouts > Export) to check the bank figure?

Checked by payout-reconciliation v0.11.6 · seal 07f720cc04d3
