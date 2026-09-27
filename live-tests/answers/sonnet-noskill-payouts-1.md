# Where the August money went

I matched every order in `orders_export.csv` against every transaction in `payout_transactions.csv`. The gap is fully explained — it's not one mystery, it's six separate, smaller things stacking up. Here's the exact waterfall from your order totals down to what actually landed in the bank by August 31:

| Step | Amount (EUR) | Running total |
|---|---:|---:|
| Sum of "Total" on all August orders, excluding the cancelled one (#1021, see below) | 2,999.72 | 2,999.72 |
| minus Order #1013 — tagged "test", never actually charged (see below) | −80.90 | 2,918.82 |
| minus Order #1055 — paid by **PayPal**, not Shopify Payments (see below) | −99.00 | 2,819.82 |
| minus normal Shopify Payments processing fees on all charges | −56.59 | 2,763.23 |
| minus refunds paid back to customers | −70.50 | 2,692.73 |
| minus a chargeback/dispute on order #1060 (principal + dispute fee) | −34.30 | 2,658.43 |
| minus 4 orders whose payout hadn't landed yet as of Aug 31 (in transit) | −209.69 | **2,448.74** |

**2,448.74 EUR is what had actually reached your bank account by August 31.** Another **209.69 EUR** is real money that is simply still on its way (see "in transit" below) — that's not lost, just delayed into September.

So of the ~2,999.72 EUR you'd naturally add up from order totals, about **550.98 EUR** doesn't show up in your August bank balance: 209.69 of it is just late (arrives Sept 1–2), and the rest (341.29 EUR) is real fees, a real refund, a real chargeback, and two orders that were never actually paid through this channel at all. Details below.

---

## 1. Order #1021 — cancelled, never charged (22.90 EUR)
This order is marked `voided`, cancelled the same day it was placed. It was never charged, so correctly there's no matching entry in the payout file. If you were adding up "Total" across the whole export without checking status, this is 22.90 EUR that was never real sales in the first place.

## 2. Order #1013 — looks paid, but no money ever moved (80.90 EUR)
This order shows `Financial Status = paid`, `Payment Method = Shopify Payments`, total 80.90 EUR — but it is **tagged "test"**, and there is no matching charge for it anywhere in the payout export. Every other Shopify Payments order has a corresponding charge line; this is the only one that doesn't. That strongly suggests it was placed with a test/bogus payment gateway (common when testing checkout) rather than a real card, so no real money was ever collected.
**Action:** open order #1013 in Shopify admin and confirm whether it was a real payment. If it's a test order, it should be excluded from your sales figures.

## 3. Order #1055 — paid by PayPal, not Shopify Payments (99.00 EUR)
This order's `Payment Method` is "PayPal Express Checkout," not "Shopify Payments." Your `payout_transactions.csv` is the **Shopify Payments** payout report only — PayPal has its own separate payout schedule and its own report/bank deposit. This 99.00 EUR isn't missing; it simply won't ever appear in this particular file. Check your PayPal account (or PayPal's own transaction report) to see when/if it was deposited.

## 4. Processing fees (56.59 EUR)
Every real Shopify Payments charge has a card-processing fee deducted before payout (roughly 2% + a small fixed amount, and Amex tends to run a bit higher than Visa/Mastercard). Across all of August's real charges (gross 2,819.82 EUR), fees totaled 56.59 EUR. This is normal and expected — it's the fee Shopify Payments charges to process cards, not an error.

## 5. Refunds given to customers (70.50 EUR)
- **Order #1042** — refunded in full: 60.50 EUR. Note the original processing fee (1.16 EUR) on this charge was **not** returned to you when you refunded the customer, so this order cost you 1.16 EUR net even beyond the refund itself.
- **Order #1030** — partially refunded: 10.00 EUR back to the customer, out of a 49.00 EUR order.

## 6. A dispute/chargeback on order #1060 (34.30 EUR)
This is the one worth looking at closest. Order #1060 was charged 19.30 EUR on Aug 6 and paid out normally on Aug 10 (net 18.76 EUR after fee). Then on Aug 18, the customer's bank filed a **dispute (chargeback)**: Shopify pulled the 19.30 EUR back out of your balance *and* charged a 15.00 EUR dispute fee on top, for a net hit of −34.30 EUR in the Aug 20 payout.
Net result for this one order: you received 18.76 EUR, then lost 34.30 EUR — a net loss of **15.54 EUR** on a 19.30 EUR sale.
Note: your Shopify orders export still shows #1060 as "paid" with "Refunded Amount = 0.00" — chargebacks don't show up as refunds in that export, so this kind of loss is easy to miss unless you check the payments/payout side. If you haven't already, you may want to respond to this dispute in Shopify admin (there's often a deadline to submit evidence).

## 7. Money still in transit, not yet in the bank (209.69 EUR)
Four orders placed at the very end of August were charged but their payouts hadn't landed yet as of Aug 31 (Shopify Payments typically pays out a few days after the charge):

| Order | Charged | Net payout | Payout date |
|---|---:|---:|---|
| #1050 | 44.10 | 43.19 | Sept 1 |
| #1059 | 92.00 | 90.37 | Sept 1 |
| #1009 | 43.40 | 42.50 | Sept 2 |
| #1058 | 34.40 | 33.63 | Sept 2 |

This is completely normal timing lag, not lost money — it should show up in your September bank statement.

---

### Bottom line
- **Real, permanent gap** (fees + refund + chargeback, plus the test order and the PayPal order that were never going to appear here): about **341.29 EUR**.
- **Timing gap** (will still arrive in September): **209.69 EUR**.
- The single item most worth your attention is the **34.30 EUR chargeback on order #1060** — it's the only one that wasn't a normal, expected part of running the shop, and it may need a response before its dispute deadline.
