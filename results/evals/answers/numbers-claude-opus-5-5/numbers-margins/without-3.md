<!-- numbers-claude-opus-5-5 / numbers-margins / without the plugin / run 3: passed -->

**Only the Steel Strainer (STR-STL-001) loses money.** It sells for €6.50 including VAT, which is €5.46 after the 19% is taken out. It costs you €7.10, so you lose about €1.64 on every one you sell.

**Unit economics (prices net of VAT):**

| Product | Price incl. VAT | Price excl. VAT | Unit cost | Profit per unit | Margin |
|---|---|---|---|---|---|
| **Steel Strainer** | 6.50 | 5.46 | 7.10 | **−1.64** | **−30%** |
| Glass Teapot 600ml | 34.00 | 28.57 | 15.90 | 12.67 | 44% |
| Ceramic Cup | 18.00 | 15.13 | 7.50 | 7.63 | 50% |
| Matcha 30g | 24.00 | 20.17 | 9.70 | 10.47 | 52% |
| Oolong 50g | 16.00 | 13.45 | 6.20 | 7.25 | 54% |
| Black Tea 100g | 11.50 | 9.66 | 3.80 | 5.86 | 61% |
| Green Tea 100g | 12.90 | 10.84 | 4.10 | 6.74 | 62% |
| Gift Set | 49.00 | 41.18 | **not in cogs.csv** | ? | ? |

**What the strainer cost you in August:** you sold 20 units in 13 orders. Revenue excluding VAT was about €108 after one 10% WELCOME10 discount, and the units cost €142, so you lost about **€34** on them. Two orders contained nothing but strainers (#1007 and #1054).

**Open question: the Gift Set.** It's one of your biggest sellers, with 16 units kept after refunds. But SET-GFT-001 isn't in `cogs.csv`, so I can't tell whether it makes money. It breaks even at a unit cost of about €41.18, or about €37 for orders that used WELCOME10. If the set bundles several of your products (for example teapot + cups + tea), its cost could get close to that, so please check it.

**How I got these numbers:**
- I left out order #1013 (tagged `test`), #1021 (voided) and #1042 (fully refunded).
- #1030 had a partial €10 refund on a Gift Set. That doesn't change any of the per-unit numbers above.
- WELCOME10 takes 10% off. That doesn't push any other product below zero; the Teapot has the thinnest margin and still keeps about 37% after the discount.
- I didn't include shipping, payment fees or packaging, because the files don't have those costs. Some orders were charged €4.90 shipping and others shipped free. Your real shipping cost could make small orders unprofitable too, and strainer-only orders would be hit hardest.
