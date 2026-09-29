**The gap: £5,186.28** between card orders placed in August and what Shopify Payments paid out to the bank in August. The bridge below explains all of it; the unexplained difference is £0.00.

**Warning, read first:**

- The bank figure is not checked: the payouts export was not given, so what reached the bank is taken from the transactions export alone.

| | GBP |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 99,582.82 |
| − Refunds processed in August | 2,762.41 |
| &nbsp;&nbsp;of which on orders from earlier months | 1,093.51 |
| − Card fees | 2,019.03 |
| − Disputes: amount and fees | 223.95 + 45.00 |
| Shopify adjustments | 2.35 |
| − Still in transit at month end | 6,075.32 |
| **= Paid out for August's card transactions** | **88,472.41** |
| + Paid out in August for earlier months' transactions | 5,924.13 |
| **= Paid out to the bank in August** | **94,396.54** |

Shopify held no reserve and no payout failed. The last line is the figure to look for on your bank statement for August.

**Where the money went:**
- **Refunds:** money paid back to customers, some of it on orders placed before August.
- **Card fees:** Shopify Payments' processing fee on each charge.
- **Disputes (chargebacks):** three customers disputed a charge; each returned the amount to the customer and cost a fee. Their net cost is £268.95.
  - #32603: amount £41.95, fee £15.00
  - #32955: amount £116.00, fee £15.00
  - #33706: amount £66.00, fee £15.00
- **Timing:** 87 orders from the last days of August were still in transit at month end and paid out on 1–2 September. In the other direction, 93 transactions from the end of July were paid out on 3 August. The two partly offset.

**Not in the payouts at all:** 180 orders were paid by PayPal or gift card. Orders paid outside Shopify Payments total £11,918.00; that money never goes through Shopify Payments, so do not look for it in the payouts. Another 36 orders were paid partly by gift card and partly by card; only the card part reaches the payouts.

**Unmatched:** a charge in the payouts with no counted August order: #33431. It may be a test order or an order left out of sales.

**How this was counted:**

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)

- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- the payout export has records on 31 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: GBP)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- payout_transactions.csv: 4,133 rows, SHA-256 2bf625390cc8ebe1
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.11.0, scripts a07884a2bdbf

**Question for you** (the figures above use the usual answer until you confirm it; a different answer would change them):

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

The full list of every order is in `files/reconciliation_2026-08.md`.

---

The full report with every order listed is saved as `files/reconciliation_2026-08.md`. It passed the number check and ends with `Checked by payout-reconciliation v0.11.0 · seal 4fc43cc20e41`. The summary above uses the same wording and figures, with the long lists shown as counts.

Two corrections to what I said before:
- **No lists are repeated in the report.** I was wrong: the "duplicate" was my own mistake when viewing the file.
- **The split-payment list still gives only order numbers.** It doesn't show how much of each order went on the card and how much on the gift card, although I have those amounts.
