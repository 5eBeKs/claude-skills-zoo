# September 2026 sales, Shopify basis (EUR)

Source: `files/orders_export.csv` + `files/payment_transactions_export.csv` (exported through 4 Oct 2026).
The period is 1–30 Sep 2026 in store time (Europe/Amsterdam, +02:00).

## How the figures are built

Shopify's sales report works like this:
- **Sales** are dated by when the order was created.
- **Returns and cancellations** are dated by when the refund or cancellation happened, not by the order date.
- **All prices include VAT.** Shopify takes the VAT out, so gross sales, discounts, returns and shipping are ex-VAT. VAT is shown on its own line.

| Line | Amount | Notes |
|---|---:|---|
| Gross sales | 648,850.19 | 7,483 orders, 18,729 product units |
| Discounts | −23,314.23 | Codes (WELCOME10, AUTUMN20, SUMMER15, …), automatic discounts, and 100% on €0 replacement/staff orders |
| Returns | −25,740.89 | Refunds and cancellations dated in September (401 orders, some from July/August) |
| **Net sales** | **599,795.07** | |
| Shipping | 37,170.20 | Net of shipping discounts and refunded shipping, ex-VAT |
| Duties | 3,653.11 | US / CH orders |
| Taxes (VAT) | 122,273.52 | |
| **Total sales** | **762,891.90** | |

### Estimated extra returns (not in the table above)
There are €22.5k of refunds on PayPal, Klarna and bank-transfer orders that the exports don't date, because only card/iDEAL
(Shopify Payments) refunds have dates. The card refunds give a timing pattern. Applied to the undated refunds, it suggests about
**€9.4k incl. VAT (≈ €8.0k returns + €1.5k VAT)** of them fall in September. That would make:
net sales ≈ **591.8k** and total sales ≈ **753.4k**. Shopify's own Sales report (Analytics → Reports → "Sales over time",
Sep 2026) will have the exact figure.

## What is included
- All channels: online store (6,997 orders), POS Showroom Utrecht (124), draft/B2B orders (30, €21.2k), and
  an app sales channel with ID 3890849 (332 orders, €29.8k).
- Unpaid orders count as sales: 46 September orders still owe €13,225.70 (bank transfer, Klarna, Net 30 invoices).
- Orders paid with gift cards (151) count as normal sales.
- Voided orders are cancelled Klarna/authorisation orders. They count as a sale on the order date and as a reversal on the cancellation date.
  11 August orders cancelled in September reduce September's figure (€706). 2 September orders cancelled in October stay in September.
- Orders tagged `duplicate` (2) or `test` (3 × €0 with STAFF100) are real orders to Shopify. They net to zero.

## What is excluded
- **Gift card sales**: €8,100 (141 cards). These are a liability until redeemed, not revenue.
- **Tips**: €26.50 on 11 orders.
- **Chargebacks/disputes** (−€367 net in September) and the €5,000 Shopify Payments reserve. These affect payouts, not sales.
- **Payment fees.** Also, payouts won't match sales: they only cover Shopify Payments, not PayPal/Klarna/bank, and they arrive on a delay.
- Test orders on the test gateway (only 2, both in July).

## VAT by rate (September orders, before returns)
| Tax | Orders | Net product sales | Shipping | VAT |
|---|---:|---:|---:|---:|
| NL BTW 21% | 3,057 | 260,991.17 | 6,857.54 | 56,251.40 |
| DE MwSt 19% | 1,299 | 109,657.95 | 7,558.28 | 22,274.76 |
| BE BTW 21% | 737 | 57,225.24 | 2,804.36 | 12,608.42 |
| GB VAT 20% | 537 | 39,834.15 | 5,265.03 | 9,023.29 |
| FR TVA 20% | 358 | 30,798.57 | 2,048.81 | 6,570.92 |
| No tax (US / exempt) | 337 | 30,259.97 | 5,241.96 | 0.00 |
| CH MWST 8.1% | 196 | 16,626.28 | 2,911.10 | 1,582.73 |
| AT USt 20% | 190 | 13,797.12 | 1,124.28 | 2,984.96 |
| IT IVA 22% | 148 | 12,682.35 | 835.60 | 2,973.58 |
| ES IVA 21% | 129 | 11,363.65 | 732.50 | 2,540.57 |
| DK Moms 25% | 106 | 9,842.48 | 553.28 | 2,598.89 |
| SE Moms 25% | 124 | 8,746.75 | 687.08 | 2,358.39 |
| IE VAT 23% | 88 | 8,329.47 | 445.85 | 2,018.36 |
| PL VAT 23% | 65 | 6,136.93 | 312.30 | 1,483.47 |
| FI ALV 25.5% | 77 | 5,980.31 | 387.81 | 1,623.79 |
| LU TVA 17% | 35 | 3,263.57 | 170.00 | 583.84 |

The VAT split between products and shipping is worked out from each order's rate, because the export only gives total tax per order.

