<!-- numbers-0.5.2-claude-opus-5-5 / numbers-payouts / with the plugin / run 2: passed -->

Nothing is missing. Card orders came to €371.08 more than reached your bank in August, and every euro of that gap is accounted for.

# August 2026: card sales vs. what reached the bank

**The gap: €371.08.** Card orders placed in August came to €2,819.82, and €2,448.74 was paid out to the bank in August. The bridge closes with nothing left unexplained (€0.00).

The biggest single piece is not lost money: €209.69 was already on its way and lands in early September.

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees | 34.30 |
| − Still in transit at month end | 209.69 |
| **= Paid out for August's card transactions** | **2,448.74** |
| **= Paid out to the bank in August** | **2,448.74** |

"Paid out to the bank in August" is the figure to check against your bank statement. No money from July's transactions was paid out in August, so the last two lines are the same.

## Disputes

- Order #1060: €19.30 taken back, plus a €15.00 dispute fee. The fee cost almost as much as the order itself.

## Still in transit at month end

These payouts were sent but landed after 31 August:

#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)

## Not in Shopify Payments at all

This order was paid through PayPal (€99.00), so it is not in the payout report or the figures above. Look for it in your PayPal account:

#1055 (PayPal Express Checkout)

## Unmatched items

None: every card order has a matching charge, every charge has a counted order, and all amounts agree.

## Open questions

The figures above use the usual answer to each question until you confirm it; a different answer changes them.

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
