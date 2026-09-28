<!-- numbers-0.6.0-claude-opus-5-5 / numbers-summary-b / with the plugin / run 1: passed -->

August went cleanly: 67 orders brought in $4,205.63, and only 2 were refunded. The totals below were calculated from the export and passed a check that every number traces back to the data. I haven't compared them with anything outside the export, like your Shopify dashboard or bank statement. Here's the summary for your bookkeeper:

---

# Sales summary, 2026-08

The export has no internal inconsistencies. It has orders on 27 of 31 days, from 2026-08-01 to 2026-08-31. It doesn't start late or stop early. These days have no orders: 2026-08-02, 2026-08-07, 2026-08-13, 2026-08-22. If the store did take orders on those days, let me know and I'll recheck the export.

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. The total charged includes $284.28 of sales tax/VAT and $229.35 of shipping. The amount left after refunds still contains most of both, because refunds returned only part of them. **None of this is profit.** The tax goes to the tax authority, shipping pays the carrier, and product costs, Shopify and card fees haven't been subtracted.

| Figure | 2026-08 |
|---|---:|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| Sales tax/VAT inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 |

**Revenue as the store defines it:** $4,205.63 (VAT included, shipping included, partial refunds as amount). After refunds, revenue is $4,147.57.

**Refunds:** 2 orders were refunded: #2038, #2049. The export doesn't record why. 2 orders used a discount.

## Top products

These figures use line price x quantity, before order discounts, VAT included when prices include it.

| Product | SKU | Units | Revenue |
|---|---|---:|---:|
| Reed Diffuser | MO-DIF-001 | 39 | $1,248.00 |
| Cedar Candle 8oz | MO-CND-001 | 28 | $672.00 |
| Fig Candle 8oz | MO-CND-002 | 22 | $528.00 |
| Travel Tin Trio | MO-CND-010 | 24 | $468.00 |
| Match Cloche | MO-MAT-001 | 34 | $408.00 |

## Excluded orders

Of the 70 orders in the export, 3 were excluded: cancelled: #2008; test order (test payment gateway): #2011, #2044.

Orders are assigned to a month by order Created at, as written in the export. Each refund counts in the month of its original order.

## How this was counted

Definitions used. None of these has been confirmed by you yet:
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

What the figures were computed from:
- the orders export has records on 27 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: USD; payment method: Bogus Gateway (for testing), Gift card, Shopify Payments; tags: none)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it
- orders_export.csv: 143 rows, SHA-256 48a2c1db82927e07
- computed by shopify-month-end v0.6.0, scripts 7c2c32653639

## Questions for you

Until you answer these, the figures use the usual answers:
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

If your answers to the questions above change any definition, I'll recalculate. Once you confirm the payment methods, statuses and currency are what you expect, I'll save them so next month's export gets flagged if anything new appears.
