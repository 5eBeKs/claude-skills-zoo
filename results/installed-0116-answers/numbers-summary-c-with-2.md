# August 2026 sales summary

In August the store charged £106,722.52 and had £105,019.33 left after refunds. The total charged includes VAT (£17,788.28) and shipping (£2,915.10). The net after refunds still holds most of both, because refunds only gave some of it back. So neither figure is profit.

Revenue as your store defines it is **£86,504.99** (VAT excluded, shipping excluded, partial refunds as amount).

| Figure | Amount |
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

## Top products

These are ranked by line price × quantity, before order discounts, with VAT included because your prices include it:

1. Deluxe Gift Box: £8,295.00
2. Retinol Serum 30ml: £7,956.00
3. Peptide Serum 30ml: £6,840.00
4. Night Cream 50ml: £6,240.00
5. Day Moisturiser 50ml: £6,048.00

## What was left out

85 orders were left out. They were cancelled orders, test orders (tagged "test" or paid through the test gateway) and paid orders that hadn't shipped yet. The full list, with every order number, is in the saved file. Each order is placed in the month its "Created at" date falls in, and refunds count in the month of their order. No other orders looked like tests.

## How this was counted

- Orders tagged "test" and orders paid through Shopify's test gateway are left out of sales (your answer)
- A sale counts only once it has shipped, so paid orders not yet shipped (pre-orders) are left out (your answer)
- Revenue is reported without VAT (your answer)
- The shipping customers pay is kept out of revenue (your answer)
- A partial refund takes off only the amount refunded (your answer)
- A refund belongs to the month of its order (your answer)
- Prices include VAT at 20% (your answer)

What it was computed from:

- The orders export has records on all 31 days of August 2026
- The export's column values (statuses, payment methods, tags and currency) haven't been confirmed and saved yet. What it contains: financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test
- Subtotal in this export is before discounts (200 orders)
- Nothing outside the export was checked. If you send a figure from Shopify or the bank, I can compare against it.
- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- Computed by shopify-month-end v0.11.6, scripts ab61cfedc85c

## Question for you

- Are the payment methods, statuses, tags and currency listed above all what you'd expect? If so, I'll save them, and next month any new value will be flagged.

Checked by shopify-monthly-summary v0.11.6 · seal a7c92e7def19

---

The full checked summary, including every excluded order number, is saved at `files/summary_2026-08.md`. That's the copy to send your accountant.

These are sales figures. They don't show what reached your bank, because card fees, payouts still in transit and refund timing aren't in the orders export. If your accountant needs that, send me a Shopify Payments payout export for August and I'll reconcile it against these sales.
