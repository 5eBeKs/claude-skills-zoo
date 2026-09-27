# August 2026: summary

In short, it was a solid month. You had 58 real orders and about €2.9k in sales. You kept about €2.76k after refunds, a chargeback and payment fees. All amounts are in EUR and include VAT unless marked "ex-VAT". The export shows VAT at 19%, and it's included in your prices and shipping.

## Key numbers for your accountant

| | Amount |
|---|---|
| **Orders** | **58** (export has 60 rows. I left out 1 voided and 1 test order, see below) |
| Product sales before discounts | €2,787.20 |
| Discounts (WELCOME10, 6 orders) | −€20.28 |
| Shipping charged | €151.90 |
| **Charged to customers** | **€2,918.82** (of which VAT €466.00) |
| **Refunds** | **−€70.50** (#1042 fully refunded, €60.50. #1030 partly refunded, €10.00) |
| **Net sales after refunds** | **€2,848.32**, which is **€2,393.55 ex-VAT** (VAT ≈ €454.77) |
| Chargeback lost (#1060) | −€19.30 |
| Payment fees | −€71.59 (€56.59 Shopify Payments + €15.00 chargeback fee) |
| **What you kept** | **€2,757.43** (before the PayPal fee on one order, which isn't in these files) |
| **Average order value** | **€50.32** (€2,918.82 ÷ 58). After refunds: €49.97 per order you kept |
| **Units sold** | **134** (132 after the fully refunded order) |

### Where the money you kept actually is
- **€2,448.74** reached your bank in August (Shopify Payments payouts, 3 to 31 Aug).
- **€209.69** was still on its way on 31 Aug. It lands on 1 and 2 September (orders #1050, #1059, #1009, #1058).
- **€99.00** came through PayPal (order #1055). It's not in the Shopify payout file, so check PayPal for the fee.

These add up to €2,757.43.

## Best products

| Product | Units kept | Sales (incl. VAT) | Margin per unit ex-VAT |
|---|---|---|---|
| Gift Set | 16 | €784.00 | unknown (no cost in cogs.csv) |
| Glass Teapot 600ml | 19 | €646.00 | €12.67 (44%) |
| Black Tea 100g | 26 | €299.00 | €5.86 (61%) |
| Oolong 50g | 16 | €256.00 | €7.25 (54%) |
| Ceramic Cup | 14 | €252.00 | €7.63 (50%) |
| Matcha 30g | 8 | €192.00 | €10.47 (52%) |
| Green Tea 100g | 13 | €167.70 | €6.74 (62%) |
| Steel Strainer | 20 | €130.00 | **−€1.64 (−30%)** |

The Gift Set brings in the most money, and the Glass Teapot earns you the most profit among the products with a known cost. Black Tea sells the most units.

## Things I found that you should know

1. **You lose money on the Steel Strainer.** It sells for €6.50 (€5.46 ex-VAT), but cogs.csv puts its cost at €7.10. That's about €33 lost this month on 20 units. Either the price or the cost figure is wrong.
2. **The Gift Set has no cost in cogs.csv.** Your top seller has an unknown margin. Please add its cost.
3. **Chargeback on #1060 (18 Aug).** The customer disputed €19.30 and Shopify also charged a €15 fee, so you're €34.30 down. The Shopify order export still shows this order as "paid". Check in Shopify admin whether you can still contest it.
4. **I left out order #1013 (€80.90).** It's tagged "test" and no money for it appears in your payouts. If it was a real sale, tell me and I'll add it back.
5. **I left out order #1021 (€22.90).** It was voided and cancelled the same day, so no money changed hands.

Quick note on method: costs in cogs.csv are assumed to be ex-VAT. Margins use list prices before the small WELCOME10 discounts. Everything above comes from orders_export.csv, payout_transactions.csv and cogs.csv. Nothing else was used.
