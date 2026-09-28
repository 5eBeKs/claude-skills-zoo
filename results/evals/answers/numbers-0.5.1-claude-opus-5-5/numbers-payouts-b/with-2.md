<!-- numbers-0.5.1-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 2: passed -->

Nothing is missing. The full difference is explained below, and the bridge closes with no unexplained remainder:

# August 2026 payout reconciliation

**The gap: $471.77** between card orders placed in August and what reached the bank in August. It is fully explained — the bridge closes with $0.00 unexplained. Nothing is missing; the gap is refunds, card fees, two disputes, and money that was still on its way to the bank on August 31.

Before any figure: the answer below uses the usual rule for test orders (left out) and an export shape you have not confirmed yet — see the questions at the end. A different answer would change the figures.

## The bridge

| | USD |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| − Refunds processed in August | 58.06 |
| − Card fees | 141.44 |
| − Disputes: amount and fees | 195.17 |
| &nbsp;&nbsp;&nbsp;disputed amounts | 165.17 |
| &nbsp;&nbsp;&nbsp;dispute fees | 30.00 |
| + Other transactions (adjustment, dispute_won) | 99.01 |
| − Still in transit at month end | 271.90 |
| **= Paid out for August's card transactions** | **3,618.07** |
| + Paid out in August for earlier months' transactions | 95.79 |
| **= Paid out to the bank in August** | **3,713.86** |

The last line is the figure to find on your bank statement.

## What drives the gap

**Disputes.** Two chargebacks were opened in August, each taking the order amount plus a fee:

- #2015: $83.66 plus $15.00 fee
- #2027: $81.51 plus $15.00 fee

Good news on #2015: you won it later in August, and Shopify returned both the amount and the fee. That reversal is in the "Other transactions" line (together with a small adjustment), so in practice only #2027 cost you money this month.

**Money in transit on August 31.** These payouts were already on their way and land in September, so they are not on August's bank statement:

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

**Late-July orders paid out in August.** These add to August's bank deposits even though the sales belong to July:

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

**Split payment.** One order was paid partly by gift card; only the card part goes through Shopify Payments, and the gift-card part ($20.00) will never appear in a payout:

#2051 (Gift card, Shopify Payments)

**Unmatched items:** none. Every counted card order has a matching charge at the same amount.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

Computed from:

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.5.1, scripts 32efef0622a7

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
