<!-- numbers-c-claude-opus-5-5 / numbers-payouts-c / without the plugin / run 2: passed -->

Nothing is missing. Every Shopify Payments charge in August matches its order to the penny, and every refund in the payout file matches a refund on an order. The gap is made up of money that was never going to reach this bank account, money Shopify deducted, and money that arrived in September.

**August orders: £113,314.07 billed to customers → £89,620.52 paid into the bank in August**

| | £ | Orders | What happened |
|---|---:|---:|---|
| **Customer order totals, August** | **113,314.07** | 1,640 | |
| PayPal orders | −7,706.80 | 132 | Paid into your PayPal account, not through Shopify Payments |
| Gift card redemptions | −4,211.20 | 48 full + 36 part | You got this cash when the gift cards were sold, not now |
| Test orders | −912.85 | 8 | 4 tagged `test`, 4 through the test gateway. Not real sales |
| Cancelled before payment was taken | −887.45 | 6 | Never charged |
| **Charged through Shopify Payments** | **99,595.77** | 1,446 | |
| Card processing fees | −2,019.03 | | About 2% (Visa/Mastercard ~1.6% + 20p, Amex ~2.6% + 20p). Steady every month |
| Refunds on August orders | −1,668.90 | 43 | |
| Chargebacks | −212.00 | 2 | £182 disputed plus £30 dispute fees (#32955, #33706), both still open |
| Orders from 30–31 Aug, paid out 1–2 Sept | −6,075.32 | 87 | Normal two-day delay |
| **Paid into the bank in August from August orders** | **89,620.52** | | |

The bank actually received **£94,396.54** in August. The extra £4,776.02 is the same delay from the July side: sales from 30–31 July were paid out in early August, less £1,380.64 of July-order refunds and one chargeback on a July order.

**Things to check**
- **PayPal (£7,706.80)** is the biggest item. Check that your PayPal balance has been moved to the bank; it won't appear in Shopify payouts.
- **The 1–2 Sept payouts (£6,075.32)** still show as "in transit" in this export. It's now [run date], so confirm they arrived.
- **Three open chargebacks:** #32603 (£41.95, a July order), #32955 (£116) and #33706 (£66). You won both chargebacks you contested in June–July and got the £15 fees back, so these are worth answering.
- **Fees and refunds (about £3,700)** are the only real losses. The rest is the payment route, gift cards or timing.

**What "sold" means changes the answer.** By your own sales definitions (shipped orders only, no VAT, no shipping, after refunds, test orders left out), August sales were **£85,086.86**. That's *less* than the £94,396.54 banked. The gap only appears if you compare what customers paid, VAT included, with the bank. Two things make the bank look bigger than it really is:
- About £17,800 of what you received is VAT you owe HMRC.
- £4,778.30 of pre-orders (70 orders, not shipped yet) has been paid into the bank but isn't counted as a sale until it ships.
