<!-- numbers-0.6.0-claude-opus-5-5 / numbers-summary-c / with the plugin / run 3: passed -->

Here are August 2026's figures. The full summary, which names all 85 left-out orders and why each was left out, passed the number check and is saved as `files/summary_2026-08.md`. Give your accountant that file: it's the complete record.

**The headline:** in August the store charged **£106,722.52** and had **£105,019.33** left after refunds. That total includes **£17,788.28 of VAT** and **£2,915.10 of shipping**, and the figure after refunds still holds most of both. Neither number is profit.

| | |
|---|---|
| Total charged | £106,722.52 |
| Refunds | £1,703.19 |
| Net after refunds | £105,019.33 |
| Orders counted | 1555 (of 1640 in the export) |
| Average order value | £68.63 |
| Refund rate | 1.6% (45 orders with a refund) |
| Units sold | 4918 |
| VAT inside the total | £17,788.28 |
| Shipping charged | £2,915.10 |
| Discounts given | £1,197.08 (200 orders had a discount) |

**Revenue by your store's own rules:** £86,504.99 (without VAT and shipping; partial refunds take off only the amount refunded). After refunds it's **£85,085.66**. This is probably the revenue figure your accountant wants.

**Top products** (line price × quantity, before order discounts, VAT included):
1. Deluxe Gift Box: 105 units, £8,295.00
2. Retinol Serum 30ml: 221 units, £7,956.00
3. Peptide Serum 30ml: 180 units, £6,840.00
4. Night Cream 50ml: 208 units, £6,240.00
5. Day Moisturiser 50ml: 216 units, £6,048.00

**What was left out:** 85 orders: cancelled orders, test orders, and pre-orders that were paid but not yet shipped. Your settings count a sale only once it ships, so the unshipped pre-orders will count when they ship.

**How it was counted:**
- **Which orders are August's:** those created in August.
- **Refunds:** each one counts in the month of its order, even if it was paid out later.
- **Your settings:** the rules from your `store_definitions.json` were applied, including a VAT rate of 20%.
- **Coverage:** the export has orders on all 31 days of August, so none appear to be missing.
- **Outside check:** nothing outside the export has confirmed these figures. If you send me a total from Shopify Analytics or your bank, I'll compare it.

**One question for you:** the export contains these values:
- **Order statuses:** paid, partially refunded, refunded, voided
- **Currency:** GBP only
- **Payment methods:** Shopify Payments, PayPal, gift card, and Shopify's test gateway
- **Tags:** "pre-order" and "test"

Is that everything you'd expect? If so, I'll record it, and any new value in next month's export will be flagged.

I haven't compared August with June or July. If you'd like that, or a check of what Shopify actually paid into your bank, just ask.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes £17,788.28 of VAT and £2,915.10 of shipping; the net after refunds still holds most of both (refunds gave some back). Neither figure is profit.

| | |
|---|---|
| Total charged | £106,722.52 |
| Refunds | £1,703.19 |
| Net after refunds | £105,019.33 |
| Orders counted | 1555 (of 1640 in the export) |
| Average order value | £68.63 |
| Refund rate | 1.6% (45 orders with a refund) |
| Units sold | 4918 |
| VAT inside the total | £17,788.28 |
| Shipping charged | £2,915.10 |
| Discounts given | £1,197.08 (200 orders had a discount) |

**Revenue as your store defines it:** £86,504.99 (VAT excluded, shipping excluded, partial refunds as amount); after refunds, £85,085.66.

## Top products

By line price x quantity, before order discounts, VAT included when prices include it:

1. Deluxe Gift Box: 105 units, £8,295.00
2. Retinol Serum 30ml: 221 units, £7,956.00
3. Peptide Serum 30ml: 180 units, £6,840.00
4. Night Cream 50ml: 208 units, £6,240.00
5. Day Moisturiser 50ml: 216 units, £6,048.00

## What was left out

85 orders were left out: cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449.

Orders are placed in a month by order Created at, as written in the export. Refunds are counted in the month of their order, not the month they were paid out.

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

Until you confirm, the figures above use the export as it stands.

