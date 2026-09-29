August was a clean month: the export adds up with itself and there were no warnings. Here's the summary for your bookkeeper:

---

# Sales summary, 2026-08

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes $284.28 of VAT/sales tax and $229.35 of shipping; the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: product costs, fees, tax owed and shipping costs have not come off.

| Figure | Value |
|---|---|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Refunded orders (partial refunds still count as sales) | 1 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| VAT/sales tax inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 |

Revenue as the store defines it: $4,205.63 (VAT included, shipping included, partial refunds as amount). 2 orders had a discount. No tips, gift cards sold or duties were in the total.

## Top products

By revenue (line price x quantity, before order discounts, VAT included when prices include it):

1. Reed Diffuser: 39 units, $1,248.00
2. Cedar Candle 8oz: 28 units, $672.00
3. Fig Candle 8oz: 22 units, $528.00
4. Travel Tin Trio: 24 units, $468.00
5. Match Cloche: 34 units, $408.00

## What was left out

3 orders were left out: cancelled: #2008; test order (test payment gateway): #2011, #2044. Orders are placed in the month by order Created at, as written in the export, and refunds are counted in the month of their order. No untagged orders looked like tests.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

Computed from and by:

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- Subtotal in this export is before discounts (2 orders)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- computed by shopify-month-end v0.11.6, scripts ab61cfedc85c

## Questions for you

These figures use the usual answers until you confirm them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partially refunded order: is it still a sale (usual), or a refunded order? Either way only the amount refunded comes off.
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-monthly-summary v0.11.6 · seal d95cc41b9154

---

**Before you send it:**
- **Confirm the questions above.** If your answers differ from the usual ones (for example, if your bookkeeper wants revenue without VAT or shipping), I'll recalculate. Once you confirm the payment methods and statuses, I'll record them so a new one gets flagged next month.
- **Nothing outside the export was checked.** If you give me a figure from Shopify Analytics or your bank, like the order count or total sales, I'll check the export against it.
- **This is sales, not cash in the bank.** If your bookkeeper also needs to know why the payouts differ from sales (card fees, payouts still in transit), I can reconcile it if you send the Shopify Payments payout export.
