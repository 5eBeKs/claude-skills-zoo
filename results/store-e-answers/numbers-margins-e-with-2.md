In July, every product with a known cost made money and none lost money. For 11 products I can't tell, because their costs are missing or don't match the orders. The full report passed the number check and is saved as `files/margins_2026-07.md`, with every product's figures and every order left out.

Below is the summary, filled in from the calculated results. All its figures traced back to those results. The number check only objects that it doesn't list the 134 excluded orders one by one; they're all in the file.

# Product margins, July 2026

**Warnings:** 

The full report, with every product's units, revenue without VAT, cost and margin, and every order left out, is saved as `files/margins_2026-07.md`.

## Made money

Every product with a known cost sold above that cost. The lowest margin is Stoneware Mug - Second Choice (KK-MUG-2ND) at 38.4%.

## Lost money

None: no product with a known cost sold below it (below cost: 0 products).

## Cannot tell: cost unknown

(no SKU) Gift Wrapping, (no SKU) Unique Handthrown Bowl - Large, (no SKU) Unique Handthrown Bowl - Medium, (no SKU) Unique Handthrown Bowl - Small, HT-OSB-L, HT-OSB-M, HT-OSB-S, KK-PIC-BLU, KK-PIC-RED, LN-NAP-OT, LN-NAP-SG

Their margin is unknown, not zero.

- The Linen Napkins Oat and Sage sell as LN-NAP-OT and LN-NAP-SG. The cost sheet has LIN-NAP-OAT-4 and LIN-NAP-SAGE-4, which sold nothing. Are they the same products? I have not used those costs until you confirm.
- The three Unique Handthrown Bowl sizes have no SKU in the orders or the products export, so no cost could be matched to them. Adding SKUs in Shopify would fix this.
- The Oak Serving Board variants have no Cost per item. The Striped Picnic Blankets and Gift Wrapping have no cost row at all. Picnic Blanket Blue revenue without VAT was 10,208.60, and Picnic Blanket Red was 10,050.49.

## Not spread over products

This is not spread over products: 41,764.43 in discounts, 26,538.33 in refunds and 6,950.00 in tips and gift cards sold (not products). Per-product margins are before these.

## Orders left out

Orders left out: 134, all listed in the file.

Orders with tax inside their prices: 6103. Each order's own tax was taken out of its lines.

VAT removed: each order's own tax, where its prices include it. Orders counted: 6516.

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
- a sale counts once it is paid, shipped or not (the usual answer; please confirm)
- no VAT rate given: each order's own tax is taken out of its lines where its prices include it (from the export)

- the orders export has records on 31 of 31 days of July 2026
- the orders export's shape is not recorded yet (financial status: authorized, paid, partially_paid, partially_refunded, pending, refunded, voided; fulfillment status: fulfilled, partial, unfulfilled; currency: EUR; payment method: Bank Deposit, Cash, Klarna, PayPal Express Checkout, Shopify Payments, bogus, gift_card, manual; tags: b2b, duplicate, horeca, replacement, telefonisch, test)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 37,159 rows, SHA-256 9183e83aad61ad26
- products_export.csv: 123 rows, SHA-256 de9ad79b898d8cac
- computed by shopify-month-end v0.10.1, scripts d5fb38167bf3

## Open questions

The figures use the usual answers until you confirm them. A different answer changes them.

- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
