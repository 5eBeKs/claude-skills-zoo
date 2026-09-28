<!-- numbers-0.5.2-claude-opus-5-5 / numbers-summary-c / with the plugin / run 2: passed -->

## August 2026 sales summary

In August the store charged **£106,722.52**, and **£105,019.33** was left after refunds. The total charged includes **£17,788.28 of VAT** and **£2,915.10 of shipping** paid by customers. Refunds only gave back a small part of those, so the net figure still contains most of both. **Neither figure is profit.**

| Figure | Amount |
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

200 orders had a discount.

**Revenue, using your store's definition:** **£86,504.99** (VAT excluded, shipping excluded, partial refunds counted by amount). After refunds it's **£85,085.66**. This is probably the figure your accountant wants.

**Top products** (line price × quantity, before order discounts, VAT included):
1. Deluxe Gift Box: £8,295.00 (105 units)
2. Retinol Serum 30ml: £7,956.00 (221 units)
3. Peptide Serum 30ml: £6,840.00 (180 units)
4. Night Cream 50ml: £6,240.00 (208 units)
5. Day Moisturiser 50ml: £6,048.00 (216 units)

**Left out:** 85 of the 1640 August orders in the export aren't in the figures above:
- **Cancelled:** #32854, #32993, #33276, #33356, #33431, #33443, #33631
- **Test orders (test payment gateway):** #32872, #33456, #33634, #34406
- **Test orders (tagged "test"):** #32917, #33065, #33415, #33420
- **Not shipped yet:** all the remaining orders. Your rule is that a sale only counts once it has shipped, so paid pre-orders are left out. The full list of order numbers is in the saved file.

Each order is assigned to a month by its "Created at" date. Refunds are counted in the month of their order, not the month the money went back.

**How this was counted:** these are all your own answers from `store_definitions.json`:
- Test orders are left out.
- A sale counts only once it has shipped.
- Revenue is reported without VAT and without shipping.
- A partial refund takes off only the amount refunded.
- Prices include VAT at 20%.

The export has records on all 31 days of August. I haven't checked it against anything outside the export. If you send me a total from Shopify or the bank, I can check it.

**One question for you:** your export contains these values:
- **Payment methods:** Shopify Payments, PayPal Express Checkout, Gift card, and Bogus Gateway (the test gateway)
- **Statuses:** paid, partially_refunded, refunded, voided
- **Tags:** pre-order, test
- **Currency:** GBP only

Are these all as expected? If so, I'll record them, and next month any new value will be flagged. Until you confirm, the figures use the usual treatment for each.

The full summary, including every excluded order number and the file checksums, is saved as `files/summary_2026-08.md`. That's the version to give your accountant. It isn't a payout reconciliation, so it doesn't show card fees or what actually reached the bank. I can do that too if you have the Shopify Payments payouts export.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# Sales summary: 2026-08

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes £17,788.28 of VAT and £2,915.10 of shipping paid by customers. The net after refunds still holds most of both, because refunds gave only some of it back. None of these figures is profit.

| Figure | Amount |
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

200 orders had a discount.

## Revenue as your store defines it

Revenue: **£86,504.99** (VAT excluded, shipping excluded, partial refunds as amount). After refunds: £85,085.66.

## Top products

Product revenue is counted as line price x quantity, before order discounts, VAT included when prices include it.

1. Deluxe Gift Box: £8,295.00 (105 units)
2. Retinol Serum 30ml: £7,956.00 (221 units)
3. Peptide Serum 30ml: £6,840.00 (180 units)
4. Night Cream 50ml: £6,240.00 (208 units)
5. Day Moisturiser 50ml: £6,048.00 (216 units)

## What was left out

Of 1640 orders in the export for 2026-08, 85 were left out of the figures:

cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449

Orders are placed in a month by order Created at, as written in the export. Refunds are counted in the month of their order, not the month they were paid out.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)
- a sale counts only once it is shipped; paid orders not yet shipped (pre-orders) are left out (your answer)
- revenue is reported without VAT (your answer)
- the shipping customers pay is kept out of revenue (your answer)
- a partial refund takes off only the amount refunded (your answer)
- a refund belongs to the month of its order (your answer)
- prices include VAT at 20% (your answer)

Computed from:

- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.5.2, scripts ae0423f29e4e

## Question for you

These figures use the usual answer until you confirm:

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

