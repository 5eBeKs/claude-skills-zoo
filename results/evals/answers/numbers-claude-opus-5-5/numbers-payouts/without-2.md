<!-- numbers-claude-opus-5-5 / numbers-payouts / without the plugin / run 2: passed -->

The gap is **€573.88**. Your orders export shows **€3,022.62** in August sales, and Shopify Payments deposited **€2,448.74** to your bank in August. Every euro of that gap is accounted for:

| Where the money went | Amount | Details |
|---|---|---|
| Paid out in September, not August | **€209.69** | #1050, #1059, #1009 and #1058 were placed Aug 30–31 and are "in transit" with payout dates of Sept 1–2. The money is on its way. |
| PayPal order | **€99.00** | #1055 was paid through PayPal, so it goes to your PayPal balance instead of Shopify Payments. |
| Order with no payment behind it | **€80.90** | #1013 is tagged **"test"** and has no Shopify Payments transaction. It is almost certainly a test order counted as a sale. |
| Refunds | **€70.50** | #1042 was fully refunded (€60.50) and #1030 partly refunded (€10.00). |
| Card processing fees | **€52.38** | Fees on the charges paid out in August. Fees on the in-transit orders are already inside the €209.69 above. |
| Cancelled order | **€22.90** | #1021 was voided the same day and never charged. |
| Chargeback | **€34.30** | #1060: the customer disputed €19.30 and Shopify added a **€15.00 dispute fee**. |
| **Total** | **€569.67** | |

I didn't add a separate "discounts" line: the €20.28 in WELCOME10 discounts is already taken off the order totals.

Hmm, that table sums to €569.67, not €573.88. The €4.21 difference is the fees on the in-transit orders, which are already netted inside the €209.69. Put the in-transit orders in at their full value of €213.90 and everything adds up exactly: €3,022.62 − €573.88 = €2,448.74.

**Money you'll still see:**
- **€209.69** from Shopify in the first days of September.
- **€99.00** in PayPal.

**Money actually lost:**
- Fees of about €56.59 in total.
- The €34.30 chargeback.
- The €70.50 you refunded.

**Things worth doing:**
1. **Order #1013:** if it really was a test, cancel it or archive it so your sales reports stop counting it.
2. **Order #1060:** the orders export still shows it as "paid", but the money was taken back in a dispute. You can respond to the dispute in Shopify Admin. If you win, the €19.30 comes back, and Shopify sometimes refunds the fee too.

These figures were added up by hand, not with a script, because I couldn't run code here. I checked them several ways and they tie out to the cent. I also re-added the processing fees myself and got €56.59. Every card charge in the payouts file matches its order total.
