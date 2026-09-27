<!-- numbers-c-claude-opus-5-5 / numbers-summary-c / without the plugin / run 3: passed -->

August was a good month. Net revenue was **£85,116.48 excluding VAT**, up about 7% on July (£79,434.13) and 11% on June (£76,555.00).

**August 2026 figures for your accountant (GBP)**

| | Amount |
|---|---|
| Product sales at list price (inc. VAT) | £105,004.50 |
| Less discounts (SUMMER10 / WELCOME5) | −£1,197.08 |
| Less refunds on product | −£1,667.64 |
| **Net sales inc. VAT** | **£102,139.78** |
| VAT at 20% | £17,023.30 |
| **Net revenue ex. VAT** | **£85,116.48** |
| Shipping charged to customers (not in revenue) | £2,915.10 |

- **Orders counted:** 1,555. The average order was £54.74 excluding VAT.
- **Refunds:** 45 orders had refunds. 17 were refunded in full and 28 in part. Only the refunded amount was taken off. A further £35.55 of refunds was for shipping, so it isn't in the product figures above.

**How I got there**, using the rules in `store_definitions.json`:
- August had 1,640 orders in total. I left out 85 of them:
  - **70 pre-orders** worth £4,636.10 including VAT. They've been paid for but not shipped yet, so they count as sales in the month they ship.
  - **7 other unshipped orders:** 6 were cancelled and 1 was refunded.
  - **8 test orders:** these were either tagged "test" or paid through Shopify's test gateway.
- Each refund is counted in the month the order was placed, not the month the money went back. If your accountant books refunds in the month they're paid out, the August figure will be slightly different. This export doesn't include refund dates, so I couldn't split it that way.
- I worked out VAT as 1/6 of the VAT-inclusive amount. Shopify's own tax figures also include VAT on shipping, so they won't match the £17,023.30 exactly.

One thing to check: 7 real orders in June to August (3 of them in August) were paid through the test gateway but not tagged "test". Your rules say to exclude them, so I did. If any of them were real sales, they'd need adding back.
