August went fine. The export adds up with itself, has no warnings and no data problems, and covers the whole month. Below is the checked summary. A copy for your bookkeeper is saved as `files/summary_2026-08.md`, next to the export.

---

# 2026-08 sales summary

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes $284.28 of VAT and $229.35 of shipping; the net after refunds still holds most of both (refunds gave some back), so neither figure is profit.

| Figure | Amount |
|---|---|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Refunded orders (partial refunds still count as sales) | 1 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| VAT inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 |

Revenue as the store defines it: $4,205.63 (VAT included, shipping included, partial refunds as amount). 2 orders had a discount.

## Top products (line price x quantity, before order discounts, VAT included when prices include it)

1. Reed Diffuser: $1,248.00
2. Cedar Candle 8oz: $672.00
3. Fig Candle 8oz: $528.00
4. Travel Tin Trio: $468.00
5. Match Cloche: $408.00

## What was left out

3 orders were excluded: cancelled: #2008; test order (test payment gateway): #2011, #2044.

Months are by order Created at, as written in the export; refunds are counted in the month of their order.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

Computed from:

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- Subtotal in this export is before discounts (2 orders)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- computed by shopify-month-end v0.11.0, scripts c018b6dee526

## Questions for you

The figures above use the usual answers until you confirm them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partially refunded order: is it still a sale (usual), or a refunded order? Either way only the amount refunded comes off.
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-monthly-summary v0.11.0 · seal 5a92a033eecb

---

These are sales figures, not what reached your bank. Card fees, refund timing and payouts still in transit aren't included. If your bookkeeper needs that too, send me the Shopify Payments payout export for August and I'll match it against these sales.
