<!-- numbers-claude-opus-5-5 / numbers-margins / without the plugin / run 2: passed -->

**Only one product clearly loses money: the Steel Strainer (STR-STL-001).** It sells for €6.50 including VAT, which is €5.46 after taking out the 19%. It costs €7.10, so every strainer sold loses about €1.64, even at full price.

In August you sold 20 strainers. They lost about **€33.85** in total, including a 10% WELCOME10 discount on one order (#1043).

A second product can't be checked. **Gift Set (SET-GFT-001) has no row in cogs.csv.** It sells for €41.18 after VAT (€37.06 with WELCOME10), and 16 were sold in August. It's one of your biggest sellers, so it's worth adding its cost. It loses money only if its cost is above about €37–41, which could happen if it bundles a teapot or several items.

Everything else makes money, even with the 10% discount:

| Product | Price after VAT | Unit cost | Margin |
|---|---|---|---|
| Green Tea 100g | €10.84 | €4.10 | €6.74 |
| Black Tea 100g | €9.66 | €3.80 | €5.86 |
| Oolong 50g | €13.45 | €6.20 | €7.25 |
| Matcha 30g | €20.17 | €9.70 | €10.47 |
| Ceramic Cup | €15.13 | €7.50 | €7.63 |
| Glass Teapot 600ml | €28.57 | €15.90 | €12.67 |
| Steel Strainer | €5.46 | €7.10 | **−€1.64** |

**What I left out of the unit counts:**
- #1013, because it's tagged `test`
- #1021, because it was voided
- #1042, because it was fully refunded

None of these three contained a strainer, so leaving them out doesn't change the strainer figure.

**What this doesn't include:** shipping, payment fees and packaging, because the files don't have those costs. Once you add them, the thinner products (Black Tea with a €5.86 margin, and the teas bought on their own in general) may make much less on small orders. The export also shows most orders under €40 pay €4.90 shipping, so shipping is partly covered but the real cost is unknown.
