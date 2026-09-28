<!-- numbers-0.5.1-claude-opus-5-5 / numbers-summary-c / with the plugin / run 2: passed -->

August 2026 sales came to **£106,722.52 charged**, with **£105,019.33 left after refunds**. For your accountant, revenue without VAT and without shipping is **£86,504.99**, or **£85,085.66 after refunds**.

The full version is saved as `files/summary_2026-08.md`, and it lists every excluded order by number. That file passed the number check that confirms each figure came from the export. The version below replaces the 85-order list with a count, which is the only difference.

---

# August 2026 sales summary

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes £17,788.28 of VAT and £2,915.10 of shipping. The amount left after refunds still contains most of both, because refunds only gave some back. Neither figure is profit: the VAT is owed to HMRC, and product costs, shipping costs and fees haven't been taken off.

| | 2026-08 |
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

200 orders had a discount, and 45 orders had a full or partial refund.

## Revenue as your store defines it

**Revenue: £86,504.99** (VAT excluded, shipping excluded, partial refunds counted by amount). It is **£85,085.66** after refunds. This is probably the figure your accountant wants.

## Top products

Based on line price × quantity, before order discounts, with VAT included:

| Product | Revenue | Units |
|---|---|---|
| Deluxe Gift Box | £8,295 | 105 |
| Retinol Serum 30ml | £7,956 | 221 |
| Peptide Serum 30ml | £6,840 | 180 |
| Night Cream 50ml | £6,240 | 208 |
| Day Moisturiser 50ml | £6,048 | 216 |

## What was left out

Of the 1640 orders in the export for 2026-08, 85 were left out: cancelled orders, test orders (tagged "test" or paid through the test gateway), and paid orders not yet shipped (pre-orders). `files/summary_2026-08.md` lists each one by number.

Each order is put in a month by its "Created at" date in the export. Refunds are counted in the month of their order, so a refund issued in August for a July order is not in these figures.

## How this was counted

**Rules from your `store_definitions.json`:**
- Orders tagged "test" and orders paid through Shopify's test gateway are left out of sales.
- A sale counts only once it has shipped, so paid orders not yet shipped (pre-orders) are left out.
- Revenue is reported without VAT.
- The shipping customers pay is kept out of revenue.
- A partial refund takes off only the amount refunded.
- A refund belongs to the month of its order.
- Prices include VAT at 20%.

**The export:**
- It has records on all 31 days of August 2026.
- These figures were not checked against anything outside the export. A total from Shopify or your bank would let me cross-check them.
- Files used: `orders_export.csv` (9,074 rows, SHA-256 3035dcb90b8edd7c) and `store_definitions.json` (SHA-256 c370f6ea8162b60d). Computed by shopify-month-end v0.5.1.

## Question for you

- Are these the values you expect to see in your export?
  - Payment methods: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments
  - Financial statuses: paid, partially_refunded, refunded, voided
  - Fulfillment statuses: fulfilled, unfulfilled
  - Tags: pre-order, test
  - Currency: GBP

  If you confirm, I'll record them as the store's standard values, and any new one in a later month will be flagged. None of this changes the figures above.

---

These are sales figures, not bank figures. If your accountant also needs to know why the Shopify Payments deposits differ from sales (card fees, payouts still on the way), I can reconcile that if you share the August payout transactions export.

<!-- the report this run saved next to the exports: summary_2026-08.md -->

# August 2026 sales summary

In 2026-08 the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes £17,788.28 of VAT and £2,915.10 of shipping; the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: VAT is owed to HMRC, and product costs, shipping costs and fees have not been taken off.

| | 2026-08 |
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

200 orders had a discount; 45 orders had a refund (full or partial).

## Revenue as your store defines it

**Revenue: £86,504.99** (VAT excluded, shipping excluded, partial refunds as amount); **£85,085.66** after refunds. This is probably the figure your accountant wants.

## Top products

By line price x quantity, before order discounts, VAT included when prices include it:

| Product | Revenue | Units |
|---|---|---|
| Deluxe Gift Box | £8,295 | 105 |
| Retinol Serum 30ml | £7,956 | 221 |
| Peptide Serum 30ml | £6,840 | 180 |
| Night Cream 50ml | £6,240 | 208 |
| Day Moisturiser 50ml | £6,048 | 216 |

## What was left out

Of 1640 orders in the export for 2026-08, 85 orders were left out:

cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449

Months are assigned by order Created at, as written in the export. Refunds are counted in the month of their order, so a refund issued in August for a July order is not in these figures.

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

The figures above use the usual answer until you confirm.

