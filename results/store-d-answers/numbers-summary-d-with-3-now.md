The full sealed summary, which names all 305 orders that were left out, is saved at `files/summary_2026-08.md`. That file is the one to send your bookkeeper. Below is the same answer, shortened for chat. **The one sales figure is the revenue line under "The figure".**

# Sales summary, 2026-08

## Check first

- 15 orders in the export do not add up with themselves, for example #78754: line items sum to 70.00, Subtotal says 36.90: an item removed by an order edit may still be listed; they are counted as the export has them.

## The figure

In 2026-08 the store charged $1,540,975.01 and had $1,475,207.62 left after refunds. The total charged includes VAT ($114,479.38) and shipping ($103,391.18); the net after refunds still holds most of both (refunds gave some back). Neither figure is profit.

**Revenue as the store defines it: $1,507,876.52** (VAT included, shipping included, partial refunds as amount, tips, gift cards sold and duties left out (a gift card is revenue when it is used; duties are passed on to customs)). Revenue after refunds: $1,442,109.13.

The total charged also holds money that is not a sale:

- tips: $1,827.67
- gift cards sold: $15,475.00 (revenue when they are used)
- duties collected: $15,795.82 (passed on to customs)

| | |
|---|---|
| Total charged | $1,540,975.01 |
| Refunds | $65,767.39 |
| Net after refunds | $1,475,207.62 |
| Orders counted | 14867 |
| Average order value | $103.65 |
| Refund rate | 4.3% |
| Units sold | 32742 |
| VAT inside the total | $114,479.38 |
| Shipping charged | $103,391.18 |
| Discounts given | $104,160.94 |

5968 orders had a discount; 935 orders had a refund.

## Top products

(line price x quantity, before order discounts, VAT included when prices include it)

1. Silk Bandana - Navy Dot: $38,429.36
2. Everyday Ankle Socks 5-Pack: $26,876.48
3. Canvas Weekender Bag: $25,637.29
4. Summer Wrap Dress - Floral / M: $23,351.44
5. Summer Wrap Dress - Floral / L: $22,133.90

## Left out

305 orders were left out of the figures, each named by reason in files/summary_2026-08.md.

Month basis: order Created at, as written in the export. Refunds are counted in the month of their order.

## Possibly a test order, still counted

#67254

These are counted until the owner says otherwise.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: authorized, expired, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: USD; payment method: (for testing) Bogus Gateway, Bank Deposit, Cash, Cash on Delivery (COD), Gift Card, PayPal Express Checkout, Shopify Payments, manual; tags: Net 15, Net 30, Subscription, Subscription First Order, Subscription Recurring Order, replacement, test, wholesale)
- Subtotal in this export is after discounts (5933 orders) on some orders and before discounts (29 orders)
- 1434 orders differ from the sum of their parts by a few cents (rounding, or currency conversion field by field), not counted as data issues
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 58,166 rows, SHA-256 4c14bc07ab3d150c
- computed by shopify-month-end v0.10.1, scripts 3f193068ad79

## Questions for the owner

The figures use the usual answers until the owner confirms them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
- 1 order(s) look like tests but carry no test tag or test gateway (#67254): leave them out of sales? They are counted until you say so; tagging them 'test' leaves them out.
