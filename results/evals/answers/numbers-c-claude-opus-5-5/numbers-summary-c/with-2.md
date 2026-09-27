<!-- numbers-c-claude-opus-5-5 / numbers-summary-c / with the plugin / run 2: passed -->

Here's how August 2026 went, worked out from your orders export and the answers in your `store_definitions.json`:

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes VAT (£17,788.28) and shipping (£2,915.10). The net after refunds still holds most of both, since refunds gave some back. Neither figure is profit: the VAT is owed to HMRC, the shipping pays the carrier, and product costs and fees haven't been taken off.

| | 2026-08 |
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

By product sales (line price x quantity, before order discounts, VAT included when prices include it):

1. Deluxe Gift Box: £8,295.00 (105 units)
2. Retinol Serum 30ml: £7,956.00 (221 units)
3. Peptide Serum 30ml: £6,840.00 (180 units)
4. Night Cream 50ml: £6,240.00 (208 units)
5. Day Moisturiser 50ml: £6,048.00 (216 units)

## What was left out

Months are by order Created at, as written in the export. Refunds are counted in the month of their order. Of 1640 orders in the export for 2026-08, 85 were left out (test orders, cancelled orders, and paid orders not yet shipped).

The full list, with every order and its reason, is in `files/summary_2026-08.md`.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- a sale counts only once it is shipped; paid orders not yet shipped (pre-orders) are left out (your answer)
- revenue is reported without VAT (your answer)
- the shipping customers pay is kept out of revenue (your answer)
- a partial refund takes off only the amount refunded (your answer)
- a refund belongs to the month of its order (your answer)
- prices include VAT at 20% (your answer)

All of these are your answers from `store_definitions.json`; there are no open questions.

---

**For your accountant:** send them `files/summary_2026-08.md`. It's the complete version: the same figures, plus each of the 85 left-out orders by number and reason. It passed the automatic number check. This chat version is shorter only because it gives those 85 orders as a count.

The export found no internal inconsistencies. Also note that these are sales figures, not what reached your bank: card fees and payout timing aren't included. If your accountant needs that, I can reconcile August against a Shopify Payments payouts export.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes VAT (£17,788.28) and shipping (£2,915.10), and the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: VAT is owed to HMRC, shipping pays the carrier, and product costs and fees are not taken off.

| | 2026-08 |
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

By product sales (line price x quantity, before order discounts, VAT included when prices include it):

1. Deluxe Gift Box: £8,295.00 (105 units)
2. Retinol Serum 30ml: £7,956.00 (221 units)
3. Peptide Serum 30ml: £6,840.00 (180 units)
4. Night Cream 50ml: £6,240.00 (208 units)
5. Day Moisturiser 50ml: £6,048.00 (216 units)

## What was left out

Months are by order Created at, as written in the export. Refunds are counted in the month of their order. Of 1640 orders in the export for 2026-08, 85 were left out (test orders, cancelled orders, and paid orders not yet shipped).

By reason: cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- a sale counts only once it is shipped; paid orders not yet shipped (pre-orders) are left out (your answer)
- revenue is reported without VAT (your answer)
- the shipping customers pay is kept out of revenue (your answer)
- a partial refund takes off only the amount refunded (your answer)
- a refund belongs to the month of its order (your answer)
- prices include VAT at 20% (your answer)

All of these are your answers from `store_definitions.json`; there are no open questions.

