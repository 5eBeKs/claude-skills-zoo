Nothing is missing from your August payouts. The reconciliation below accounts for every dollar of the $471.77 gap, with nothing left unexplained. Most of it is money for orders placed on August 29–31 that is still on its way to your bank ($271.90), plus card fees ($141.44) and two disputes. One caveat: I only had the transactions export, so the bank figure hasn't been checked against the payouts export (Finances > Payouts > Export). If you send that file, I can check each payout against what reached the bank.

---

# August 2026: card sales vs. payouts

**Warning, read first:**

- The bank figure is not checked: the payouts export was not given, so what reached the bank is taken from the transactions export alone.

Card orders placed in August came to $4,185.63, but $3,713.86 was paid out to the bank in August: a gap of **$471.77**. The bridge below closes with an unexplained difference of $0.00. Nothing is missing: the gap is refunds, card fees, two disputes, and money for late-August orders still in transit to the bank, partly offset by late-July orders paid out in August.

## The bridge

| | Amount |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | $4,185.63 |
| − Refunds processed in August | $58.06 |
| − Card fees | $141.44 |
| − Disputes: amount and fees | $165.17 and $30.00 |
| + Disputes won back | $83.66 |
| + Dispute fees returned | $15.00 |
| Reserve held (-) or released (+) by Shopify | $0.00 (still held at month end: $0.00) |
| Failed payout paid again | $0.00 |
| Shopify adjustments | $0.35 |
| − Still in transit at month end | $271.90 |
| **= Paid out for August's card transactions** | **$3,618.07** |
| + Paid out in August for earlier months' transactions | $95.79 |
| **= Paid out to the bank in August** | **$3,713.86** |

The last line is the figure to find on your bank statement for August.

The disputes' net cost is $96.51.

## Disputes

- Order #2015: amount $83.66, fee $15.00
- Order #2027: amount $81.51, fee $15.00

## Still in transit at month end (arrives in September)

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

## July orders paid out in August

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

## Other items

- Unmatched: no orders without a charge, no charges without a counted order, no charge amount mismatches, and no orders charged after month end.
- Orders paid partly another way: order #2051 (Gift card, Shopify Payments), order total $120.12, of which the card part $100.12 went through Shopify Payments and the other part $20.00 did not, so it never appears in payouts.
- No failed payouts. The bank figure was not checked against a payouts export; it comes from the transactions alone.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- the payout export has records on 26 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: USD)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- payout_transactions.csv: 76 rows, SHA-256 48b34f56e559c4a7
- computed by shopify-month-end v0.11.0, scripts a07884a2bdbf

## Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by payout-reconciliation v0.11.0 · seal 91222cc1d785

---

This is also saved as `reconciliation.md` in your working folder. If you confirm the two questions above, next month's exports will flag any new payment method, status or payout type.
