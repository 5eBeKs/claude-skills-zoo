Nothing is missing. In August you took €2,819.82 in card orders and €2,448.74 was paid out to your bank, a gap of €371.08. Refunds, card fees, one chargeback and payouts that hadn't reached the bank by 31 August account for the whole gap. The largest part, €209.69, is the in-transit money, and it lands on 1–2 September. There is also one PayPal order that never goes through Shopify payouts.

I haven't been able to check the bank figure itself. To do that I need the Shopify payouts export, which is covered in the questions at the end.

Here is the checked reconciliation (also saved as `reconciliation.md`):

# August 2026: card sales vs. what reached the bank

**Read this first:**

- The bank figure is not checked: the transactions export starts on 2026-08-01 and the payouts export was not given.

**The gap: €371.08** between card orders placed in August and what was paid out to the bank in August. The bridge below closes: unexplained difference €0.00.

## The bridge

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees | 19.30 + 15.00 |
| − Still in transit at month end | 209.69 |
| = Paid out for August's card transactions | 2,448.74 |
| = **Paid out to the bank in August** | **2,448.74** |

No reserve, adjustments, failed payouts or disputes won back this month. The dispute's total cost to you is €34.30.

## Where the money went

- **Still in transit (the biggest piece):** this money is not lost, it lands in the first days of September:
#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)
- **Refunds:** all on August's own orders.
- **Card fees:** Shopify Payments processing fees on each charge.
- **Dispute (chargeback):** order #1060, amount €19.30 plus a €15.00 dispute fee.

## Not in payouts at all

Orders paid outside Shopify Payments (their money goes to that provider, not your Shopify payouts), €99.00 in total:

#1055 (PayPal Express Checkout)

## Unmatched items

None: every card order has a matching charge, every charge a counted order, and the amounts agree. No split payments, no failed payouts. The bank figure comes from the transactions alone (no payouts export was given).

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

Checked by payout-reconciliation v0.11.6 · seal 5ee8020a53aa
