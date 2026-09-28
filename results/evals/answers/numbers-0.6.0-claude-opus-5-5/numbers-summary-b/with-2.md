<!-- numbers-0.6.0-claude-opus-5-5 / numbers-summary-b / with the plugin / run 2: passed -->

August went well. The store charged **$4,205.63** across 67 orders and kept **$4,147.57** after refunds. Refunds were small, at 1.4%. The export had no internal inconsistencies. I left out three orders: one cancelled and two test orders. Keep in mind that the figures don't count processing fees, product costs or payouts.

Before you send it to your bookkeeper, please answer the questions at the end. I used the standard Shopify settings for now, and a few of the answers could change the numbers. Here is the summary exactly as it passed the number check:

---

# Sales summary, 2026-08

In 2026-08 the store charged **$4,205.63** and had **$4,147.57** left after refunds. That total includes $284.28 of tax collected and $229.35 of shipping charged to customers; the net after refunds still holds most of both (refunds gave some back). Neither figure is profit: the tax is owed on, and product costs, shipping costs and fees have not been taken off.

| Figure | 2026-08 |
|---|---|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| Tax inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 |

**Revenue as the store defines it:** $4,205.63 (VAT included, shipping included, partial refunds as amount).

Refunded orders: #2038, #2049. 2 orders had a discount. The export does not say why refunds happened.

## Top products

By line price x quantity, before order discounts, VAT included when prices include it:

1. Reed Diffuser: $1,248.00 (39 units)
2. Cedar Candle 8oz: $672.00 (28 units)
3. Fig Candle 8oz: $528.00 (22 units)
4. Travel Tin Trio: $468.00 (24 units)
5. Match Cloche: $408.00 (34 units)

## What was left out

3 orders were left out: cancelled: #2008; test order (test payment gateway): #2011, #2044.

Orders are placed in the month by order Created at, as written in the export; refunds are counted in the month of their order.

## How this was counted

Definitions:

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

The export:

- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

Files and version:

- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- computed by shopify-month-end v0.6.0, scripts 7c2c32653639

## Questions for you

The figures above use the usual answers until you confirm them:

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

**Other notes:**
- **Tax:** the export adds tax on top of prices, so for a US store this is most likely sales tax, even though the report calls it "VAT." The $284.28 is money you owe, not income.
- **Days with no orders:** August 2, 7, 13 and 22 have no orders in the export. Could you confirm those really were quiet days and not a gap in the export?
- **Sample Votive:** 9 units went out at $0. They were probably free samples, so they count toward the 183 units sold but add no revenue.
- **Checking against outside figures:** I only checked the numbers against the export itself. If you send me Shopify's own sales total for August or your bank deposits, I'll check against those too.
