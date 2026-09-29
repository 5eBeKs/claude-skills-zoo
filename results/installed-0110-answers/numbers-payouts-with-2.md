No money is missing. The €371.08 gap between August card sales and what was paid out is fully accounted for by refunds, card fees, one chargeback, and payouts that hadn't reached the bank by 31 August. The one caveat is in the warning at the top: I couldn't check the bank figure itself. Here is the checked reconciliation (also saved as `reconciliation.md`):

---

# August 2026: card sales vs. money paid out to the bank

**Warning, read first:**

- The bank figure is not checked: the transactions export starts on 2026-08-01 and the payouts export was not given.

**The gap: €371.08** between card orders placed in August and what was paid out to the bank in August. None of it is missing money: it is refunds, card fees, one dispute, and payouts that were still on their way to the bank on 31 August. The bridge below closes with an unexplained difference of €0.00.

## The bridge

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees | 19.30 + 15.00 |
| Reserve held (-) or released (+) by Shopify | 0.00 (still held at month end: 0.00) |
| Failed payout paid again | 0.00 |
| Shopify adjustments | 0.00 |
| − Still in transit at month end | 209.69 |
| **= Paid out for August's card transactions** | **2,448.74** |
| **= Paid out to the bank in August** | **2,448.74** |

The last line is the figure to look for on your bank statement.

## Where the money went

- **Refunds:** refunds processed in August came to €70.50.
- **Card fees:** Shopify Payments kept €56.59 in card fees.
- **Dispute:** one chargeback, order #1060: amount €19.30, dispute fee €15.00. The dispute's total cost is €34.30.
- **Still in transit at month end** (paid out in early September, so they will be on September's bank statement):

#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)

## Not in the payouts at all

This order was paid through PayPal, so its money went to your PayPal account, not through Shopify Payments. Don't look for it in the payout report:

#1055 (PayPal Express Checkout)

Total paid outside Shopify Payments: €99.00.

## Everything else matched

Every card order had a matching charge with the same amount, there were no charges without an order, no split payments, and no failed payouts. The bank figure is not checked against the payouts export (see the warning above); it comes from the transactions export alone.

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
- computed by shopify-month-end v0.11.0, scripts a07884a2bdbf

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
- The transactions export starts on 2026-08-01, so the payouts of the first days of August 2026 may be short of what the bank received. Can you add the payouts export (Finances > Payouts > Export) to check the bank figure?

Checked by payout-reconciliation v0.11.0 · seal 09e87a746a56
