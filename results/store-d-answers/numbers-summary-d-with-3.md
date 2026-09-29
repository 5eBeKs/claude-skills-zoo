My last reply reworded the checked text, and the check caught figures I had moved around by hand. Below is the checked text exactly as rendered. The full version, which lists all 305 left-out orders by number and reason, is saved at `files/summary_2026-08.md`. It's the answer of record and passed the number check. The only change in this chat copy is that the list of 305 orders is shown as a count.

In short, sales for August are **$1,457,904.95** after refunds. That figure includes VAT, shipping and duties. It rests on the usual definitions, which the store hasn't confirmed yet (see the questions at the end). A figure without VAT isn't computed.

---

# Sales summary, 2026-08

## First: the export does not fully add up with itself

15 orders have line items that do not match their Subtotal. The figures below use each order's Subtotal and Total, but the product table may overstate these orders:

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

The export has records on 31 of 31 days of the month (from 2026-08-01 to 2026-08-31), so it does not start late or stop early.

## The figure

**Sales for 2026-08: $1,457,904.95** after refunds ($1,523,672.34 before refunds), on the store's usual definitions: VAT included, shipping included, partial refunds as amount, tips and gift cards sold left out (a gift card is revenue when it is used).

In 2026-08 the store charged $1,540,975.01 and had $1,475,207.62 left after refunds. The total charged includes $114,479.38 of VAT and $103,391.18 of shipping. The net after refunds still holds most of both (refunds gave some back). None of this is profit: VAT is owed to the tax authority, and shipping, product cost and fees have not been taken off.

The total charged also holds money that is not a sale this month:

- tips: $1,827.67
- gift cards sold: $15,475.00 (these become revenue when the card is spent)
- duties collected: $15,795.82 (these are still inside the sales figure above)

Tips and gift cards are left out of the sales figure. A sales figure without VAT is not computed.

| | USD |
|---|---:|
| Total charged | 1,540,975.01 |
| Refunds | 65,767.39 |
| Net after refunds | 1,475,207.62 |
| Orders counted | 14867 |
| Average order value | 103.65 |
| Refund rate | 4.3% |
| Units sold | 32742 |
| VAT inside the total | 114,479.38 |
| Shipping charged | 103,391.18 |
| Discounts given | 104,160.94 |

5968 orders had a discount. 935 orders had a refund. The export does not say why.

## Top products

Basis: line price x quantity, before order discounts, VAT included when prices include it.

| Product | Units | Revenue |
|---|---:|---:|
| Silk Bandana - Navy Dot (no SKU in the export) | 1665 | 38,429.36 |
| Everyday Ankle Socks 5-Pack | 1210 | 26,876.48 |
| Canvas Weekender Bag | 173 | 25,637.29 |
| Summer Wrap Dress - Floral / M | 374 | 23,351.44 |
| Summer Wrap Dress - Floral / L | 342 | 22,133.90 |

## What was left out, and why

The export holds 15172 orders for the month. 14867 are counted, and 305 were left out. Orders that are cancelled, or whose payment is pending or only authorized, are not sales. Every one is listed by order number and reason in the saved file.

The month is based on the order Created at, as written in the export. Refunds are counted in the month of their order.

## Looks like a test, still counted

Order #67254 ($142.58): the order's note says test, but it has no test tag or test gateway. It stays in the figures until you say otherwise.

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
- 1434 orders differ from the sum of their parts by a cent or two (currency conversion field by field), not counted as data issues
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 58,166 rows, SHA-256 4c14bc07ab3d150c
- computed by shopify-month-end v0.7.0, scripts 4810985b2401

## Questions for the owner

The figures use the usual answers until you confirm them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
- 1 order(s) look like tests but carry no test tag or test gateway (#67254): leave them out of sales? They are counted until you say so; tagging them 'test' leaves them out.
