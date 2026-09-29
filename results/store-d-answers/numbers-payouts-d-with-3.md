**$572,456.23 reached the bank from Shopify in June.** June's card orders came to $691,562.27, so the gap is **$119,106.04**. The breakdown accounts for the whole gap, leaving $0.00 unexplained. The bank figure matches your payouts export: 20 payouts paid in June.

Your June sales are higher again than the card orders figure. $82,635.67 of June orders (610 orders) were paid outside Shopify Payments: PayPal, bank deposit, manual, cash, cash on delivery and gift cards. That money never goes through Shopify payouts, so look for it in PayPal or directly in the bank.

## From June's card orders to the bank

| | USD |
|---|---:|
| Card orders placed in June (Shopify Payments, shipped yet or not) | 691,562.27 |
| − Refunds processed in June | −82,726.47 |
| &nbsp;&nbsp;of which on orders from earlier months | 45,616.95 |
| − Card fees | −25,967.07 |
| − Disputes: amount and fees | −1,212.93 / −240.00 |
| − Still in transit at month end | −117,366.90 |
| **= Paid out for June's card transactions** | **467,444.55** |
| + Paid out in June for transactions before the transactions export starts | +105,011.68 |
| **= Paid out to the bank in June** | **572,456.23** |

**Where the rest went:**
- **Refunds: $82,726.47.** $37,109.52 was on June orders and $45,616.95 on orders from earlier months.
- **Card fees: $25,967.07.**
- **Disputes: $1,452.93 in total.** There were 16 disputes at $15.00 each in fees, and none has been won back yet: #45476, #43139, #42339, #46132, #48748, #50960, #46564, #46016, #47881, #48462, #43365, #47863, #42377, #46314, #43148, #43258.
- **Not in the bank by 30 June: $117,366.90** (1,512 orders).
  - $18,132.40 of this is the **payout of 2026-06-30, which failed** and wasn't paid again in June. Check that Shopify re-sent it in July, and check the bank account details it failed on.
  - The rest was in the payout scheduled for 2026-07-07.
- **Partly offset by $105,011.68 that reached the bank in June but belonged to May:**
  - 2026-06-01: $17,678.53, all May money
  - 2026-06-02: $21,209.54, all May money
  - 2026-06-03: $60,256.61, all May money
  - 2026-06-04: $18,603.09, of which $5,867.00 was May money

No reserves, Shopify adjustments or other transaction types affected June.

## Worth a look
These don't change the totals, but they didn't match up one-to-one:
- **135 charges** whose order isn't among the counted June card orders.
- **179 orders** where the amount charged differs from the order total.
- **87 split payments** (gift card plus card), where only the card part is counted.
- **5 orders** placed in June but charged in early July: #55864, #55838, #55835, #55667, #55378.
- There are no June card orders without a charge.

## How this was counted
- Test orders (tagged "test" or paid through the test gateway) are left out of sales. That's the usual choice, but you haven't confirmed it yet.
- Both exports have records on all 30 days of June, all in USD.
- The June payout total was checked against the payouts export payout by payout, and it matches.
- The payment transactions export starts on 1 June. That's why the May money in the early June payouts appears as its own line.

## Two questions for you
The figures above use the usual answer to each question until you confirm it. A different answer would change them.
1. **Test orders:** should they stay out of sales (usual), or be counted?
2. **Export contents:** are these values in your exports all expected? If you confirm, they're saved so a new value is flagged next month.
   - Payment methods: Shopify Payments, PayPal Express Checkout, Bank Deposit, Cash, Cash on Delivery (COD), Gift Card, manual, and "(for testing) Bogus Gateway"
   - Order tags: Net 15, Net 30, Subscription, replacement, test, wholesale, and similar
   - Payout transaction types, including reserve and dispute reversal

The full report is saved as `files/reconciliation_2026-06.md`. It lists every in-transit order and every unmatched order, charge and payment, and it passes the skill's number check. This chat version gives counts for the long lists, which is why only the saved file passes that check.
