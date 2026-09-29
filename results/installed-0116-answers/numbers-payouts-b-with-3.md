No money is missing. You placed **$471.77** more in card orders in August than reached your bank, and every dollar of that gap is accounted for (unexplained difference: 0.00). Card fees are the largest piece, followed by two chargebacks (customer disputes) and three orders whose payouts only arrived in early September. A small amount from July sales landed in August and offsets part of the gap.

One caveat: you didn't include the payouts export, so the bank figure below comes from the transactions file alone. To check it against what actually arrived, export Finances > Payouts > Export and send it over. You could also just compare the **3,713.86** figure with your bank statement.

Here is the full reconciliation:

---

# August 2026 payout reconciliation

**Warnings**

- The bank figure is not checked: the payouts export was not given, so what reached the bank is taken from the transactions export alone.

**The gap:** $471.77 less reached the bank in August than was placed in card orders in August. Nothing is missing — the bridge below closes to zero. The biggest pieces are card fees, two disputes, and money that was still on its way to the bank on 31 August.

## The bridge

| | USD |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| − Refunds processed in August | 58.06 |
| − Card fees | 141.44 |
| − Disputes: amount and fees | 165.17 and 30.00 |
| + Disputes won back | 83.66 |
| + Dispute fees returned | 15.00 |
| + Shopify adjustments | 0.35 |
| − Still in transit at month end | 271.90 |
| **= Paid out for August's card transactions** | **3,618.07** |
| + Paid out in August for earlier months' transactions | 95.79 |
| **= Paid out to the bank in August** | **3,713.86** |

Unexplained difference: 0.00. Paid out to the bank in August is the figure to check against your bank statement.

## Disputes

- Order #2015: 83.66 disputed, fee 15.00
- Order #2027: 81.51 disputed, fee 15.00

One of these was won back (Disputes won back and Dispute fees returned above), so the disputes' net cost for the month is 96.51.

## Still in transit at month end (arrives in September)

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

## July orders paid out in August

These July 31 sales landed in the 3 August payout, so they count in August's bank deposits:

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

## Split payments

Order #2051 was paid partly by gift card: of its 120.12 total, only the card part of 100.12 goes through payouts; the other 20.00 was the gift card and never reaches the bank.

No orders were paid outside Shopify Payments, and there are no unmatched orders or charges, no amount mismatches and no failed payouts.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.11.6, scripts 6e9e71a410d0

## Questions for you

The figures above use the usual answer until you confirm; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by payout-reconciliation v0.11.6 · seal adbef52f68b9
