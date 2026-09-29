# September 2026 sales (Kade & Klei)

I rebuilt September the way Shopify's sales reports count it. Sales are booked on the order date, refunds and cancellations on the date they happened, and VAT is taken out of the sales figures because your prices include VAT. All amounts are in EUR, Amsterdam time.

## Shopify-style summary, 1–30 September

| Line | EUR |
|---|---:|
| Gross sales (excl. VAT) | 648,850.19 |
| Discounts | −23,306.80 |
| Returns (refunds and cancellations dated in September) | −24,657.57 |
| **Net sales** | **600,885.82** |
| Shipping charges (excl. VAT) | 36,346.55 |
| Duties (US and CH orders) | 3,582.38 |
| Taxes (VAT) | 122,311.26 |
| **Total sales** | **763,126.01** |

These rest on 7,483 orders placed in September, worth €802,753.75 at checkout including VAT.

**One gap to know about:** returns are not quite complete. The orders export only gives a total refunded amount per order, not the date of each refund. I dated refunds three ways:
- **Shopify Payments refunds:** dated from the payment transactions export.
- **Cancelled orders:** dated by the cancellation date.
- **Refunds paid through PayPal, Klarna or bank transfer that weren't cancellations:** these have no date. There are 292 of them, worth €22.5k, spread over July to September orders. Based on how long Shopify Payments refunds usually take, about €7.0k of that probably falls in September. That would bring net sales down to about **€595.3k** and total sales to about **€756.1k**.

For the exact figures, pull **Analytics → Reports → Finance summary (or "Total sales breakdown") for 1–30 Sep** in Shopify. It should match the table above except for those undated refunds.

## What's in the figures

- **Sales channels:** online store 6,997 orders (€739.9k), app channel "3890849" 332 orders (€30.1k), Utrecht showroom till 124 orders (€11.5k), draft orders 30 (€21.2k). I can't tell what the app channel is from the data; it may be a marketplace, so please confirm.
- **B2B:** 15 horeca orders (€20.1k) on 30-day payment terms. Some German and Belgian ones carry no VAT, which looks like reverse charge, so the bookkeeper should check.
- **Not yet paid:** Shopify counts a sale when the order is placed, not when it's paid. This includes 26 pending orders (€12.3k, bank transfer or manual payment), 14 Klarna orders authorised but not yet captured (€0.9k) and 6 partly paid ones (€0.4k).
- **Gift cards:** €8,100 of gift cards sold in September are **left out** of sales. They are a liability until someone spends them; orders paid with a gift card count as normal sales.
- **Zero-value orders:** 6 free replacement orders (€312 gross) and 3 internal test orders using the STAFF100 code (€202). Each adds the same amount to gross sales and to discounts, so the net effect is zero.
- **Two duplicate orders** were cancelled and refunded the same day. They appear in both gross sales and returns.
- **Returns include earlier orders:** refunds processed in September for July and August orders count against September, and refunds for September orders made in October count against October.
- **VAT is charged in 15 countries.** The largest amounts are NL €56.3k, DE €22.3k, BE €12.6k and GB €9.0k (full list available for the EU OSS VAT return). Swiss prices include 8.1% VAT. US orders carry no VAT, but customers paid €3.2k in duties; like the Swiss duties (€0.4k), this is money passed on, not revenue.
- **Currencies:** payments in GBP, USD and CHF are already converted to EUR in the export.
- **Not in sales:** chargebacks, Shopify's reserve holds and card fees. That's why the September payouts don't match these figures.

Two details from the data:
- **Test orders:** the orders paid with Shopify's test payment method and those marked as checkout tests are all from July and August, so they don't affect September.
- **Export dates:** the export runs to 4 October, which is later than today's date ([run date]). You may want to check where the file came from.
