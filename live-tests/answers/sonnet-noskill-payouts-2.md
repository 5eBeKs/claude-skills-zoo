# Where your August money went

**Shopify order total for August: €2,999.72**
**Actually deposited to your bank in August (Shopify Payments payouts): €2,448.74**

**Gap: €550.98**

Here is the exact breakdown of that gap — nothing is actually "lost," but it is split across five different reasons:

| # | Reason | Amount | Real money issue? |
|---|--------|-------:|---|
| 1 | Paid via PayPal, not Shopify Payments (order #1055) | €99.00 | No — check your PayPal balance separately, it never goes through Shopify Payments payouts |
| 2 | Test order counted as a real sale (order #1013, tagged "test") | €80.90 | No — no card was ever charged, exclude it from your revenue |
| 3 | Shopify Payments processing fees on August charges | €56.59 | Yes — normal cost of accepting cards |
| 4 | Refunds issued to customers | €70.50 | Yes — money you gave back, plus you don't get the original fee back either |
| 5 | Still "in transit," not yet deposited by month end | €209.69 | No — it lands in September, just a timing lag |
| 6 | Chargeback (dispute) penalty on order #1060 | included below | Yes — extra cost beyond the refund |

Adding it up: €99.00 + €80.90 + €56.59 + €70.50 + €209.69 = **€516.68**. The remaining **€34.30** is the chargeback on order #1060, explained below — it nets out against amounts already counted above, so the categories aren't perfectly additive, but every euro is accounted for in the detail below.

## 1. PayPal order — €99.00 (order #1055)
This order was paid through "PayPal Express Checkout," not Shopify Payments. It never appears in your Shopify Payments payout file at all — it settles into a separate PayPal account on PayPal's own schedule. Nothing is wrong here; just don't expect it in the Shopify Payments deposits, and check your PayPal balance for it.

## 2. Test order counted as a sale — €80.90 (order #1013)
Order #1013 is tagged "test" in your export and shows as "paid" for €80.90, but there is **no matching transaction anywhere in your Shopify Payments payout file** — no charge, no fee, nothing. No customer card was actually charged. This inflates your "sold" total in Shopify by €80.90 that was never real money. Recommend deleting or excluding this order from your sales reports.

## 3. Processing fees — €56.59
Shopify Payments deducts its card-processing fee from every charge before paying you out. Across your 54 real Shopify Payments charges in August, fees totaled €56.59. This is a normal cost of doing business, not a problem — but it's part of why "Total" on the order never equals what lands in the bank.

## 4. Refunds — €70.50
Two refunds went out in August:
- Order **#1042**: fully refunded, €60.50. You'd already been paid out €59.34 net (after a €1.16 fee) on this order; the refund pulled the full €60.50 back out, so you also permanently lose the €1.16 fee you already paid — Shopify does not return processing fees on refunds.
- Order **#1030**: partially refunded €10.00 (out of a €49.00 order). You keep €38.01 net on this order (49.00 − 0.99 fee − 10.00 refund).

Total refunded to customers: €70.50. Total fees lost forever because of these refunds: €2.15 (€1.16 + €0.99).

## 5. Chargeback on order #1060 — net €15.54 loss
This is the one that actually costs you real money beyond a normal refund:
- Aug 6: charge of €19.30, fee €0.54, you were paid out €18.76 net on Aug 10.
- Aug 18: the customer's bank filed a **dispute/chargeback**. Shopify reversed the €19.30 **and** charged you a €15.00 dispute fee, a net **−€34.30** deducted from your Aug 20 payout.
- Net result for this one order: €18.76 − €34.30 = **−€15.54**. You not only lost the sale, you paid an extra €15 penalty on top of it.

## 6. Money still in transit — €209.69
Shopify Payments holds a short delay (about 2 business days) before depositing funds. Four orders charged on Aug 30–31 (**#1050** €44.10, **#1059** €92.00, **#1009** €43.40, **#1058** €34.40, net €209.69 after fees) are scheduled to pay out on **Sep 1–2**, so they simply hadn't reached your bank account yet when August closed. This money is not lost — it will appear in your September bank statement.

## Reconciliation, step by step

| Step | Amount |
|---|-------:|
| Shopify order total, August (excl. voided order #1021) | €2,999.72 |
| minus PayPal order (different account) | −€99.00 |
| minus test order (no real charge) | −€80.90 |
| = Real Shopify Payments gross charges | **€2,819.82** ✅ matches payout file exactly |
| minus processing fees | −€56.59 |
| minus refunds | −€70.50 |
| minus chargeback (dispute) | −€34.30 |
| = Total net processed by Shopify Payments in August | **€2,658.43** |
| minus still in transit (pays out in September) | −€209.69 |
| = **Actually deposited to your bank by Aug 31** | **€2,448.74** |

## Bottom line
- €2,448.74 landed in your bank in August.
- €209.69 is on its way and will land in early September — not lost.
- €99.00 went to PayPal instead of Shopify Payments — check that account.
- €80.90 was never a real sale (test order) — remove it from your books.
- €56.59 went to normal card-processing fees.
- €70.50 was refunded to customers, and €2.15 of the fees on those refunded orders is gone for good.
- €15.54 net was lost on a single chargeback (order #1060), which includes a €15 dispute penalty fee.

Practical fixes: delete/exclude test order #1013 from your reporting so "sales" reflects real revenue, and if chargebacks become frequent, it may be worth tightening fraud/verification settings, since each one costs a flat €15 on top of losing the sale.
