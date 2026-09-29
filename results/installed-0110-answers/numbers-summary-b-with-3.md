August went quietly: the store took in $4,205.63 across 67 orders and refunded very little. The script found no data problems and gave no warnings. Here is the checked summary for your bookkeeper:

---

# Shopify sales summary — 2026-08

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes VAT ($284.28) and shipping ($229.35); the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: product costs, Shopify fees and VAT owed still come out of it.

| Figure | Amount |
|---|---|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Refunded orders (a partial refund still counts as a sale) | 1 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| VAT inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 |

Revenue as the store defines it: $4,205.63 (VAT included, shipping included, partial refunds as amount). 2 orders had a discount. Orders with a refund: #2038, #2049.

## Top products (line price x quantity, before order discounts, VAT included when prices include it)

| Product | Units | Revenue |
|---|---|---|
| Reed Diffuser | 39 | $1,248.00 |
| Cedar Candle 8oz | 28 | $672.00 |
| Fig Candle 8oz | 22 | $528.00 |
| Travel Tin Trio | 24 | $468.00 |
| Match Cloche | 34 | $408.00 |

## Left out

3 orders were left out: cancelled: #2008; test order (test payment gateway): #2011, #2044. Orders are placed in the month by order Created at, as written in the export, and refunds are counted in the month of their order. No untagged orders looked like tests.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

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

Checked by shopify-monthly-summary v0.11.0 · seal e7bd2b7a04ad

---

**Before sending it on:**
- **These are sales figures, not what reached your bank.** They don't include Shopify's card fees or payouts. If your bookkeeper needs that, send me the Shopify Payments payouts export and I'll match it against these orders.
- **Please answer the questions above.** The figures use the usual answers for now. If any of your answers are different (for example, reporting revenue without VAT), I'll rerun it so next month is counted the same way.
