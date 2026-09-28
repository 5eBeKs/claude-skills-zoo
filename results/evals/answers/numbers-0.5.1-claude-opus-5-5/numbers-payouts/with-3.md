<!-- numbers-0.5.1-claude-opus-5-5 / numbers-payouts / with the plugin / run 3: passed -->

No money is missing. You had €2,819.82 in card orders in August and €2,448.74 reached the bank. The €371.08 difference is fully explained by refunds, card fees, one dispute and money still in transit, and the bridge below closes to €0.00. Here is the reconciliation, with every figure checked against both exports:

---

# August 2026: card sales vs. money in the bank

**Gap: €371.08** between card orders placed in August and what Shopify Payments paid out to the bank in August. Nothing is missing: the bridge below closes to €0.00.

## The bridge

| | Line | EUR |
|---|---|---:|
| | Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − | Refunds processed in August | 70.50 |
| − | Card fees | 56.59 |
| − | Disputes: amount and fees | 19.30 + 15.00 = 34.30 |
| − | Still in transit at month end | 209.69 |
| = | Paid out for August's card transactions | 2,448.74 |
| = | **Paid out to the bank in August** (check this against the bank statement) | **2,448.74** |

All August payouts were for August transactions; nothing from earlier months was paid out in August.

## Where the gap went

- **Money still on its way:** €209.69 was in transit on 31 August and lands in early September:
#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)
- **Refunds:** €70.50, all on August orders.
- **Card fees:** €56.59, taken by Shopify Payments before paying out.
- **Dispute:** order #1060 was charged back: €19.30 taken back plus a €15.00 dispute fee.

**Not in the payouts at all:** orders paid with PayPal (€99.00) go to your PayPal account, not through Shopify Payments, so don't look for them in the payout report:
#1055 (PayPal Express Checkout)

**Unmatched items:** none. Every card order has a matching charge, and every charge matches its order amount.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
- payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
- computed by shopify-month-end v0.5.1, scripts 32efef0622a7

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer would change them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
