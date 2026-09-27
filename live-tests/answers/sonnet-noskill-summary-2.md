# August Orders Summary (for accountant)

Source: `orders_export.csv` (Shopify orders export, all amounts in EUR). Covers orders created 2026‑08‑01 through 2026‑08‑31.

## Headline numbers

| Metric | Value |
|---|---|
| Orders charged | **59** |
| What we charged (gross, incl. VAT & shipping) | **€2,999.72** |
| Refunds issued | **€70.50** |
| What we kept (net of refunds) | **€2,929.22** |
| Average order value (gross) | **€50.84** |
| Average order value (net of refunds) | **€49.65** |
| Units sold | **139** |

Of the €2,999.72 charged, about €478.92 is VAT embedded in the listed prices (Shopify's "Taxes" column — your prices are tax‑inclusive, so this is not an extra charge on top, just the tax portion within it). €151.90 of the total was shipping fees collected from customers, and €20.28 was given away via discount codes (all `WELCOME10`, used on 6 orders). None of this includes Shopify/payment‑processor fees, since those aren't in this export.

## Refunds detail

| Order | Status | Order total | Refunded |
|---|---|---|---|
| #1030 | Partially refunded | €49.00 | €10.00 |
| #1042 | Fully refunded | €60.50 | €60.50 |

Total refunded: **€70.50** (2 orders out of 60 placed).

## Orders excluded from the count above

- **#1021** — status "voided", cancelled ~2 hours after it was placed. No payment was ever captured (Shopify voided the authorization), so it's not counted as a charged order and isn't in any of the totals above. If you had 60 order numbers this month, this is the 60th — it was a no-charge cancellation.

## Best-selling products

By **revenue** (what actually drove your sales):

| Product | Revenue | Units sold |
|---|---|---|
| Gift Set | €833.00 | 17 |
| Glass Teapot 600ml | €646.00 | 19 |
| Black Tea 100g | €310.50 | 27 |
| Oolong 50g | €288.00 | 18 |
| Ceramic Cup | €288.00 | 16 |
| Matcha 30g | €192.00 | 8 |
| Green Tea 100g | €180.60 | 14 |
| Steel Strainer | €130.00 | 20 |

**Top seller by revenue: Gift Set** (€833.00). **Top seller by units: Black Tea 100g** (27 units), followed closely by Steel Strainer (20) and Glass Teapot 600ml (19).

## One thing to double-check before you send this to your accountant

Order **#1013** (€80.90, paid, not refunded) is tagged **"test"** in the export. It looks like a normal customer order (Green Tea 100g, 2x Ceramic Cup, 2x Oolong 50g) and I've left it in the totals above since it shows as a real, paid, non-refunded transaction — but the tag suggests it might have been a test/internal order rather than a genuine sale. If you confirm it wasn't a real customer purchase, subtract it from the figures above:
- Orders charged: 58 (not 59)
- Gross charged: €2,918.82
- Net kept: €2,848.32
- Units sold: 134

Worth a quick check with whoever placed that order.
