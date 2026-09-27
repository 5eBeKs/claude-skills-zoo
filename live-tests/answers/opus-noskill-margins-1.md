# August product profitability

## Short answer

- **Steel Strainer loses money on every unit.** You sell it for €6.50 including VAT, which is €5.46 after VAT, but it costs you €7.10. In August 20 units lost you **€36.74**, before postage.
- **Everything else in the cost sheet makes money.** Glass Teapot earns the most per unit (€12) and the most in total (€229). The teas and the cup keep about 40–60% of the ex-VAT price.
- **I can't tell you about the Gift Set.** It's your biggest seller by revenue (€642 ex VAT), but `SET-GFT-001` isn't in the cost sheet. It made money in August only if one set costs you less than about **€37**.
- **Shipping may be the real leak.** You shipped 58 parcels and collected about €120 net for postage (27 orders shipped free over €40). I don't have your carrier or packaging cost. At €5 per parcel all-in, shipping would cost you about €170 net for the month.

## Profit by product, August 2026

These figures are ex VAT and after discounts, refunds, the chargeback, and actual Shopify Payments fees. They are **before** postage, packaging, ads and fixed costs.

| Product | Units | Net revenue | Product cost | Fees | **Profit** | Margin | Per unit |
|---|---:|---:|---:|---:|---:|---:|---:|
| Glass Teapot 600ml | 19 | €542.86 | €302.10 | €11.31 | **€229.45** | 42% | €12.08 |
| Black Tea 100g | 27 | €251.26 | €102.60 | €6.86 | **€141.80** | 56% | €5.25 |
| Ceramic Cup | 14 | €210.25 | €105.00 | €5.27 | **€99.98** | 48% | €7.14 |
| Green Tea 100g | 13 | €138.76 | €53.30 | €3.76 | **€81.69** | 59% | €6.28 |
| Matcha 30g | 8 | €161.34 | €77.60 | €3.68 | **€80.07** | 50% | €10.01 |
| Oolong 50g | 16 | €198.99 | €99.20 | €19.77¹ | **€80.02** | 40% | €5.00 |
| Steel Strainer | 20 | €108.15 | €142.00 | €2.89 | **−€36.74** | −34% | −€1.84 |
| **Subtotal (known costs)** | | **€1,611.62** | **€881.80** | **€53.54** | **€676.27** | 42% | |
| Gift Set | 17 | €642.18 | **unknown** | €14.29 | €627.90 *minus set cost* | ? | €36.94 *minus set cost* |

¹ Includes a lost chargeback on order #1060 (Oolong): €15 dispute fee, and the tea shipped but wasn't paid for. Without it, Oolong made €101.62 (51%).

## Profit per unit at full price

| Product | Price incl. VAT | Net of VAT | Your cost | Card fee (1.5%) | Profit/unit | Margin |
|---|---:|---:|---:|---:|---:|---:|
| Green Tea 100g | €12.90 | €10.84 | €4.10 | €0.19 | €6.55 | 60% |
| Black Tea 100g | €11.50 | €9.66 | €3.80 | €0.17 | €5.69 | 59% |
| Oolong 50g | €16.00 | €13.45 | €6.20 | €0.24 | €7.01 | 52% |
| Matcha 30g | €24.00 | €20.17 | €9.70 | €0.36 | €10.11 | 50% |
| Ceramic Cup | €18.00 | €15.13 | €7.50 | €0.27 | €7.36 | 49% |
| Glass Teapot 600ml | €34.00 | €28.57 | €15.90 | €0.51 | €12.16 | 43% |
| Steel Strainer | €6.50 | €5.46 | €7.10 | €0.10 | **−€1.74** | **−32%** |
| Gift Set | €49.00 | €41.18 | ? | €0.74 | €40.44 − cost | ? |

Shopify also charges a fixed €0.25 per order. That's why small single-item orders keep less.

## Orders that lost money

- **#1060** (Oolong): chargeback. You lost the €19.30 payment, the tea, and a €15 dispute fee, so about **−€21.74** on this order.
- **#1007** (3 strainers): **−€1.42** before the parcel was even paid for.
- **#1054** (2 strainers): **+€0.32** before postage, so a loss once the parcel is paid for.
- **#1042** (Black Tea + Gift Set): fully refunded after it shipped. That's **−€4.96** (tea cost and the card fee Shopify keeps), plus the Gift Set cost if it didn't come back.

## What I'd do

1. **Fix the Steel Strainer.** First check that €7.10 is really the unit cost. If it is:
   - At €6.50 you lose money on every one.
   - Break-even is about **€8.60** incl. VAT.
   - For a margin like the teapot (about 42%), price it around **€15**. At €12 it would keep only about 28%.
   - Or keep it cheap only as an add-on with tea. Strainer-only orders (#1007, #1054) lose money outright.
2. **Send me the Gift Set cost** (contents + box). It's 28% of your net revenue, so it decides whether August was a good month.
3. **Send me your average cost per parcel** (carrier + packaging). Then I can say whether €4.90 shipping and free shipping from €40 cover it. A €12.90 green tea order keeps about €10 before postage, so it gets thin if a parcel costs €6–7.
4. **Check chargeback #1060.** See whether it can still be contested, or whether the order had fraud signs. One of these wipes out the profit from about four tea orders.

## How I calculated this, and what to check

- **Files:** I used the orders export and the cost sheet. I also used `payout_transactions.csv`, which was in the same folder, for the real payment fees, refunds and the chargeback. Every card fee matches 1.5% + €0.25 per charge, and every order total matches its payout amount.
- **Left out:**
  - #1013, tagged "test". There's no payment for it in the payouts; it was €80.90 and looked like a real sale.
  - #1021, voided.
- **VAT:** I removed 19% from all prices and from shipping. The Taxes column in the export matches this exactly.
- **Discounts:** WELCOME10 discounts (€20.28 incl. VAT) are spread across the products in each order.
- **PayPal order #1055** (€99): its PayPal fee isn't in these files, so that order's profit is overstated by the fee, probably €3–4.
- **Refund #1042:** I assumed the goods did not come back into sellable stock. If they did, Black Tea gains €3.80 and the Gift Set cost is recovered.
- **Not included:** postage, packaging, ads, Shopify subscription, apps, rent, your time. The "profit" above is what each product contributes toward those costs.
