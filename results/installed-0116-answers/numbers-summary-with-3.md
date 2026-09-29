August went cleanly: the export adds up with itself and there were no warnings. Here is the checked summary:

# Sales summary, 2026-08

In 2026-08 the store charged €2,918.82 and had €2,848.32 left after refunds. The total charged includes VAT (€466.00) and shipping (€151.90); the net after refunds still holds most of both (refunds gave some back), so neither figure is profit.

| Figure | Amount |
|---|---|
| Total charged | €2,918.82 |
| Refunds | €70.50 |
| Net after refunds | €2,848.32 |
| Orders counted | 58 |
| Refunded orders | 1 |
| Average order value | €50.32 |
| Refund rate | 2.4% |
| Units sold | 134 |
| VAT inside the total | €466.00 |
| Shipping charged | €151.90 |
| Discounts given | €20.28 |

Revenue as the store defines it: €2,918.82 (VAT included, shipping included, partial refunds as amount). 6 orders had a discount.

Refunded orders (a partial refund stays a sale, only the amount comes off): #1030, #1042.

## Top products

By revenue (line price x quantity, before order discounts, VAT included when prices include it):

1. Gift Set: €833.00
2. Glass Teapot 600ml: €646.00
3. Black Tea 100g: €310.50
4. Oolong 50g: €256.00
5. Ceramic Cup: €252.00

## What was left out

2 orders were excluded: test order: #1013; cancelled: #1021.

Orders are placed in the month by order Created at, as written in the export; refunds are counted in the month of their order.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

- the orders export has records on 25 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
- Subtotal in this export is before discounts (6 orders)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
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

Checked by shopify-monthly-summary v0.11.6 · seal ccde133241a5

---

**Before you send this to your accountant,** please answer the questions above. The figures use the usual answers until you do. The VAT one probably matters most to an accountant: if they want revenue without VAT, the €466.00 VAT comes off. Once you've answered, I'll save them so every month is counted the same way.

This summary covers sales only. It doesn't show what actually reached your bank after card fees and payouts. If you also export your Shopify Payments payout transactions for August, I can do that reconciliation too.
