<!-- numbers-0.5.2-claude-opus-5-5 / numbers-summary-c / with the plugin / run 3: passed -->

August sold **£106,722.52** in total. After £1,703.19 of refunds, **£105,019.33** was left. Neither figure is profit, because both still include VAT and shipping. The full summary is saved as `files/summary_2026-08.md` for your accountant, and every figure in it was checked against the calculation.

**August 2026 (GBP)**

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

**Revenue as you define it** (without VAT or shipping; a partial refund takes off only the amount refunded): **£86,504.99**, or **£85,085.66** after refunds. This is probably the number your accountant wants.

**Top products:** these figures include VAT and come before order discounts.
1. Deluxe Gift Box: £8,295.00 (105 units)
2. Retinol Serum 30ml: £7,956.00 (221 units)
3. Peptide Serum 30ml: £6,840.00 (180 units)
4. Night Cream 50ml: £6,240.00 (208 units)
5. Day Moisturiser 50ml: £6,048.00 (216 units)

**Left out:** 85 of the 1640 August orders in the export aren't counted. They are cancelled orders, test orders (tagged "test" or paid through the test gateway) and paid orders that haven't shipped yet, such as pre-orders. The saved file lists each order number. An order belongs to the month it was created in. A refund is counted in its order's month, so a refund made in September on an August order is included here.

**How this was counted:**
- Everything follows the answers in your `store_definitions.json`: test orders are left out, a sale counts once it ships, revenue excludes VAT (20%) and shipping, and refunds belong to their order's month.
- The export has records on all 31 days of August, so nothing looks cut off.
- The figures haven't been checked against anything outside the export. If you give me a total from Shopify or your bank for August, I can compare them.

**One question for you:** these are the values the export contains:
- **Order statuses:** paid, partially_refunded, refunded, voided
- **Shipping statuses:** fulfilled, unfulfilled
- **Payment methods:** Shopify Payments, PayPal Express Checkout, Gift card, Bogus Gateway (for testing)
- **Tags:** pre-order, test
- **Currency:** GBP

Are these all what you'd expect? If you confirm, I'll save them, and any new value in next month's export will be flagged. Until then the figures assume they're normal.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes £17,788.28 of VAT and £2,915.10 of shipping; the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: VAT is passed on to the tax office, shipping pays the carrier, and product costs and fees are not taken off.

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

Revenue: **£86,504.99** (VAT excluded, shipping excluded, partial refunds as amount); after refunds: **£85,085.66**.

## Top products

By product revenue (line price x quantity, before order discounts, VAT included when prices include it):

1. Deluxe Gift Box: £8,295.00 (105 units)
2. Retinol Serum 30ml: £7,956.00 (221 units)
3. Peptide Serum 30ml: £6,840.00 (180 units)
4. Night Cream 50ml: £6,240.00 (208 units)
5. Day Moisturiser 50ml: £6,048.00 (216 units)

## What was left out

85 orders were left out of the 1640 in the export for this month: cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449.

Orders are placed in a month by order Created at, as written in the export. Refunds are counted in the month of their order, so a refund issued in September on an August order is in these figures, and a refund issued in August on a July order is not.

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
- computed by shopify-month-end v0.5.2, scripts ae0423f29e4e

## Question for you

These figures use the usual answer until you confirm:

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

