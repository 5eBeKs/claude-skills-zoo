September's numbers are done and passed the check. The full version, which lists every order, is saved as `files/summary_2026-09.md`. Your bookkeeper should read the warning at the top first: 136 orders in the export don't add up with themselves, and they're counted exactly as Shopify exported them. The chat version below gives those 136 orders and the 184 refunded orders as counts and lists every left-out order; the file names every order in every list.

# September 2026 sales, as the Shopify orders export reports them

## First: the export does not fully add up with itself

- 136 orders in the export do not add up with themselves, for example #74094: Subtotal - Discount + Shipping (+ Taxes) does not give Total 243.02; they are counted as the export has them.

The orders concerned:

136 orders; every one is listed in the file summary_2026-09.md next to the export.

In 2026-09 the store charged €775,856.03 and had €763,203.06 left after refunds. The total charged includes VAT (€123,688.79) and shipping (€43,100.10); the net after refunds still holds most of both (refunds gave some back), so neither figure is profit.

| | |
|---|---|
| Total charged | €775,856.03 |
| Refunds | €12,652.97 |
| Net after refunds | €763,203.06 |
| Orders counted | 7305 |
| Average order value | €106.21 |
| Refund rate | 1.6% |
| Units sold | 17823 |
| VAT inside the total | €123,688.79 |
| Shipping charged | €43,100.10 |
| Discounts given | €26,247.91 (1372 orders had a discount) |

## Revenue as the store defines it

Revenue: €764,349.44 (VAT included, shipping included, partial refunds as amount, tips, gift cards sold and duties left out (a gift card is revenue when it is used; duties are passed on to customs)); after refunds, €751,696.47.

The total charged also holds amounts that are not sales of the month:
- gift cards sold: €7,875.00 (revenue when they are used, not when sold);
- duties collected: €3,631.59 (passed on to customs).

## Top products

By revenue (line price x quantity, before order discounts, VAT included when prices include it):

| Product | Units | Revenue |
|---|---|---|
| Wool Throw - Forest | 161 | €18,880.53 |
| Ceramic Table Lamp - Moss | 125 | €18,508.82 |
| Ceramic Table Lamp - Chalk | 118 | €17,513.83 |
| Jute Rug - 200x300 cm | 50 | €17,451.27 |
| Wool Throw - Charcoal | 139 | €16,509.28 |

## What was left out, and why

178 orders were left out: payment authorized, not captured: #74166, #73935, #73814, #73799, #73608, #73454, #73440, #72989, #72938, #72829, #72623, #72451, #71749, #71372; payment pending, not a sale yet: #74153, #74150, #74134, #74112, #74074, #73978, #73951, #73920, #73892, #73871, #73717, #73547, #73232, #73133, #73076, #72711, #72391, #72058, #72004, #71575, #70485, #70465, #69995, #69252, #67529, #67300; cancelled: #74130, #74100, #74098, #74026, #73850, #73775, #73637, #73525, #73499, #73485, #73426, #73314, #73278, #73146, #73136, #73129, #73128, #73107, #73004, #72815, #72785, #72673, #72618, #72594, #72461, #72424, #72403, #72386, #72358, #72305, #72269, #72183, #72180, #72088, #72082, #72052, #71923, #71846, #71843, #71838, #71814, #71585, #71498, #71413, #71211, #71182, #71176, #70997, #70925, #70811, #70805, #70683, #70584, #70436, #70322, #70201, #70179, #70150, #70141, #70095, #70044, #69987, #69973, #69881, #69804, #69730, #69575, #69532, #69518, #69482, #69461, #69446, #69432, #69304, #69299, #69275, #69274, #69255, #69250, #69208, #69109, #69070, #69062, #69047, #69036, #68994, #68992, #68982, #68974, #68828, #68824, #68805, #68761, #68743, #68614, #68588, #68458, #68457, #68454, #68418, #68388, #68373, #68342, #68325, #68230, #68153, #67955, #67900, #67829, #67740, #67683, #67667, #67517, #67435, #67394, #67393, #67384, #67377, #67367, #67342, #67297, #67218, #67208, #67158, #67029, #66945, #66794, #66793, #66750; partly paid: the export's Total is not what was received: #74003, #71389, #69193, #68665, #66961, #66799; test order: #68459, #68448, #68444.

Orders are placed in the month by order Created at, as written in the export. Refunds are counted in the month of their order, so a September refund on an August order is not in these figures, and a refund on a September order made in October is. Pending, authorized and partly paid orders are not counted as sales yet.

184 orders had a refund; every one, and every order left out, is named in summary_2026-09.md.

No order looked like a test without being tagged or paid through the test gateway.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

- the orders export has records on 30 of 30 days of September 2026
- the orders export's shape is not recorded yet (financial status: authorized, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: EUR; payment method: Bank Deposit, Cash, Klarna, PayPal Express Checkout, Shopify Payments, bogus, gift_card, manual; tags: b2b, duplicate, horeca, replacement, telefonisch, test)
- Subtotal in this export is after discounts (1244 orders)
- 308 orders differ from the sum of their parts by a few cents (rounding, or currency conversion field by field), not counted as data issues
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 37,159 rows, SHA-256 9183e83aad61ad26
- computed by shopify-month-end v0.10.1, scripts 7f1d3055b74c

## Questions for you

The figures above use the usual answer to each of these until you confirm them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-monthly-summary v0.10.1 · seal 033b25ac93ce
