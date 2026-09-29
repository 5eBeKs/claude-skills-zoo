Here's the August summary. I've also saved it as `files/summary_2026-08.md` so you can send it to your accountant. The figures follow the counting rules already in your `store_definitions.json`. One thing to know first: nothing here has been checked against Shopify's own totals or your bank, so a total from either would be a useful cross-check. There's one question for you at the end.

---

# 2026-08 sales summary

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes VAT (£17,788.28) and shipping (£2,915.10); the net after refunds still holds most of both (refunds gave some back). Neither figure is profit.

| Figure | 2026-08 |
|---|---|
| Total charged | £106,722.52 |
| Refunds | £1,703.19 |
| Net after refunds | £105,019.33 |
| Orders counted | 1555 |
| Refunded orders | 17 |
| Average order value | £68.63 |
| Refund rate | 1.6% |
| Units sold | 4918 |
| VAT inside the total | £17,788.28 |
| Shipping charged | £2,915.10 |
| Discounts given | £1,197.08 |

200 orders had a discount.

**Revenue as the store defines it:** £86,504.99 (VAT excluded, shipping excluded, partial refunds as amount).

## Top products

By revenue (line price x quantity, before order discounts, VAT included when prices include it):

1. Deluxe Gift Box: £8,295.00
2. Retinol Serum 30ml: £7,956.00
3. Peptide Serum 30ml: £6,840.00
4. Night Cream 50ml: £6,240.00
5. Day Moisturiser 50ml: £6,048.00

## What was left out

85 orders were left out: cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449.

Months are assigned by order Created at, as written in the export; refunds are counted in the month of their order.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- a sale counts only once it is shipped; paid orders not yet shipped (pre-orders) are left out (your answer)
- revenue is reported without VAT (your answer)
- the shipping customers pay is kept out of revenue (your answer)
- a partial refund takes off only the amount refunded (your answer)
- a refund belongs to the month of its order (your answer)
- prices include VAT at 20% (your answer)

- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- Subtotal in this export is before discounts (200 orders)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.11.6, scripts ab61cfedc85c

## Question for you

The figures above use the usual answer until you confirm:

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-monthly-summary v0.11.6 · seal a032ac347b1b

---

This covers August only. Your accountant may also want to know how much actually reached the bank. That needs your Shopify Payments payouts export for August, which isn't in the folder. If you add it, I can match it against these sales and show where refunds and card fees account for the gap.
