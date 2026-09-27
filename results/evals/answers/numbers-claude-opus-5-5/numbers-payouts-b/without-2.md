<!-- numbers-claude-opus-5-5 / numbers-payouts-b / without the plugin / run 2: passed -->

Most of the gap isn't lost money. I matched every August order to the payout file, and the $621.37 difference comes down to timing, a few orders that were never going to pay out, and some real deductions. The numbers tie out to the cent.

**Totals**
- August orders (#2001–#2070), order totals: **$4,335.23**
- Payouts that landed in August (Aug 3 – Aug 31): **$3,713.86**
- Difference: **$621.37**

**Where the $621.37 went**

| | Amount | What it is |
|---|---|---|
| August orders | $4,335.23 | |
| Still in transit | −$280.94 | #2052, #2067 and #2066 were placed Aug 30–31. They pay out Sep 1–2 ($271.90 after fees). |
| July orders in the Aug 3 payout | +$99.57 | #1998–#2000 were placed Jul 31 and paid out in August. |
| **Test-gateway orders** | −$79.25 | #2011 ($20.32) and #2044 ($58.93) were paid with "Bogus Gateway (for testing)". No money was collected for them. |
| Voided order | −$50.35 | #2008 was cancelled the same day. |
| Gift card on #2051 | −$20.00 | Shopify Payments only charged $100.12 of the $120.12 total. The rest was a gift card, which doesn't show up in payouts. |
| Refunds | −$58.06 | #2038 was fully refunded ($46.06). #2049 was partly refunded ($12.00). |
| **Chargeback on #2027** | −$96.51 | $81.51 was taken back plus a $15 dispute fee. There's no resolution in the file. |
| Adjustment on #2033 | +$0.35 | |
| Processing fees | −$136.18 | About 3.4% of charges, which is normal. |
| **August payouts** | **$3,713.86** | |

**Things to look into**
1. **#2011 and #2044 are marked paid and fulfilled, but they went through the test gateway.** If those were real customers, you shipped $79.25 of goods without being paid. This usually means test mode was left on, or a staff member placed the orders with the test gateway. Check your payment settings.
2. **The #2027 chargeback ($96.51) is still open.** You may be able to get it back. Another dispute, on #2015, was won and reversed in full on Aug 26, so it cost you nothing overall. If #2027 is still within the response window, submit evidence the same way.
3. **#2038 was fully refunded after it was fulfilled.** Check whether it was a return or a refund where the item was never sent back.

Only about $311 of the gap is actually gone: fees, refunds, the chargeback and the test-gateway orders. The rest is either still on its way ($271.90 net) or was never Shopify Payments money (the void and the gift card).
