<!-- numbers-0.5.1-claude-opus-5-5 / numbers-payouts-b / with the plugin / run 1: passed -->

The gap is $471.77, and all of it is accounted for. Card fees, two chargebacks and money still on its way to the bank explain most of it. The bridge closes with $0.00 left unexplained, and every figure below was checked against the calculation.

# August 2026: card sales vs. payouts

**The gap is $471.77.** That's the difference between card orders placed in August and what Shopify Payments paid to the bank in August. The bridge below accounts for all of it (unexplained difference: $0.00).

In short, there are three main reasons:
- **Two chargebacks** cost $195.17, counting the disputed amounts and the fees.
- **Card fees** were $141.44.
- **Money still in transit** at month end: $271.90 lands in the first days of September.

Refunds took off another $58.06. Two things partly offset the gap: adjustments and won disputes added $99.01, and July's late sales paid out in August added $95.79.

## The bridge

| | USD |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 4,185.63 |
| − Refunds processed in August | 58.06 |
| − Card fees | 141.44 |
| − Disputes: amount and fees | 165.17 + 30.00 = 195.17 |
| + Other transactions (adjustment, dispute_won) | 99.01 |
| − Still in transit at month end | 271.90 |
| **= Paid out for August's card transactions** | **3,618.07** |
| + Paid out in August for earlier months' transactions | 95.79 |
| **= Paid out to the bank in August** | **3,713.86** |

The last line is the figure that should appear on your bank statement for August. Please check it against the bank.

## Disputes (chargebacks)

| Order | Amount | Dispute fee |
|---|---:|---:|
| #2015 | 83.66 | 15.00 |
| #2027 | 81.51 | 15.00 |

The payouts also include `dispute_won` and `adjustment` transactions. These are counted in the "Other transactions" line, which added money back.

## Still in transit at month end (arrives in September)

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

## July orders paid out in August

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

## Other payment methods and unmatched items

- Order #2051 was paid partly with a gift card. Only the card part ($100.12) goes through Shopify Payments. The gift-card part of $20.00 will never show up in a payout, so don't look for it there.
- Orders with no matching card charge: 0. Charges with no counted order: 0. Charges whose amount differs from the order: 0.

## Open questions (the figures above assume the usual answer)

These figures use the usual answer to each question below. If your answer is different, the figures will change.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

The export includes orders paid through "Bogus Gateway (for testing)", so the first question affects these figures.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.5.1, scripts 32efef0622a7
