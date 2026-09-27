<!-- numbers-c-claude-opus-5-5 / numbers-payouts-c / without the plugin / run 3: passed -->

Nothing is missing. I tied every August order to the payout file to the penny. The gap comes from money that doesn't go through Shopify Payments, Shopify's own deductions, and payout timing.

**August orders to August bank deposits**

| | £ |
|---|---:|
| August orders, total as the customer paid (1,640 orders) | **113,314.07** |
| Cancelled/voided orders (6), never charged | −887.45 |
| Test orders (8: tagged "test" or paid through the test gateway), never charged | −912.85 |
| **Real August orders** | **111,513.77** |
| Paid by PayPal (132 orders). This goes to your PayPal account, not the Shopify payout | −7,706.80 |
| Paid by gift card (full or part). That cash came in when the gift cards were sold, earlier | −4,211.20 |
| **Card charges through Shopify Payments** | **99,595.77** |
| Shopify processing fees | −2,019.03 |
| Refunds paid out in August (£1,668.90 on August orders, £1,093.51 on June/July orders) | −2,762.41 |
| Chargebacks (3 disputes: £223.95 plus £45 dispute fees) | −268.95 |
| Small Shopify adjustments | +2.35 |
| Late-August activity paid out 1 Sept (still "in transit") | −6,075.32 |
| Late-July activity paid out in early August | +5,924.13 |
| **Shopify payouts dated August = money that reached the bank** | **94,396.54** ✓ |

**What I checked**
- **Charges:** every Shopify Payments order has exactly one charge for the exact order total. No sales are missing from the payouts and none are counted twice.
- **Fees:** all 3,945 fees match 1.5% + 25p (Visa/Mastercard) or 2.5% + 25p (Amex). There are no overcharges.
- **Refunds:** every refund in the payout file matches the refunded amount on its order.

**Where to follow up**
1. **PayPal, about £7,680 after £26 of refunds.** This is the biggest real cash item. Check that it's still sitting in PayPal or was moved to the bank separately. It will never show up in Shopify payouts.
2. **The £6,075 in transit** should have arrived in early September.
3. **The 3 August chargebacks** (#32603, #32955, #33706) are still open. In June and July you won 2 out of 3, so some of that £224 may come back. The £15 fee per dispute is only refunded if you win.

**Which "sales" figure are you comparing?** Using your reporting rules (count only shipped orders, exclude VAT and shipping, take off refunds), August revenue is **£85,086.86**, which is *below* the £94.4k banked. So the gap you noticed must be based on gross sales, as the customer paid. The bank figure also still includes about £17.8k of VAT that belongs to HMRC. It also includes £4,778 for 70 August pre-orders: they were paid for but haven't shipped, so they aren't sales under your rules yet.
