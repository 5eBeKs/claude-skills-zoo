<!-- numbers-claude-opus-5-5 / numbers-margins / without the plugin / run 1: passed -->

**Only one product loses money: the Steel Strainer (STR-STL-001).** It sells for €6.50 including VAT, which is €5.46 after VAT. It costs €7.10, so you lose about **€1.64 on every unit**.

In August you sold 20 strainers. Across those that comes to a **loss of about €34**, a bit more than 20 × €1.64 because 2 of them were bought with the WELCOME10 discount (10% off). I left out the test order (#1013), the voided order (#1021) and the fully refunded order (#1042).

Per-unit margin for every product in `cogs.csv`:

| Product | Price incl. VAT | Price excl. VAT | Unit cost | Margin |
|---|---|---|---|---|
| Steel Strainer | 6.50 | 5.46 | 7.10 | **−1.64** |
| Black Tea 100g | 11.50 | 9.66 | 3.80 | +5.86 |
| Green Tea 100g | 12.90 | 10.84 | 4.10 | +6.74 |
| Oolong 50g | 16.00 | 13.45 | 6.20 | +7.25 |
| Ceramic Cup | 18.00 | 15.13 | 7.50 | +7.63 |
| Glass Teapot 600ml | 34.00 | 28.57 | 15.90 | +12.67 |
| Matcha 30g | 24.00 | 20.17 | 9.70 | +10.47 |

Everything except the strainer keeps a margin of at least 43% of its ex-VAT price. So a 10% discount or typical payment fees won't push any of them into a loss.

**What I couldn't check:**
- **Gift Set (SET-GFT-001) isn't in `cogs.csv`.** You sold 16 in August at €41.18 each after VAT. It only loses money if it costs you more than about €41, or about €37 when WELCOME10 is used. If it's a bundle of the items above, its cost is probably well below that, but I'd need the real number.
- **Payment fees and shipping costs aren't in either file.** One order (#1054) was just 2 strainers for €13 plus €4.90 shipping, which probably lost money overall. Most other strainer sales came in orders alongside other products.

To fix the strainer, the price would need to be at least about €8.45 including VAT just to break even, before fees.
