I've saved the September summary as `files/summary_2026-09.md` for your bookkeeper. It is the checked text in full, including the long lists: the 136 orders that don't add up, the 178 orders left out and the 184 refunded orders, each with its order number.

**Before they use it:** these figures are worked out from the orders export. They are not Shopify's own Analytics "Total sales" report. In particular, refunds are counted in the month of their order, while Shopify's sales report counts them in the month the refund was made. The export has no refund dates, so it can't be done Shopify's way. If you send me Shopify's September "Total sales" figure or the bank payouts, I can check these against it.

Below is the checked text, with the long lists left out:

---

## First: what does not add up

- 136 orders in the export do not add up with themselves, for example #74094: Subtotal - Discount + Shipping (+ Taxes) does not give Total 243.02; they are counted as the export has them.

For most of these orders, including #74094, the gap is exactly the order's duties.

## The month in one line

In 2026-09 the store charged €775,856.03 and had €763,203.06 left after refunds. The total charged includes VAT (€123,688.79) and shipping (€43,100.10); the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: no product costs, fees or VAT owed have been taken off.

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
| Discounts given | €26,247.91 |

1372 orders had a discount. 184 orders had a refund.

## Revenue

Revenue as the store defines it: €764,349.44 (VAT included, shipping included, partial refunds as amount, tips, gift cards sold and duties left out (a gift card is revenue when it is used; duties are passed on to customs)). After refunds: €751,696.47.

The total charged also holds money that is not a sale:

- gift cards sold: €7,875.00, which become revenue when they are used;
- duties collected: €3,631.59, passed on to customs.

## Top products

Basis: line price x quantity, before order discounts, VAT included when prices include it.

| Product | SKU | Units | Revenue |
|---|---|---|---|
| Wool Throw - Forest | BW-THR-FOR | 161 | €18,880.53 |
| Ceramic Table Lamp - Moss | SV-LMP-MOS | 125 | €18,508.82 |
| Ceramic Table Lamp - Chalk | SV-LMP-CHK | 118 | €17,513.83 |
| Jute Rug - 200x300 cm | SV-RUG-200 | 50 | €17,451.27 |
| Wool Throw - Charcoal | BW-THR-CHR | 139 | €16,509.28 |

## What was left out, and why

178 orders were left out: they were cancelled, their payment was pending or only authorized, they were partly paid, or they were test orders. The saved file names every one with its reason.

Orders whose payment is pending or only authorized, and partly paid orders, are not sales yet, so they are left out.

Month basis: order Created at, as written in the export. Refunds are counted in the month of their order, not in the month they were paid out.

No orders look like tests without carrying a test tag or the test gateway.

## How this was counted

Definitions:

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

The export:

- the orders export has records on 30 of 30 days of September 2026
- the orders export's shape is not recorded yet (financial status: authorized, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: EUR; payment method: Bank Deposit, Cash, Klarna, PayPal Express Checkout, Shopify Payments, bogus, gift_card, manual; tags: b2b, duplicate, horeca, replacement, telefonisch, test)
- Subtotal in this export is after discounts (1244 orders)
- 308 orders differ from the sum of their parts by a few cents (rounding, or currency conversion field by field), not counted as data issues
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Files and version:

- orders_export.csv: 37,159 rows, SHA-256 9183e83aad61ad26
- computed by shopify-month-end v0.10.1, scripts 7f1d3055b74c

## Questions for the owner

The figures above use the usual answers until you confirm them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

Checked by shopify-monthly-summary v0.10.1 · seal 843fa7faaef5
