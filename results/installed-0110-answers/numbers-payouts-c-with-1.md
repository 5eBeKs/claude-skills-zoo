Nothing is missing. The gap is refunds, fees, three disputes and money that was still on its way to the bank at 31 August. The full answer, with every order listed, is saved as `files/reconciliation_2026-08.md`. Here it is with the long lists shortened to counts:

---

# Where August's money went: Shopify Payments, August 2026

**Warning, read first:**

- The bank figure is not checked: the payouts export was not given, so what reached the bank is taken from the transactions export alone.

The bridge below closes: the unexplained difference is £0.00.

## The gap

Card orders placed in August came to £99,582.82, and £94,396.54 was paid out to the bank in August. That is a gap of **£5,186.28**. No money is missing: the gap is refunds, card fees, three disputes and money still in transit at 31 August, partly offset by July sales that were paid out in early August.

Separately, £11,918.00 of August orders was paid by PayPal or gift card. That money never goes through Shopify Payments, so don't look for it in the payouts. There are 180 of these orders, all listed in the file.

## The bridge

| | GBP |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | £99,582.82 |
| minus Refunds processed in August | -£2,762.41 |
| &nbsp;&nbsp;of which on orders from earlier months | £1,093.51 |
| minus Card fees | -£2,019.03 |
| minus Disputes: amount and fees (amount) | -£223.95 |
| minus Disputes: amount and fees (fees) | -£45.00 |
| Reserve held (-) or released (+) by Shopify | £0.00 |
| Failed payout paid again | £0.00 |
| Shopify adjustments | £2.35 |
| minus Still in transit at month end | -£6,075.32 |
| **= Paid out for August's card transactions** | **£88,472.41** |
| plus Paid out in August for earlier months' transactions | £5,924.13 |
| **= Paid out to the bank in August** | **£94,396.54** |

The last line is the figure to find on your bank statement. Shopify holds back no reserve (£0.00 still held at month end).

## Disputes

The disputes cost £268.95 in total. None has been won back yet.

- #32603: amount £41.95, fee £15.00
- #32955: amount £116.00, fee £15.00
- #33706: amount £66.00, fee £15.00

## Other details (full lists in the file)

- **Still in transit at 31 August:** 87 orders, paid out in early September starting 2026-09-01.
- **July transactions paid out in August:** 93, mostly in the 2026-08-03 payout.
- **Orders paid partly by gift card:** 36. Only the card part of each reaches the payouts.
- **Charges without a counted order:** #33431. This order was cancelled and refunded in full the next day, so it is not counted as a sale. Its charge and its refund are both in the payouts.
- There are no orders without a charge, no charge amount mismatches, no orders charged after month end and no failed payouts.

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
- computed by shopify-month-end v0.11.0, scripts a07884a2bdbf

The bank figure comes from the transactions export alone. To check it payout by payout, send the payouts export (Finances > Payouts > Export).

## Open question for you

Until you confirm this, the figures above use the usual answer. A different answer would change them.

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by payout-reconciliation v0.11.0 · seal 8d7d151acc22

---

To confirm this against the bank, check that your statement shows £94,396.54 from Shopify in August. Also send the payouts export if you can, so I can check the figure payout by payout. Tell me whether the payment methods, statuses and tags listed above look right, and I'll record them so any new one gets flagged next month.
