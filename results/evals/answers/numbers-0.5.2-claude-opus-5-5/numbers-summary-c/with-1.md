<!-- numbers-0.5.2-claude-opus-5-5 / numbers-summary-c / with the plugin / run 1: passed -->

# August 2026 sales summary

I've saved the full summary as `files/summary_2026-08.md`, including the complete list of orders that were left out. That file is the version to give your accountant. Every figure below comes from the calculation script, and a separate check confirmed that each one traces back to the data.

In August the store charged **£106,722.52** and had **£105,019.33** left after refunds. That total includes £17,788.28 of VAT and £2,915.10 of shipping. Refunds only gave back a small part of those, so most of both is still in the £105,019.33. **Neither figure is profit.**

| | |
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

**Revenue under your store's definition:** £86,504.99. This excludes VAT and shipping, and a partial refund takes off only the amount refunded. After refunds it is **£85,085.66**. Your accountant most likely wants this figure.

## Top products
These figures are line price × quantity, before order discounts, with VAT included.
1. Deluxe Gift Box: 105 units, £8,295.00
2. Retinol Serum 30ml: 221 units, £7,956.00
3. Peptide Serum 30ml: 180 units, £6,840.00
4. Night Cream 50ml: 208 units, £6,240.00
5. Day Moisturiser 50ml: 216 units, £6,048.00

## What was left out
The export has 1640 August orders, and **85 were left out**:
- **Cancelled:** #32854, #32993, #33276, #33356, #33431, #33443, #33631
- **Test orders (test payment gateway):** #32872, #33456, #33634, #34406
- **Test orders (tagged "test"):** #32917, #33065, #33415, #33420
- **Not shipped yet:** the rest (mostly pre-orders). Your rule is that a sale counts only once it ships. All of their order numbers are in the saved file.

Each order counts in the month it was created. Refunds count in the month of their order, not the month the money went back.

## How this was counted
All of these rules are the ones you set in `store_definitions.json`:
- Test orders (tagged "test" or paid through the test gateway) are left out.
- A sale counts only once it has shipped.
- Revenue is reported without VAT; prices include VAT at 20%.
- Shipping that customers pay is kept out of revenue.
- A partial refund takes off only the amount refunded.
- A refund belongs to the month of its order.

The export has records on all 31 days of August, so nothing looks cut off. I haven't checked these figures against anything outside the export. If you give me a total from Shopify Analytics or a bank statement, I can check them against it.

## One question for you
This is the first run, so the export's layout hasn't been recorded yet. **Are all of these values what you'd expect?**
- **Financial status:** paid, partially_refunded, refunded, voided
- **Fulfilment status:** fulfilled, unfulfilled
- **Currency:** GBP
- **Payment methods:** Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments
- **Tags:** pre-order, test

If you say yes, I'll record them, and anything new in September's export will be flagged. Until then, these figures assume they're all as expected.

This summary is sales only. If your accountant also needs to know why the Shopify Payments payouts don't match these sales (card fees, payouts still on the way), I can reconcile that from a payout transactions export.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes £17,788.28 of VAT and £2,915.10 of shipping. The net after refunds still holds most of both, because refunds only returned part of them. Neither figure is profit.

| | |
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

**Revenue as your store defines it:** £86,504.99 (VAT excluded, shipping excluded, partial refunds as amount). After refunds it is £85,085.66.

## Top products

These figures are line price x quantity, before order discounts, VAT included when prices include it.

1. Deluxe Gift Box: 105 units, £8,295.00
2. Retinol Serum 30ml: 221 units, £7,956.00
3. Peptide Serum 30ml: 180 units, £6,840.00
4. Night Cream 50ml: 208 units, £6,240.00
5. Day Moisturiser 50ml: 216 units, £6,048.00

## What was left out

Of 1640 orders in the export for the month, 85 were left out: cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449.

Orders are assigned to a month by order Created at, as written in the export. Refunds are counted in the month of their order.

## How this was counted

These are the definitions behind every figure above:

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- a sale counts only once it is shipped; paid orders not yet shipped (pre-orders) are left out (your answer)
- revenue is reported without VAT (your answer)
- the shipping customers pay is kept out of revenue (your answer)
- a partial refund takes off only the amount refunded (your answer)
- a refund belongs to the month of its order (your answer)
- prices include VAT at 20% (your answer)

What the figures were computed from:

- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.5.2, scripts ae0423f29e4e

## Question for you

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Until you confirm this, the figures use the usual answer.

