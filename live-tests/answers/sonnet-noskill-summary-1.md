# August Orders Summary

Source: `orders_export.csv` (Shopify orders export). All amounts in EUR.

## Key numbers for your accountant

| Metric | Value |
|---|---|
| Orders (counted) | 59 |
| Amount charged (gross, after discounts, before refunds) | **€2,999.72** |
| Refunds | **€70.50** |
| Net kept (charged − refunded) | **€2,929.22** |
| Average order value (gross) | €50.84 |
| Average order value (net of refunds) | €49.65 |
| Units sold | 139 |
| Discounts given (already subtracted from the charged total above) | €20.28 |

**Note on order count:** the file contains 60 order numbers, but order **#1021** was **voided and cancelled** the same day (no money was ever captured), so it's excluded from all totals above. If you'd rather have the raw count including it, that's 60 orders / 61 line items.

**Refunds detail:**
- **#1030** — partially refunded, €10.00 refunded on a €49.00 order.
- **#1042** — fully refunded, €60.50 refunded on a €60.50 order.

## Best products (August)

**By revenue:**
1. Gift Set — €833.00 (17 units)
2. Glass Teapot 600ml — €646.00 (19 units)
3. Black Tea 100g — €310.50 (27 units)

**By units sold:**
1. Black Tea 100g — 27 units
2. Steel Strainer — 20 units
3. Glass Teapot 600ml — 19 units

**Full breakdown (units sold, revenue):**

| Product | Units | Revenue |
|---|---|---|
| Black Tea 100g | 27 | €310.50 |
| Steel Strainer | 20 | €130.00 |
| Glass Teapot 600ml | 19 | €646.00 |
| Oolong 50g | 18 | €288.00 |
| Gift Set | 17 | €833.00 |
| Ceramic Cup | 16 | €288.00 |
| Green Tea 100g | 14 | €180.60 |
| Matcha 30g | 8 | €192.00 |

## Notes / assumptions

- "Amount charged" = the order **Total** column (post-discount, pre-refund), summed across the 59 valid orders — this matches what actually settled through your payment processor.
- Refunds are taken from the **Refunded Amount** column.
- Units sold and product revenue are computed from line items across the 59 valid orders (the voided order's single line item is excluded).
- Three orders used the discount code **WELCOME10**, totaling €20.28 in discounts — already reflected in the charged total, not deducted again.
