<!-- numbers-0.6.0-claude-opus-5-5 / numbers-summary-c / with the plugin / run 1: passed -->

August 2026 went like this. The full version, which lists every order that was left out, is saved as `files/summary_2026-08.md`. That file is the one to send your accountant. Every figure in it came straight from the calculation and passed a check that looks for any number not taken from it. The version below is the same, except the 85 left-out orders are shown as a count.

---

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes VAT (£17,788.28) and the shipping customers paid (£2,915.10). The net after refunds still holds most of both, since refunds only gave some of it back. Neither figure is profit.

| Figure | Amount |
|---|---|
| Total charged | £106,722.52 |
| Refunds | £1,703.19 |
| Net after refunds | £105,019.33 |
| Orders counted | 1555 |
| Average order value | £68.63 |
| Refund rate | 1.6% |
| Units sold | 4918 |
| VAT inside the total | £17,788.28 |
| Shipping charged | £2,915.10 |
| Discounts given | £1,197.08 (200 orders had a discount) |

## Revenue as your store defines it

Revenue: **£86,504.99** (VAT excluded, shipping excluded, partial refunds as amount). After refunds: £85,085.66.

## Top products

By product revenue (line price x quantity, before order discounts, VAT included when prices include it):

1. Deluxe Gift Box: £8,295.00 (105 units)
2. Retinol Serum 30ml: £7,956.00 (221 units)
3. Peptide Serum 30ml: £6,840.00 (180 units)
4. Night Cream 50ml: £6,240.00 (208 units)
5. Day Moisturiser 50ml: £6,048.00 (216 units)

## What was left out

Of 1640 orders in the export for the month, 85 were left out. They were cancelled orders, test orders, and orders that were paid but not yet shipped. Every one is named in the saved file.

An order counts toward the month by its "Created at" date, as written in the export. Refunds are counted in the month of their order, so a refund made in August on a July order is not in these figures.

## How this was counted

Definitions:

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- a sale counts only once it is shipped; paid orders not yet shipped (pre-orders) are left out (your answer)
- revenue is reported without VAT (your answer)
- the shipping customers pay is kept out of revenue (your answer)
- a partial refund takes off only the amount refunded (your answer)
- a refund belongs to the month of its order (your answer)
- prices include VAT at 20% (your answer)

The export:

- the orders export has records on 31 of 31 days of August 2026
- the orders export's layout is not saved yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Files and version:

- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.6.0, scripts 7c2c32653639

## Question for you

- Are the payment methods, statuses, tags and currency listed under "How this was counted" all what you'd expect? If so, I'll save them as `store_shape.json`, and next month any new value will be flagged.

Until you confirm, the figures use the export as it is.

---

**For your accountant:**
- **Profit:** these are sales figures, not profit. The £86,504.99 revenue excludes VAT and shipping. Card fees and cost of goods aren't taken off.
- **Cross-check:** nothing here was checked against a source outside the export. If you have Shopify's own August total or a bank payout figure, I can compare against it.
- **Payouts:** I can reconcile August against your Shopify Payments payouts if you send that export.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes VAT (£17,788.28) and the shipping customers paid (£2,915.10); the net after refunds still holds most of both (refunds gave some back). Neither figure is profit.

| Figure | Amount |
|---|---|
| Total charged | £106,722.52 |
| Refunds | £1,703.19 |
| Net after refunds | £105,019.33 |
| Orders counted | 1555 |
| Average order value | £68.63 |
| Refund rate | 1.6% |
| Units sold | 4918 |
| VAT inside the total | £17,788.28 |
| Shipping charged | £2,915.10 |
| Discounts given | £1,197.08 (200 orders had a discount) |

## Revenue as your store defines it

Revenue: **£86,504.99** (VAT excluded, shipping excluded, partial refunds as amount). After refunds: £85,085.66.

## Top products

By product revenue (line price x quantity, before order discounts, VAT included when prices include it):

1. Deluxe Gift Box: £8,295.00 (105 units)
2. Retinol Serum 30ml: £7,956.00 (221 units)
3. Peptide Serum 30ml: £6,840.00 (180 units)
4. Night Cream 50ml: £6,240.00 (208 units)
5. Day Moisturiser 50ml: £6,048.00 (216 units)

## What was left out

Of 1640 orders in the export for the month, 85 were left out: cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449.

Orders are placed in the month by order Created at, as written in the export. Refunds are counted in the month of their order, so a refund made in August on a July order is not in these figures.

## How this was counted

Definitions:

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- a sale counts only once it is shipped; paid orders not yet shipped (pre-orders) are left out (your answer)
- revenue is reported without VAT (your answer)
- the shipping customers pay is kept out of revenue (your answer)
- a partial refund takes off only the amount refunded (your answer)
- a refund belongs to the month of its order (your answer)
- prices include VAT at 20% (your answer)

The export:

- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Files and version:

- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.6.0, scripts 7c2c32653639

## Question for you

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Until you confirm, the figures use the export as it is.

