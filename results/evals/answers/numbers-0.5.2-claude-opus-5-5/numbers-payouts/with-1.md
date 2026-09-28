<!-- numbers-0.5.2-claude-opus-5-5 / numbers-payouts / with the plugin / run 1: passed -->

Your card sales were €371.08 more than what reached the bank in August. No money is missing: the refunds, card fees, one dispute and the payouts still in transit account for the whole gap. I ran the reconciliation script on both exports; the figures come from the script and passed its number check. Here's the full reconciliation:

---

# August 2026: card sales vs. money in the bank

**Gap: €371.08** between card orders placed in August (€2,819.82) and what Shopify Payments paid out to the bank in August (€2,448.74). The bridge closes to €0.00: nothing is unexplained. Nothing is missing. The gap is refunds, card fees, one dispute, and money that was still on its way to the bank on 31 August.

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

The last line is the figure your bank statement should show from Shopify for August. Please check it against the bank.

## Where the money went

- **Still in transit (€209.69).** This is the biggest part of the gap. The money isn't lost, it just arrives in September:
#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)
- **Refunds (€70.50).** All of it was on August orders.
- **Card fees (€56.59).** These are Shopify Payments processing fees. The totals are internally consistent. I didn't check the rates against your contract.
- **Dispute (€34.30).** Order #1060: €19.30 was taken back, plus a €15.00 dispute fee. You may be able to win back the amount (not the fee) if you respond with evidence in Shopify Admin.

**Not in payouts at all:** orders paid by PayPal (€99.00). Don't look for these in the Shopify payout report. They land in your PayPal account:
#1055 (PayPal Express Checkout)

**Unmatched items:** none. Every card order has a matching charge and every charge has an order, with no amount differences.

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

## Questions for you

The figures above use the usual answer to each question until you confirm it. A different answer would change them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
