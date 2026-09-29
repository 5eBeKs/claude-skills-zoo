The figures 122, 10,050, 148 and 5,156.62 in my last answer were totals I added up myself. The calculation doesn't produce them, so I've taken them out. Below is the rendered text as it came out. Its long lists are shortened to counts. The full report, `files/margins_2026-07.md`, passed the number check and lists every order and SKU in full.

# Product margins, July 2026 (USD)

**Warnings:** - none

**Before any figure:** the export's shape is not recorded yet, and the figures use the usual answers to the open questions at the end until you confirm them. They are checked against nothing outside the export.

## Sold below cost

None. No product with a known cost was sold below cost in July (0 products below cost). The lowest margin with a known cost is Slim Chino - Navy / 28 (HP-CHN-NVY-28): 30 units, 1,655.77 revenue, 1,025.77 margin, 62.0%.

## Can't tell: no known cost (42 SKUs)

Their margin is unknown, not zero. Please send their unit costs.

- Classic Crew Tee, 30 SKUs `CT-...`: see renamed SKUs below
- Heavyweight Hoodie - Forest: HP-HWH-FOR-L, HP-HWH-FOR-M, HP-HWH-FOR-S, HP-HWH-FOR-XL, HP-HWH-FOR-XXL
- Linen Bucket Hat: HP-ACC-BKT-NAT, HP-ACC-BKT-OLV
- No SKU in the orders: (no SKU) Custom embroidery (initials), (no SKU) Enamel Pin Set, (no SKU) Gift Wrap, (no SKU) Silk Bandana - Navy Dot, (no SKU) Silk Bandana - Paisley

| Product (unknown cost) | Units | Revenue ex VAT |
|---|---:|---:|
| HP-HWH-FOR-L | 37 | 3,055.97 |
| HP-HWH-FOR-M | 37 | 3,040.30 |
| HP-HWH-FOR-S | 25 | 2,047.79 |
| HP-HWH-FOR-XL | 20 | 1,653.91 |
| HP-HWH-FOR-XXL | 3 | 252.00 |
| HP-ACC-BKT-NAT | 70 | 2,440.78 |
| HP-ACC-BKT-OLV | 78 | 2,715.84 |
| (no SKU) Custom embroidery (initials) | 6 | 90.00 |
| (no SKU) Enamel Pin Set | 221 | 2,870.52 |
| (no SKU) Gift Wrap | 133 | 793.00 |
| (no SKU) Silk Bandana - Navy Dot | 101 | 3,334.92 |
| (no SKU) Silk Bandana - Paisley | 115 | 3,812.79 |

## Possibly renamed SKUs (30)

These sold under a `CT-...` SKU, while the products export has the same product name under an `HP-TEE-CLS-...` SKU. Are they the same product? Until you say so, their cost is not borrowed and their margin stays unknown.

Pattern: CT-BLK-L (Classic Crew Tee - Black / L) is HP-TEE-CLS-BLK-L in the products export, cost 7.40; all colours (BLK, HGR, NVY, OLV, WHT) and sizes XS to XXL follow it.

## Orders left out (152)

Cancelled, partly paid (the export's Total is not what was received), test orders (test gateway) and one payment pending. The full list, order by order, is in the file.

## Not spread over products

27,308.20 in discounts, 83,060.38 in refunds and 9,121.94 in tips and gift cards sold (not products). Product margins are before these.

1420 orders had VAT inside their prices (the store adds tax on top but sells abroad); their own tax was taken out of their lines. VAT removed: each order's own tax, where its prices include it. The figures cover 7875 orders.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- no VAT rate given: each order's own tax is taken out of its lines where its prices include it (the usual answer; please confirm)
- the orders export has records on 31 of 31 days of July 2026
- the orders export's shape is not recorded yet (financial status: authorized, expired, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: USD; payment method: (for testing) Bogus Gateway, Bank Deposit, Cash, Cash on Delivery (COD), Gift Card, PayPal Express Checkout, Shopify Payments, manual; tags: Net 15, Net 30, Subscription, Subscription First Order, Subscription Recurring Order, replacement, test, wholesale)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 58,166 rows, SHA-256 4c14bc07ab3d150c
- products_export.csv: 278 rows, SHA-256 9bfaf73f89f87d36
- computed by shopify-month-end v0.8.0, scripts a2577a534305

## Open questions

The figures use the usual answers until you confirm them; a different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

*After this answer the plugin's own answer check ended the turn with:* Month-end check: the answer above did not pass the check against the computed results (figures that are in no computed result: 122, 10,050, 148, 5,156.62). Ask for the checked answer before using these figures.
