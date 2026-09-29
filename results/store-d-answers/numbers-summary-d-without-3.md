## August 2026 net sales: **$1,248,212.61**

That's product sales on orders placed from Aug 1 to Aug 31 (store time, EDT), after discounts and refunds, with sales tax and VAT removed. It doesn't include shipping, gift cards, or tips.

| | Amount |
|---|---:|
| Gross product sales (list price × quantity) | 1,458,409.97 |
| Less discounts | (104,063.99) |
| Less VAT included in UK/EU prices | (45,918.24) |
| Less refunds, tax removed | (60,215.14) |
| **Net sales** | **1,248,212.61** |

**Included:** 14,881 orders from the web store, the Brooklyn store (POS, about $44k), subscriptions, and 6 wholesale Net-30 invoices (about $13k) that have shipped but aren't paid yet.

**Left out:**
- **Test orders:** 8 orders from qa@harborpine. One of them (#67254) isn't tagged "test", so a filter on the tag alone would miss it.
- **Orders that didn't turn into sales:** 266 cancelled or voided, 7 where the payment authorization expired, and 12 that are unpaid and unshipped. Together these add up to $31,277 in order value.

**Recorded separately (not in net sales):**
- Shipping charged to customers: $95,868.23 after shipping discounts, with VAT removed. If your bookkeeper counts shipping as revenue, the total is $1,344,080.84.
- Gift cards sold: $15,475.00. This is money owed to customers until the cards are used, not a sale. Purchases paid with gift cards are already in net sales.
- Tips: $1,827.67.
- Sales tax and VAT collected: $114,605.34. Import duties: $15,840.41. Both are paid on to the authorities and aren't revenue.

## Things your bookkeeper should know
1. **UK and EU prices include VAT.** On those orders, the export's Total doesn't add the tax on top the way it does for US orders. I took the VAT out of the price. My calculated VAT comes within $23 of what Shopify reports. Adding up all the parts gets within $670 (0.04%) of the order totals in the export.
2. **More refunds will come.** The export was pulled on Sep 5, so August orders had only a few days of September returns counted. Later refunds will lower this number. The tax part of each refund is also an estimate, because the export gives refunds only as one amount including tax.
3. **This won't match Shopify's own Sales report.** I counted refunds against the month the order was placed. Shopify counts them in the month the refund is issued, and a lot of the refunds issued in August were for June and July orders.
4. **The jump from Aug 14 is real.** Order volume roughly doubled when the SUMMER20 sale started, and about a third of orders from then on use the code. It isn't duplicate data.

The calculation script is in my scratchpad as `calc.py` if your bookkeeper wants to check it.
