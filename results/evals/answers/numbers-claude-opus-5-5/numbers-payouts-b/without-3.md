<!-- numbers-claude-opus-5-5 / numbers-payouts-b / without the plugin / run 3: passed -->

Your August orders total **$4,335.23** and the payouts dated in August total **$3,713.86**. That's a gap of **$621.37**, and every cent of it is accounted for. About two-thirds is timing, fees, or money that was never card revenue. The part you actually lost is refunds plus one open chargeback.

A caveat on method: I had no way to run code, so these totals were added up by hand. I checked them several ways (every row's net equals its amount minus its fee, subtotal + shipping + tax − discount equals the order totals, and the payout totals match). The bridge below comes to exactly $3,713.86.

| Reason | Effect on payout | Notes |
|---|---|---|
| **Timing: Aug 30–31 orders not paid out until September** | −280.94 | #2052, #2066, #2067 are "in transit" and arrive Sept 1–2 ($271.90 after fees) |
| **Timing: July 31 orders paid out in August** | +99.57 | #1998–#2000 landed in the Aug 3 payout |
| **Voided order** | −50.35 | #2008 was cancelled and never charged |
| **Test orders** | −79.25 | #2011 and #2044 went through "Bogus Gateway (for testing)", so no real money came in. They're probably inflating your sales reports, so check whether they should be deleted |
| **Gift card portion** | −20.00 | #2051 ($120.12): $20 was paid by gift card, so only $100.12 went through Shopify Payments |
| **Refunds** | −58.06 | #2038 fully refunded ($46.06), #2049 partially refunded ($12.00) |
| **Chargeback #2027** | −96.51 | $81.51 was pulled back plus a $15 dispute fee, with no reversal in the data. Check its status in Shopify admin and respond with evidence if it's still open |
| **Chargeback #2015** | 0.00 | $98.66 was debited on Aug 14 but came back on Aug 26 when you won the dispute |
| **Processing fees** | −136.18 | About 2.9% + $0.30 per charge |
| **Adjustment #2033** | +0.35 | A small credit from Shopify |
| **Total** | **−621.37** | 4,335.23 → 3,713.86 |

- **Timing (−$181.37 net)** isn't lost money. It comes out roughly even from month to month, but it will always make a calendar-month comparison look off.
- **Not real card sales ($149.60)**: the voided order, the test orders and the gift card portion show up in the orders export but were never going to be paid out. (The gift card money came in when the card was originally sold.)
- **Actual reductions ($290.40)**: refunds of $58.06, fees of $136.18 and the #2027 chargeback of $96.51. Only the chargeback is unusual.

Also, the $4,335.23 includes $293.03 of sales tax and $250.20 of shipping. The tax isn't your revenue to keep, so your real product sales for August were $3,792.00 (subtotal minus discounts).
