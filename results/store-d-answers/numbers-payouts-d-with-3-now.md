In June, $572,456.23 from Shopify reached the bank, against $691,562.27 of card orders. Most of the $119,106.04 gap is money still in transit (paid out in early July), June's refunds and card fees. The rest is disputes, offset by early-June payouts of sales made before June.

A payout of $18,132.40 on 30 June failed and was not paid again in June; please check that it arrived in July. Separately, orders paid through PayPal, cash and other methods never go through Shopify Payments, so they aren't in the payouts. Below is the checked report. Four long order lists are in the saved file `files/reconciliation_2026-06.md`: they list in-transit orders, orders paid outside Shopify Payments, and two kinds of unmatched charges.

# Shopify Payments payout reconciliation: June 2026

**Warning, read first:**

- 105011.68 of the bank figure is taken from the payouts export for payouts that carry transactions from before the transactions export starts (2026-06-01): that part is not checked transaction by transaction.

## The gap

Card orders placed in June came to $691,562.27. Shopify paid $572,456.23 to the bank in June. The gap is $119,106.04. The bridge below closes: the unexplained difference is $0.00.

## Bridge

| | USD |
|---|---:|
| Card orders placed in June (Shopify Payments, shipped yet or not) | 691,562.27 |
| − Refunds processed in June | 82,726.47 |
| &nbsp;&nbsp;of which on orders from earlier months | 45,616.95 |
| − Card fees | 25,967.07 |
| − Disputes: amount and fees | 1,212.93 + 240.00 |
| Reserve held (-) or released (+) by Shopify | 0.00 (still held at month end: 0.00) |
| Failed payout paid again | 0.00 |
| Shopify adjustments | 0.00 |
| − Still in transit at month end | 117,366.90 |
| **= Paid out for June's card transactions** | **467,444.55** |
| + Paid out in June for transactions before the transactions export starts | 105,011.68 |
| **= Paid out to the bank in June** | **572,456.23** |

The last line is the figure to check against the bank statement.

The disputes' net cost is $1,452.93.

Payouts in early June that carry transactions from before the transactions export starts (June 1):

| Payout date | Payout total | In transactions export | Before it |
|---|---:|---:|---:|
| 2026-06-04 | 18,603.09 | 12,736.09 | 5,867.00 |
| 2026-06-03 | 60,256.61 | 0.00 | 60,256.61 |
| 2026-06-02 | 21,209.54 | 0.00 | 21,209.54 |
| 2026-06-01 | 17,678.53 | 0.00 | 17,678.53 |

## Disputes

| Order | Amount | Fee |
|---|---:|---:|
| #45476 | 82.80 | 15.00 |
| #43139 | 202.09 | 15.00 |
| #42339 | 19.60 | 15.00 |
| #46132 | 99.94 | 15.00 |
| #48748 | 34.95 | 15.00 |
| #50960 | 85.00 | 15.00 |
| #46564 | 34.95 | 15.00 |
| #46016 | 85.96 | 15.00 |
| #47881 | 32.15 | 15.00 |
| #48462 | 191.89 | 15.00 |
| #43365 | 70.95 | 15.00 |
| #47863 | 71.86 | 15.00 |
| #42377 | 32.81 | 15.00 |
| #46314 | 52.58 | 15.00 |
| #43148 | 45.39 | 15.00 |
| #43258 | 70.01 | 15.00 |

## Failed payout

- Payout of 2026-06-30: $18,132.40 failed and was not paid again in June (failed payout paid again: $0.00).

The bank figure was checked against the payouts export (bank checked: True).

## Paid outside Shopify Payments (not in payouts at all)

These orders were paid through PayPal, manual, bank deposit, cash, gift card and similar methods, so this money never appears in the Shopify payouts. They total $82,635.67:

*(Full order list in `files/reconciliation_2026-06.md`.)*

## Split payments (gift card + card)

Only the card part reaches the payouts:

*(Every order, with its card part and the rest, is in `files/reconciliation_2026-06.md`.)*

## Still in transit at month end

These were paid out in July, with the payout dates shown:

*(Full order list with payout dates in `files/reconciliation_2026-06.md`.)*

## Unmatched items

Charged after the month ended (charged in July):

| Order | Order total | Charged in June | Charged after month end | Date |
|---|---:|---:|---:|---|
| #55864 | 75.52 | 0.00 | 75.52 | 2026-07-01 |
| #55838 | 52.85 | 0.00 | 52.85 | 2026-07-01 |
| #55835 | 82.80 | 0.00 | 82.80 | 2026-07-02 |
| #55667 | 196.73 | 0.00 | 196.73 | 2026-07-03 |
| #55378 | 98.00 | 0.00 | 98.00 | 2026-07-01 |

Charges with no counted June order:

*(Listed in `files/reconciliation_2026-06.md`.)*

Charge amount differs from order total:

*(Listed in `files/reconciliation_2026-06.md`.)*

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 30 of 30 days of June 2026
- the orders export's shape is not recorded yet (financial status: authorized, expired, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: USD; payment method: (for testing) Bogus Gateway, Bank Deposit, Cash, Cash on Delivery (COD), Gift Card, PayPal Express Checkout, Shopify Payments, manual; tags: Net 15, Net 30, Subscription, Subscription First Order, Subscription Recurring Order, replacement, test, wholesale)
- the payout export has records on 30 of 30 days of June 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_reversal, payout_failure, refund, reserve; payout status: failed, in_transit, paid, scheduled; currency: USD)
- checked against the payouts export: 20 payouts paid in June 2026, 572456.23
- the transactions export starts on 2026-06-01; the payouts of 2026-06-04, 2026-06-03, 2026-06-02, 2026-06-01 carry 105011.68 of transactions from before it, shown as their own line
- paid out in month: matches the figure in the payouts export (572456.23; computed 572456.23)

- orders_export.csv: 58,166 rows, SHA-256 4c14bc07ab3d150c
- payment_transactions_export.csv: 32,249 rows, SHA-256 a6932219963161c3
- payouts_export.csv: 68 rows, SHA-256 cc95fc92640b4c98
- computed by shopify-month-end v0.10.1, scripts cb3ded1855e9

## Open questions for you

The figures above use the usual answer until you confirm it. A different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-month-end v0.10.1 · seal bc7e0ea5b956

---

*After this answer the plugin's own answer check ended the turn with:* Month-end check: the answer above did not pass the check against the computed results (against the checked answer: missing: '#55844' 124.20 (in the checked answer, not in this one); missing: '#55844' 99.20 (in the checked answer, not in this one); missing: '#55844' 25.00 (in the checked answer, not in this one); missing: '#55772' 106.00 (in the checked answer, not in this one); missing: '#55772' 81.00 (in the checked answer, not in this one); missing: '#55772' 25.00 (in the checked answer, not in this one); missing: '#55670' 146.00 (in the checked answer, not in this one); missing: '#55670' 46.00 (in the checked answer, not in this one)). Ask for the checked answer before using these figures.
