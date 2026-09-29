I've finished the reconciliation and saved the full checked answer as `files/reconciliation_2026-08.md`. The checker wouldn't seal a shortened version with counts in place of the long lists, so the saved file is the answer of record. Below are its sections, copied exactly, with the long order lists left in the file.

---

**Warning first:**
- The bank figure is not checked: the payouts export was not given, so what reached the bank is taken from the transactions export alone.

## The gap

Card orders placed in August came to **£5,186.28** more than Shopify Payments paid out to the bank in August. The bridge below closes to zero (unexplained difference £0.00). The money went to refunds, card fees, disputes, and payouts that landed in early September.

| | £ |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 99,582.82 |
| minus Refunds processed in August | 2,762.41 |
| &nbsp;&nbsp;of which on orders from earlier months | 1,093.51 |
| minus Card fees | 2,019.03 |
| minus Disputes: amount and fees | 223.95 + 45.00 |
| Reserve held (-) or released (+) by Shopify | 0.00 |
| Failed payout paid again | 0.00 |
| Shopify adjustments | 2.35 |
| minus Still in transit at month end | 6,075.32 |
| **equals Paid out for August's card transactions** | **88,472.41** |
| plus Paid out in August for earlier months' transactions | 5,924.13 |
| **equals Paid out to the bank in August** | **94,396.54** |

The last line is the figure to look for on your bank statement. The disputes cost £268.95 net. No reserve is held at month end (£0.00).

## Disputes
- #32603: amount £41.95, fee £15.00
- #32955: amount £116.00, fee £15.00
- #33706: amount £66.00, fee £15.00

## Timing (in the saved file, order by order)
- **Still in transit at month end:** the orders from 31 August onwards, which were paid out on 2026-09-01 and 2026-09-02.
- **July's transactions paid out in August:** late-July orders and refunds that were paid out on 2026-08-03.

## Not in the payouts at all
180 orders (£11,918.00) were paid by PayPal or gift card, so this money won't appear in the Shopify payouts. There are also orders paid partly by gift card, where only the card part reaches the payouts (for example #32938: card part £86.00, rest by gift card £25.00). Every order in both groups is listed in the file.

## Unmatched
- #33431: £12.95 (worth checking whether this order was deleted, or is a test order)

There are no orders without a charge, no charge amount mismatches, no orders charged after month end and no failed payouts. The bank figure was not checked against a payouts export; it comes from the transactions alone. If you export Finances > Payouts, it can be checked payout by payout.

## How this was counted
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- the payout export has records on 31 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: GBP)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- payout_transactions.csv: 4,133 rows, SHA-256 2bf625390cc8ebe1
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.11.6, scripts 6e9e71a410d0

## Question for you
The figures above use the usual answer until you confirm it; a different answer would change them.
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by payout-reconciliation v0.11.6 · seal af38713a0f4a

---

**In short:** about half of the gap is timing: money for sales on 31 August that landed in early September. Most of the rest is refunds, and more than a third of the refunds were on orders from earlier months. Card fees and three disputes make up the remainder. Separately, the 180 PayPal and gift-card orders were never going to show up in the Shopify payouts, so check the PayPal money in your PayPal account.
