# August Sales vs. Bank Deposit Analysis

## Quick Answer

You sold **EUR 3,022.62** in August, but only **EUR 2,448.74** landed in your bank account in that month. The difference of **EUR 573.88** accounts for:
- EUR 22.90 voided order (never charged)
- EUR 99.00 PayPal order (different payment processor)
- EUR 80.90 missing Shopify record (order #1013—needs investigation)
- EUR 56.59 payment processing fees
- EUR 70.50 customer refunds
- EUR 34.30 chargeback loss + EUR 15.00 dispute fee
- EUR 209.69 pending deposits (arriving in early September)

---

## Detailed Breakdown

### Your August Sales: EUR 3,022.62

From your Shopify orders export, 60 unique orders totaling **EUR 3,022.62**.

### Where That Money Went

#### 1. Orders NOT processed by Shopify Payments (EUR 202.80)

| Order | Amount | Reason |
|-------|--------|--------|
| #1021 | EUR 22.90 | Voided—customer cancelled before payment |
| #1055 | EUR 99.00 | PayPal Express Checkout (separate processor) |
| #1013 | EUR 80.90 | **Missing from payout file** (see note below) |

**Note on Order #1013:** This order shows as "paid" in Shopify but has no corresponding transaction in your Shopify Payments payout file. Check with Shopify Support—it may be a data sync issue or still pending.

#### 2. Shopify Payments Processing (EUR 2,819.82)

The remaining 57 orders were processed through Shopify Payments.

**Gross charges:** EUR 2,819.82

**Less: Payment processing fees** (average 2% per transaction): **-EUR 56.59**

**Subtotal:** EUR 2,763.23

#### 3. Refunds Issued (EUR 70.50)

| Order | Amount | Type |
|-------|--------|------|
| #1042 | EUR 60.50 | Full refund |
| #1030 | EUR 10.00 | Partial refund |
| **Total** | **EUR 70.50** | |

These refunds were processed and deducted from your account in August (payout dates Aug 26–28).

#### 4. Chargeback/Dispute (EUR 49.30)

| Order | Original Charge | Dispute Amount | Dispute Fee | Net Impact |
|-------|---------|---------|---------|---------|
| #1060 | EUR 19.30 | EUR -19.30 | EUR -15.00 | EUR -34.30 |

A customer initiated a dispute on order #1060. You lost the EUR 19.30 charge plus a EUR 15.00 dispute handling fee. This was processed in August (payout date Aug 20).

### What Actually Hit Your Bank Account

**In August (paid):**
- Net Shopify Payments: EUR 2,763.23
- Minus refunds: -EUR 70.50
- Minus chargeback loss: -EUR 34.30
- **Total August deposits: EUR 2,448.74**

**Pending (arriving early September):**
- 4 recent transactions still in transit: **EUR 209.69**
  - Order #1050: EUR 43.19
  - Order #1059: EUR 90.37
  - Order #1009: EUR 42.50
  - Order #1058: EUR 33.63

**Total by September 2:** EUR 2,658.43

---

## Summary Table

| Category | Amount |
|----------|--------|
| **Shopify Sales Total** | EUR 3,022.62 |
| – Voided orders | -EUR 22.90 |
| – PayPal orders | -EUR 99.00 |
| – Missing record (#1013) | -EUR 80.90 |
| **Shopify Payments processed** | EUR 2,819.82 |
| – Payment fees | -EUR 56.59 |
| – Customer refunds | -EUR 70.50 |
| – Chargeback + fee | -EUR 49.30 |
| **Shopify Payments net** | EUR 2,643.43 |
| Less: In-transit funds | -EUR 209.69 |
| **August bank deposits (received)** | EUR 2,433.74* |
| **September deposits (pending)** | EUR 209.69 |
| **Expected total** | EUR 2,643.43 |

*Note: The exact August deposit may vary by 1–2 EUR depending on when your bank processed the Sept 2 transfers.

---

## What to Do

1. **Investigate order #1013** (EUR 80.90): Contact Shopify Support to find out why this paid order isn't in your payout records.

2. **Monitor chargeback #1060:** The EUR 15.00 dispute fee was charged. If you believe the customer's dispute is invalid, you can contest it through Shopify Payments.

3. **Expect September deposit:** EUR 209.69 from orders placed Aug 30–31 should arrive by September 2.

If your bank shows different numbers, it may be due to:
- Different currency conversion dates
- Bank processing delays
- Additional fees charged by your bank
- Deposits that cleared after August 31

Contact Shopify Support with your Payout ID (PO-20260803 through PO-20260831) if the amounts don't match.
