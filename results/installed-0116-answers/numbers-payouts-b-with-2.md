Your August payout isn't missing money. The $471.77 gap is fully explained by refunds, card fees, two disputes and timing, and nothing is left unexplained. I haven't checked the bank figure against a payouts export yet (see the first point below). This is the checked reconciliation:

---

# August 2026 payout reconciliation

**Before the figures:**

- The bank figure is not checked: the payouts export was not given, so what reached the bank is taken from the transactions export alone.

## The gap

Card orders placed in August came to $4,185.63, and $3,713.86 was paid out to the bank in August. That is a gap of **$471.77**. The bridge below explains all of it: the unexplained difference is $0.00.

In short, the gap is refunds, card fees, two disputes (one of them won back), and money from the last days of August that was still on its way to the bank at month end. It is partly offset by late-July sales that landed in August.

## The bridge

| | Amount |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | $4,185.63 |
| − Refunds processed in August | $58.06 |
| − Card fees | $141.44 |
| − Disputes: amount and fees | $165.17 and $30.00 |
| + Disputes won back | $83.66 |
| + Dispute fees returned | $15.00 |
| + Shopify adjustments | $0.35 |
| − Still in transit at month end | $271.90 |
| **= Paid out for August's card transactions** | **$3,618.07** |
| + Paid out in August for earlier months' transactions | $95.79 |
| **= Paid out to the bank in August** | **$3,713.86** |

The last line is the figure your bank statement should show for Shopify Payments deposits in August. Please check it against the bank.

No reserve was held or released, and no payouts failed.

## Disputes

- Order #2015: $83.66 disputed, fee $15.00
- Order #2027: $81.51 disputed, fee $15.00

One dispute was won, so $83.66 came back along with $15.00 in fees. The net cost of disputes in August was $96.51.

## Money still in transit at month end

These amounts were paid out in early September, not August:

#2052 (2026-09-01), #2067 (2026-09-01), #2066 (2026-09-02)

## July orders paid out in August

These July 31 sales reached the bank in August:

#1998 (2026-08-03), #1999 (2026-08-03), #2000 (2026-08-03)

## Orders paid partly another way

Only the card part of these reaches the payouts. The gift card part never shows up there:

#2051 (Gift card, Shopify Payments)

## Unmatched items

None. Every counted card order has a matching charge at the right amount, and every charge matches a counted order. No orders were paid entirely outside Shopify Payments.

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

The figures above use the usual answer to each question until you confirm it. A different answer would change them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by payout-reconciliation v0.11.6 · seal e325cd2f0d26

---

I saved this as `reconciliation.md` in your working folder. To check the bank figure payout by payout, export Finances > Payouts > Export from Shopify and I'll run it again with that file.
