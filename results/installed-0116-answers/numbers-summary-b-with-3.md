August went smoothly. The export didn't flag any problems, refunds were low, and 3 orders were left out: one cancelled and two test orders. The summary below is checked and sealed, and I saved a copy as `files/summary_2026-08.md` so you can send it to your bookkeeper.

---

# Sales summary for 2026-08

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes VAT ($284.28) and shipping ($229.35); the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: product costs, Shopify and card fees are not taken off.

| Figure | Amount |
|---|---|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Refunded orders (fully refunded; a partially refunded order still counts as a sale) | 1 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| VAT inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 |

Revenue as the store defines it: $4,205.63 (VAT included, shipping included, partial refunds as amount). There were no tips, gift cards sold or duties inside the total charged.

2 orders had a discount. Refunds came from order #2038 ($46.06, refunded) and order #2049 ($12.00, partially_refunded).

## Top products

By revenue (line price x quantity, before order discounts, VAT included when prices include it):

1. Reed Diffuser: $1,248.00 (39 units)
2. Cedar Candle 8oz: $672.00 (28 units)
3. Fig Candle 8oz: $528.00 (22 units)
4. Travel Tin Trio: $468.00 (24 units)
5. Match Cloche: $408.00 (34 units)

## What was left out

3 orders were left out of the figures: cancelled: #2008; test order (test payment gateway): #2011, #2044.

Months are assigned by order Created at, as written in the export, and refunds are counted in the month of their order. No other orders looked like tests without being tagged or paid through the test gateway.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

What it was computed from:

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- Subtotal in this export is before discounts (2 orders)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- computed by shopify-month-end v0.11.6, scripts ab61cfedc85c

## Questions for you

These figures use the usual answers below until you confirm them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partially refunded order: is it still a sale (usual), or a refunded order? Either way only the amount refunded comes off.
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-monthly-summary v0.11.6 · seal e798c4bc297c

---

**Before it goes to your bookkeeper:**
- **Answer the questions above.** If you want revenue shown without VAT or without shipping, I'll run the numbers again that way.
- **Check against an outside figure.** The export hasn't been compared with anything outside it. If you give me the August total from your Shopify dashboard or bank, I'll check the numbers against it.
- **What reached the bank** is not shown here: card fees and payout timing aren't in this export. If your bookkeeper needs that, send me the Shopify Payments payout export and I'll do a reconciliation.
