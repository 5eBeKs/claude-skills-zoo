<!-- numbers-0.5.1-claude-opus-5-5 / numbers-summary-c / with the plugin / run 1: passed -->

# August 2026 sales summary

In August 2026 the store charged **£106,722.52** and had **£105,019.33** left after refunds. The total charged includes **£17,788.28 of VAT** and **£2,915.10 of shipping**. Refunds gave back only part of those, so the £105,019.33 still holds most of both. Neither figure is profit.

| | GBP |
|---|---:|
| Total charged (incl. VAT and shipping) | £106,722.52 |
| Refunds | £1,703.19 |
| Net after refunds | £105,019.33 |
| Orders counted | 1555 |
| Average order value | £68.63 |
| Refund rate | 1.6% |
| Units sold | 4918 |
| VAT inside the total | £17,788.28 |
| Shipping charged | £2,915.10 |
| Discounts given (200 orders had a discount) | £1,197.08 |

**Revenue under your store's rules:** £86,504.99 (VAT excluded, shipping excluded, partial refunds counted as the amount refunded). After refunds that is £85,085.66. This is probably the figure your accountant will want.

## Top products

These amounts are line price × quantity, before order discounts, with VAT included because your prices include it.

1. Deluxe Gift Box: £8295.00 (105 units)
2. Retinol Serum 30ml: £7956.00 (221 units)
3. Peptide Serum 30ml: £6840.00 (180 units)
4. Night Cream 50ml: £6240.00 (208 units)
5. Day Moisturiser 50ml: £6048.00 (216 units)

## Orders left out

85 of the 1640 orders in the export were left out. The reasons were: cancelled, test order (tagged "test"), test order (paid through the test gateway), and not shipped yet (mostly pre-orders). The full list with every order number is in the saved file below.

Orders are assigned to a month by their "Created at" date. Refunds count in the month of their order.

## How this was counted

These rules come from your `store_definitions.json`:
- Test orders (tagged "test" or paid through the test gateway) are left out.
- A sale counts only once it has shipped.
- Revenue is reported without VAT and without the shipping customers pay.
- A partial refund takes off only the amount refunded.
- A refund belongs to the month of its order.
- Prices include VAT at 20%.

About the data:
- The export has orders on all 31 days of August, so it looks complete.
- The figures were only checked for consistency within the export. Nothing from outside was used, such as a Shopify Analytics total or a bank figure. If you send one, I can compare them.
- Source file: `orders_export.csv` (9,074 rows, SHA-256 3035dcb90b8edd7c). Numbers computed by the shopify-month-end plugin, version 0.5.1.

## One question for you

This is the first time the export has been checked, so there is no record yet of which values are normal for your store. The export contains:
- **Payment statuses:** paid, partially refunded, refunded, voided
- **Fulfilment statuses:** fulfilled, unfulfilled
- **Currency:** GBP
- **Payment methods:** Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments
- **Tags:** pre-order, test

Is that everything you'd expect? If so, I'll save it as the baseline, and anything new next month (for example a new payment method) will be flagged. Until then, the figures use the export as it is.

The full summary, with every excluded order listed, is saved at `files/summary_2026-08.md`. Share that file with your accountant.

I only looked at August. The export also covers June and July, and I can do those too if you'd like.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes £17,788.28 of VAT and £2,915.10 of shipping. The amount left after refunds still holds most of both, because refunds gave only some of them back. Neither figure is profit.

| | GBP |
|---|---:|
| Total charged (incl. VAT and shipping) | £106,722.52 |
| Refunds | £1,703.19 |
| Net after refunds | £105,019.33 |
| Orders counted | 1555 |
| Average order value | £68.63 |
| Refund rate | 1.6% |
| Units sold | 4918 |
| VAT inside the total | £17,788.28 |
| Shipping charged | £2,915.10 |
| Discounts given (200 orders had a discount) | £1,197.08 |

**Revenue as your store defines it:** £86,504.99 (VAT excluded, shipping excluded, partial refunds as amount). After refunds that is £85,085.66.

## Top products

These figures are line price x quantity, before order discounts, VAT included when prices include it.

1. Deluxe Gift Box: £8295.00 (105 units)
2. Retinol Serum 30ml: £7956.00 (221 units)
3. Peptide Serum 30ml: £6840.00 (180 units)
4. Night Cream 50ml: £6240.00 (208 units)
5. Day Moisturiser 50ml: £6048.00 (216 units)

## What was left out

85 of the 1640 orders in the export were left out:

cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449

Orders are placed in a month by order Created at, as written in the export. Refunds are counted in the month of their order.

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
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.5.1, scripts f1930a1babf4

## Question for you

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Until you confirm this, the figures use the export as it is.

