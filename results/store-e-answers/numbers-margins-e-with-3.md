My earlier reply included two totals I added up by hand (about 55,000 and over 20,000). The script didn't compute them, so please disregard them. Here is the answer with every figure filled in by the script. The checked answer of record, sealed `b14014378d83`, is saved at `files/margins_2026-07.md` with the full product table and every left-out order.

# July 2026 product margins

**Warnings:** none

The export has records on every day of July, so the month is complete.

## Lost money: none
No product sold below its cost in July (below cost: none). The lowest margin is KK-MUG-2ND (seconds mugs), at 38.4%, still positive: 1,203.46 margin on 3,132.66.

## Made money
Every product with a known cost made a positive gross margin (full table in `files/margins_2026-07.md`). The largest in money:
- SV-LMP-MOS (Ceramic Table Lamp - Moss): 8,945.71 margin on 120 units
- SV-RUG-200 (Jute Rug - 200x300 cm): 8,783.94 margin on 53 units
- BW-THR-CHR (Wool Throw - Charcoal): 7,329.44 margin on 126 units
- SV-LMP-CHK (Ceramic Table Lamp - Chalk): 7,132.68 margin on 95 units
- BW-THR-FOR (Wool Throw - Forest): 6,865.70 margin on 119 units

## Can't tell: cost unknown
These sold in July but have no usable cost, so their margin is unknown (not zero): (no SKU) Gift Wrapping, (no SKU) Unique Handthrown Bowl - Large, (no SKU) Unique Handthrown Bowl - Medium, (no SKU) Unique Handthrown Bowl - Small, HT-OSB-L, HT-OSB-M, HT-OSB-S, KK-PIC-BLU, KK-PIC-RED, LN-NAP-OT, LN-NAP-SG.

- (no SKU) Gift Wrapping: 158 units, 527.85 revenue without VAT (no SKU and no Cost per item)
- (no SKU) Unique Handthrown Bowl - Large: 28 units, 2,104.43 revenue without VAT (no SKU on the order lines or in the products export; the products export does have a cost on this variant, but without a SKU it cannot be matched)
- (no SKU) Unique Handthrown Bowl - Medium: 27 units, 1,326.64 revenue without VAT (same as above)
- (no SKU) Unique Handthrown Bowl - Small: 17 units, 550.23 revenue without VAT (same as above)
- HT-OSB-L: 108 units, 5,855.57 revenue without VAT (in the products export, Cost per item empty)
- HT-OSB-M: 168 units, 6,275.56 revenue without VAT (in the products export, Cost per item empty)
- HT-OSB-S: 167 units, 4,170.92 revenue without VAT (in the products export, Cost per item empty)
- KK-PIC-BLU: 204 units, 10,208.60 revenue without VAT (not in the products export at all)
- KK-PIC-RED: 201 units, 10,050.49 revenue without VAT (not in the products export at all)
- LN-NAP-OT: 227 units, 6,620.75 revenue without VAT (sold under this SKU; the products export has Oat napkins as LIN-NAP-OAT-4 instead)
- LN-NAP-SG: 231 units, 6,747.49 revenue without VAT (sold under this SKU; the products export has Sage napkins as LIN-NAP-SAGE-4 instead)

Please send the costs for these. For the napkins: are LN-NAP-OT / LIN-NAP-OAT-4 and LN-NAP-SG / LIN-NAP-SAGE-4 the same products under two SKUs? I have not used the LIN- costs until you confirm. Products in the cost sheet with no July sales: KK-XMAS-6, LIN-NAP-OAT-4, LIN-NAP-SAGE-4, LN-BTW-SEA, LN-BTW-SND.

## Orders left out
134 orders left out; each one, with its reason (cancelled, partly paid, test), is listed in `files/margins_2026-07.md`.

## Not spread over products
These margins are product revenue minus product cost. Not in them: 41,764.43 in discounts, 26,538.33 in refunds and 6,950.00 in tips and gift cards sold (not products). Shipping, payment fees and ad spend are not in them either.

6103 orders had VAT inside their prices; their own tax was taken out of their lines. VAT removed: each order's own tax, where its prices include it. The figures cover 6516 orders.

## All products
The table of every product, and every order number left out, is in `files/margins_2026-07.md`.

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
Until you confirm these, the figures use the usual answers; a different answer changes them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- Does a sale count when it is paid, or only once it is shipped?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
