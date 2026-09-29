September 2026 total sales as Shopify reports them come to about **€763k**, from 7,483 orders and 18,729 units (not counting gift cards). The file isn't enough to state an exact final figure, because Shopify counts refunds by the date they were made and the order export doesn't record that for PayPal, Klarna or bank refunds. That means the figure is likely nearer **€753k**.

## September sales, set out like Shopify's Sales report
Dates are 1–30 Sep, shop time (UTC+2). Amounts in EUR.

| Line | Amount |
|---|---:|
| Gross sales | 648,837.41 |
| Discounts | −23,307.55 |
| Returns (the ones the files can date) | −25,626.91 |
| **Net sales** | **599,902.96** |
| Shipping | 37,098.62 |
| Duties | 3,615.78 |
| Taxes | 122,273.49 |
| **Total sales** | **762,890.85** |

**Returns are understated.** There are €22.4k of PayPal, Klarna and bank refunds on July–September orders whose refund date isn't in the export. Going by how quickly card refunds usually happen, about €9.4k of that (VAT included) probably happened in September. That would bring total sales to roughly **€753.5k**. The exact number is in Shopify under Analytics → Reports → Total sales, September. The other lines should match it to within rounding.

## What's in the figures
- **VAT:** your prices include VAT, so Shopify takes it out of gross sales and shows it on the Taxes line. The rates are the destination-country rates (NL 21%, DE 19%, BE 21%, GB 20%, CH 8.1% and others). US orders have no VAT; they pay duties instead, which Shopify includes in total sales.
- **Shipping** is shown without VAT and after free-shipping codes. The €1,056.70 of shipping discounts is taken off shipping, not the Discounts line.
- **Discounts:** mostly WELCOME10, SUMMER15, AUTUMN20 and VIP5.
- **Sales channels (order totals, VAT included):**
  - Online store: 6,997 orders, €739,910
  - A sales channel that appears only as the number `3890849`: 332 orders, €30,085. Please confirm which marketplace or app this is.
  - Showroom Utrecht (in-store): 124 orders, €11,545
  - Orders entered manually in Shopify: 30 orders, €21,214. Of these, 15 are wholesale orders to restaurants/cafés (tagged "b2b, horeca", €20,062) on 30-day payment terms.
- **Some of this isn't paid yet.** Shopify counts an order as a sale when it's placed. There are 26 orders (€12,256) still awaiting payment, including 8 of the wholesale invoices (€9,884). Another 14 orders (€876) have been authorized but not yet charged.
- **Cancellations:** 121 September orders were cancelled in September. Each appears once as a sale and once as a return, so they cancel out. 8 more were cancelled in October and will show as October returns.
- **Not included:**
  - €8,100 of gift cards sold. Shopify treats these as money owed to customers, not sales. Orders paid with gift cards do count.
  - €26.50 of tips.
  - No test-mode orders fell in September.
  - 6 free replacement orders and 3 staff orders using STAFF100 are in the report at €0.

## Two warnings for the bookkeeper
1. **This won't match the bank or Shopify payouts.** Payouts only cover card, Apple Pay and iDEAL payments taken through Shopify, after fees. September's payouts also include a failed August payout paid again on 2 Sep (€14,902), €5,000 of held-back funds released on 21 Sep, and chargebacks.
2. **Some splits are estimated.** The export doesn't break VAT down between products and shipping, or refunds between items, shipping and VAT. I split them using each order's VAT rate, which could move some lines by a few euros. The order figures reconcile to order totals to the cent, apart from the tips.

The export runs to 4 October, so all of September is covered.
