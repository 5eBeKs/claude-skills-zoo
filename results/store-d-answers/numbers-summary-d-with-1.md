# Sales summary, 2026-08

## Check first: the export does not fully add up with itself

On these orders the line items add up to more than the order's Subtotal. An item removed by an order edit may still be listed, so units and product figures may be slightly high on them (the order totals are taken as written):

- #78754: line items sum to 70.00, Subtotal says 36.90: an item removed by an order edit may still be listed
- #77661: line items sum to 64.00, Subtotal says 42.00: an item removed by an order edit may still be listed
- #77017: line items sum to 164.00, Subtotal says 83.20: an item removed by an order edit may still be listed
- #76795: line items sum to 67.40, Subtotal says 45.34: an item removed by an order edit may still be listed
- #75160: line items sum to 265.00, Subtotal says 192.80: an item removed by an order edit may still be listed
- #74934: line items sum to 192.00, Subtotal says 132.00: an item removed by an order edit may still be listed
- #72089: line items sum to 73.02, Subtotal says 29.21: an item removed by an order edit may still be listed
- #71877: line items sum to 51.00, Subtotal says 17.60: an item removed by an order edit may still be listed
- #71541: line items sum to 174.86, Subtotal says 145.74: an item removed by an order edit may still be listed
- #71334: line items sum to 155.66, Subtotal says 51.78: an item removed by an order edit may still be listed
- #71092: line items sum to 118.00, Subtotal says 90.00: an item removed by an order edit may still be listed
- #70950: line items sum to 266.00, Subtotal says 192.00: an item removed by an order edit may still be listed
- #70034: line items sum to 75.00, Subtotal says 17.00: an item removed by an order edit may still be listed
- #67674: line items sum to 75.00, Subtotal says 58.00: an item removed by an order edit may still be listed
- #64959: line items sum to 202.00, Subtotal says 74.00: an item removed by an order edit may still be listed

## The figure

In 2026-08 the store charged $1,540,975.01 and had $1,475,207.62 left after refunds. The total charged includes VAT ($114,479.38) and shipping ($103,391.18). The net after refunds still holds most of both (refunds gave some back), so neither figure is profit: it is what customers paid, not what the store kept.

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
| Discounts given | $104,160.94 (5968 orders had a discount) |

## Revenue as the store defines it

Revenue: $1,523,672.34, after refunds $1,457,904.95 (VAT included, shipping included, partial refunds as amount, tips and gift cards sold left out (a gift card is revenue when it is used)).

The total charged also holds money that is not a sale this month:

- tips: $1,827.67
- gift cards sold: $15,475.00 (revenue when they are used, not when sold)
- duties collected: $15,795.82

## Top products

By line price x quantity, before order discounts, VAT included when prices include it:

| Product | SKU | Units | Revenue |
|---|---|---|---|
| Silk Bandana - Navy Dot | (no SKU) | 1665 | $38,429.36 |
| Everyday Ankle Socks 5-Pack | HP-SCK-ANK5 | 1210 | $26,876.48 |
| Canvas Weekender Bag | HP-BAG-WKD | 173 | $25,637.29 |
| Summer Wrap Dress - Floral / M | HP-DRS-WRP-FLR-M | 374 | $23,351.44 |
| Summer Wrap Dress - Floral / L | HP-DRS-WRP-FLR-L | 342 | $22,133.90 |

## What was left out, and why

Orders are placed in a month by order Created at, as written in the export; refunds are counted in the month of their order. Of 15172 August orders in the export, 305 were left out: cancelled, not paid (pending, authorized, expired), partly paid, or test orders:

Every excluded order is named, by reason, in `files/summary_2026-08.md`, the answer of record.

## Looks like a test, but is counted

- #67254

This order carries no test tag or test gateway, so it is counted until the owner says otherwise.

## Questions for the owner

The figures use the usual answers below until the owner confirms them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
- 1 order(s) look like tests but carry no test tag or test gateway (#67254): leave them out of sales? They are counted until you say so; tagging them 'test' leaves them out.

## How this was counted

Definitions (whose answer each is):

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

The export:

- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: authorized, expired, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: USD; payment method: (for testing) Bogus Gateway, Bank Deposit, Cash, Cash on Delivery (COD), Gift Card, PayPal Express Checkout, Shopify Payments, manual; tags: Net 15, Net 30, Subscription, Subscription First Order, Subscription Recurring Order, replacement, test, wholesale)
- Subtotal in this export is after discounts (5933 orders) on some orders and before discounts (29 orders)
- 1434 orders differ from the sum of their parts by a cent or two (currency conversion field by field), not counted as data issues
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Files and version:

- orders_export.csv: 58,166 rows, SHA-256 4c14bc07ab3d150c
- computed by shopify-month-end v0.7.0, scripts 4810985b2401
