<!-- numbers-0.5.1-claude-opus-5-5 / numbers-summary-c / with the plugin / run 3: passed -->

# Sales summary: August 2026

In August the store charged **£106,722.52** and had **£105,019.33** left after refunds. That total includes £17,788.28 of VAT and £2,915.10 of shipping that customers paid. The figure after refunds still contains most of both (refunds gave some back), so neither number is profit. The VAT is owed to HMRC, and nothing has been taken off yet for shipping, product costs or fees.

| Figure | August 2026 |
|---|---|
| Total charged (incl. VAT and shipping) | £106,722.52 |
| Refunds | £1,703.19 |
| Net after refunds | £105,019.33 |
| Orders counted | 1555 |
| Average order value | £68.63 |
| Refund rate | 1.6% |
| Units sold | 4918 |
| VAT inside the total | £17,788.28 |
| Shipping charged | £2,915.10 |
| Discounts given | £1,197.08 |

200 orders had a discount, and 45 orders had a refund.

## Revenue as your store defines it

**Revenue is £86,504.99.** That's without VAT and without shipping, and a partial refund takes off only the amount refunded. After refunds it is £85,085.66.

## Top products

These are ranked by line price × quantity, before order discounts. Because your prices include VAT, these amounts do too.

1. Deluxe Gift Box: £8,295 (105 units)
2. Retinol Serum 30ml: £7,956 (221 units)
3. Peptide Serum 30ml: £6,840 (180 units)
4. Night Cream 50ml: £6,240 (208 units)
5. Day Moisturiser 50ml: £6,048 (216 units)

## What was left out

**85 orders are left out of every figure above.** The reasons are cancelled orders, test orders (tagged "test" or paid through the test gateway), and orders not shipped yet (pre-orders). Every order number is listed by reason in the saved file.

An order belongs to August if its "Created at" date in the export is in August. A refund counts in the month of its order, not the month the refund was made.

## How this was counted

These rules are the answers in your `store_definitions.json`:
- Test orders are left out of sales.
- A sale counts only once it has shipped. Paid orders that haven't shipped yet (pre-orders) are left out.
- Revenue is reported without VAT.
- The shipping customers pay is kept out of revenue.
- A partial refund takes off only the amount refunded.
- A refund belongs to the month of its order.
- Prices include VAT at 20%.

About the export:
- It has records on all 31 days of August 2026.
- Its shape (the statuses, payment methods and tags that normally appear) hasn't been recorded yet. It contains:
  - **Financial status:** paid, partially_refunded, refunded, voided
  - **Fulfillment status:** fulfilled, unfulfilled
  - **Currency:** GBP
  - **Payment method:** Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments
  - **Tags:** pre-order, test
- The figures were checked against nothing outside the export. A total from Shopify or your bank would let me cross-check them.

Files used:
- `orders_export.csv`: 9,074 rows, SHA-256 3035dcb90b8edd7c
- `store_definitions.json`: 36 rows, SHA-256 c370f6ea8162b60d
- Computed by shopify-month-end v0.5.1, scripts f1930a1babf4

## Question for you

The figures use the usual answer until you confirm:
- **Is that list under "How this was counted" what you'd expect to see?** If you confirm it, I'll save it as `store_shape.json`, and anything new that turns up next month will be flagged.

---

I saved the full summary, with every left-out order numbered, as **`files/summary_2026-08.md`**. That's the version to send your accountant.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes £17,788.28 of VAT and £2,915.10 of shipping paid by customers. The net after refunds still holds most of both (refunds gave some back), so neither figure is profit: the VAT is owed to HMRC, and shipping, product costs and fees have not been taken off.

| Figure | 2026-08 |
|---|---|
| Total charged (incl. VAT and shipping) | £106,722.52 |
| Refunds | £1,703.19 |
| Net after refunds | £105,019.33 |
| Orders counted | 1555 |
| Average order value | £68.63 |
| Refund rate | 1.6% |
| Units sold | 4918 |
| VAT inside the total | £17,788.28 |
| Shipping charged | £2,915.10 |
| Discounts given | £1,197.08 |

200 orders had a discount, and 45 orders had a refund.

## Revenue as your store defines it

Revenue: **£86,504.99** (VAT excluded, shipping excluded, partial refunds as amount). After refunds: £85,085.66.

## Top products

By revenue (line price x quantity, before order discounts, VAT included when prices include it):

1. Deluxe Gift Box: £8,295 (105 units)
2. Retinol Serum 30ml: £7,956 (221 units)
3. Peptide Serum 30ml: £6,840 (180 units)
4. Night Cream 50ml: £6,240 (208 units)
5. Day Moisturiser 50ml: £6,048 (216 units)

## What was left out

85 orders were left out of every figure above: cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449

Orders are placed in a month by order Created at, as written in the export. Refunds are counted in the month of their order, not the month the refund was made.

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
- computed by shopify-month-end v0.5.1, scripts f1930a1babf4

## Question for you

The figures above use the usual answer until you confirm it:

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

