<!-- numbers-claude-opus-5-5 / numbers-summary-b / with the plugin / run 1: passed -->

August went fine: $4,205.63 charged across 67 orders, and only two orders had refunds. Below is the summary for your bookkeeper. Every figure was calculated from `files/orders_export.csv` and checked against the export.

---

## August sales summary (2026-08)

In 2026-08 the store charged $4,205.63 and had $4,147.57 left after refunds. That total includes $284.28 of tax/VAT and $229.35 of shipping paid by customers. The net after refunds still holds most of both, since refunds only gave some back. So neither figure is profit: the tax is owed to the tax authority, shipping pays the carrier, and product costs and fees haven't been taken off.

| | |
|---|---|
| Total charged | $4,205.63 |
| Refunds | $58.06 |
| Net after refunds | $4,147.57 |
| Orders counted | 67 |
| Average order value | $62.77 |
| Refund rate | 1.4% |
| Units sold | 183 |
| Tax/VAT inside the total | $284.28 |
| Shipping charged | $229.35 |
| Discounts given | $10.00 (2 orders) |

**Revenue as the store defines it:** $4,205.63 (VAT included, shipping included, partial refunds as amount).

**Top products** (line price x quantity, before order discounts, VAT included when prices include it):
1. Reed Diffuser: $1,248.00, 39 units
2. Cedar Candle 8oz: $672.00, 28 units
3. Fig Candle 8oz: $528.00, 22 units
4. Travel Tin Trio: $468.00, 24 units
5. Match Cloche: $408.00, 34 units

**Refunds:** #2038, #2049.

**Excluded:** 3 orders, cancelled: #2008; test order (test payment gateway): #2011, #2044. Orders are assigned to the month by order Created at, as written in the export, and refunds are counted in the month of their order.

**How this was counted:**
- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- revenue is reported with VAT, as customers paid (the usual answer; please confirm)
- the shipping customers pay is part of revenue (the usual answer; please confirm)
- a partial refund takes off only the amount refunded (the usual answer; please confirm)
- a refund belongs to the month of its order (the usual answer; please confirm)

**Questions for you (or your bookkeeper).** The figures above use the usual answers until you confirm them:
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- Should revenue be reported with VAT, as the customer paid, or without VAT?
- Is the shipping fee customers pay part of revenue, or kept out of it?
- A partial refund: subtract only the amount (usual), or treat the whole order as refunded?
- A refund belongs to the month of the order (this export can only do that), or the month of the refund?

---

- **Your store's rules aren't on file yet.** There was no `store_definitions.json` next to the export, so I used the usual answers for the six questions above. If any of your answers are different, some figures will change. Tell me and I'll run it again.
- **What this doesn't cover:** it isn't a comparison with other months, and it doesn't reconcile the money that reached your bank. If your bookkeeper needs to match sales to bank deposits, send me the Shopify Payments payouts export and I can do that too.
