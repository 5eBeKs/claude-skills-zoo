Nothing is missing. Of August's €371.08 gap, part went to refunds, card fees and one chargeback. The other €209.69 was still on its way to your bank on 31 August and lands in early September. The whole gap is explained, with nothing left over. The one caveat: I haven't checked the bank figure against your actual payouts yet (see the warning at the top of the report).

The checked report is below, exactly as it was produced. It's also saved as `reconciliation.md` in your working folder.

---

# Where August's money went

**Warning, before any figure:**

- The bank figure is not checked: the transactions export starts on 2026-08-01 and the payouts export was not given.

Card sales in August came to €2,819.82, and €2,448.74 was paid out to the bank in August. The gap between card sales and what reached the bank in the month is **€371.08**. The bridge closes with an unexplained difference of €0.00: every euro of the gap is accounted for below.

## The bridge

| | EUR |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 2,819.82 |
| − Refunds processed in August | 70.50 |
| − Card fees | 56.59 |
| − Disputes: amount and fees | 19.30 + 15.00 |
| − Still in transit at month end | 209.69 |
| = Paid out for August's card transactions | 2,448.74 |
| = Paid out to the bank in August | 2,448.74 |

The last line is the figure to find on your bank statement. No reserves, adjustments, failed payouts or payouts for earlier months' sales appear in the export.

## What the gap is made of

- **Refunds** processed in August: €70.50, all on August orders.
- **Card fees** from Shopify Payments: €56.59.
- **Disputes (chargebacks)**: the net cost of disputes is €34.30.
  - Order #1060: amount €19.30, dispute fee €15.00.
- **Money still in transit** at month end, arriving in early September:

#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)

This part is not lost: it lands in September's bank statement.

## Not in the payouts at all

This order was paid through PayPal, so its money is in your PayPal account, not in Shopify payouts (it is also not part of the card sales figure above):

#1055 (PayPal Express Checkout)

## Unmatched items

Every card order matched a charge at the same amount; no orders without a charge, no charges without an order, no split payments and no failed payouts. The bank figure comes from the transactions alone (the payouts export was not given), so it has not been checked payout by payout.

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

Checked by payout-reconciliation v0.11.6 · seal 683371134d22
