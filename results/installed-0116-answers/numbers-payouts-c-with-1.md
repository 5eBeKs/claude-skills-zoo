Card orders in August came to £99,582.82, and £94,396.54 was paid out to the bank in August. The gap is **£5,186.28**. The reconciliation between the two comes to exactly zero, so none of the gap is unexplained.

I couldn't check the bank figure itself. I didn't have the payouts export, so the £94,396.54 comes from the transactions export alone. Compare it with your bank statement.

## Where the money went

| | GBP |
|---|---:|
| Card orders placed in August (Shopify Payments, shipped yet or not) | 99,582.82 |
| − Refunds processed in August | 2,762.41 |
| &nbsp;&nbsp;of which on orders from earlier months | 1,093.51 |
| − Card fees | 2,019.03 |
| − Disputes: amount and fees | 223.95 + 45.00 |
| Shopify adjustments | 2.35 |
| − Still in transit at month end | 6,075.32 |
| **= Paid out for August's card transactions** | **88,472.41** |
| + Paid out in August for earlier months' transactions | 5,924.13 |
| **= Paid out to the bank in August** | **94,396.54** |

- **The biggest item is timing:** £6,075.32 from August sales (87 orders) was still on its way at month end and was paid out on 1–2 September. In the other direction, £5,924.13 for 93 July transactions was paid out on 3 August. These two roughly cancel, so almost all of the gap is money you actually lost.
- **What you actually lost:**
  - Refunds were £2,762.41, and £1,093.51 of that was on orders from earlier months.
  - Card fees were £2,019.03.
  - Three disputes cost £268.95 in total, none won back yet:
    - #32603: £41.95 plus a £15 fee
    - #32955: £116.00 plus a £15 fee
    - #33706: £66.00 plus a £15 fee
- **One charge that isn't in the order total:** order #33431 (£12.95) was charged, then cancelled and refunded the next day. It's left out of card orders because it was cancelled, and its refund is in the refunds line.

## Not part of this gap

- **Paid outside Shopify Payments:** 180 orders worth £11,918.00 were paid by PayPal or gift card. They never go through Shopify payouts. The PayPal money is in your PayPal account, and gift cards were paid for when they were sold.
- **Paid partly by gift card:** 36 orders were paid partly with a gift card and partly by card. Only the card part is in the payouts.

## Question for you

The export's shape isn't recorded yet, and the figures above assume these values are what you expect. Please confirm:
- **Payment methods:** Shopify Payments, PayPal Express Checkout, Gift card, Bogus Gateway (test)
- **Order statuses:** paid, partially refunded, refunded, voided
- **Tags:** pre-order, test

If you confirm, I'll save them so a new value is flagged next month. Test orders (tagged "test" or paid through the test gateway) are excluded, as your definitions file says.

The full report is saved as `files/reconciliation_2026-08.md`. It lists every in-transit, July, PayPal/gift-card and split-payment order and ends with a check line. Next month, also export **Finances > Payouts > Export**, so each payout can be checked against what reached the bank.
