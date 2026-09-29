**August 2026 net sales: $1,248,661.11**

This is product sales from orders placed August 1–31 (store time, UTC−4), after discounts and returns. It leaves out sales tax/VAT, shipping, gift card sales, tips and duties, and it doesn't count test orders or cancelled orders.

**What's in it**

| | Amount |
|---|---|
| Gross product sales (14,893 orders) | $1,409,625.10 |
| Less discounts | −$100,462.46 |
| Less returns (refunds on August orders, before tax) | −$60,501.53 |
| **Net sales** | **$1,248,661.11** |

- It covers the online store, the Brooklyn shop (POS, $42.6k), subscription renewals ($9.1k) and 7 wholesale draft orders ($13.3k).
- UK and EU prices include VAT, so I took the VAT out: $49.6k from gross sales and $3.7k from discounts. Otherwise sales would be overstated.
- $11.1k of it comes from 27 orders that aren't fully paid yet (bank transfer, Net 30 wholesale, card authorised but not captured). $10.2k is still outstanding. If the bookkeeper records sales only when cash comes in, these should move out.

**Left out, reported separately**

| Item | Amount | Why |
|---|---|---|
| Shipping charged, before tax | $95,650.57 | Shipping income, not product sales |
| Tax collected | $114,641.07 | Owed to tax authorities |
| Duties | $15,840.41 | Passed through to customs |
| Gift card sales | $15,475.00 | A liability until redeemed. Purchases paid with gift cards *are* in sales |
| Tips | $1,827.67 | Not sales |
| Test orders (8) | $1,090.56 | 5 were tagged "test"; 3 weren't tagged but paid via the test gateway or had a "TEST, do not ship" note |
| Cancelled or voided orders (264) | $28,694.21 | Never became sales |
| Expired card authorisations (7) | $592.55 | Never paid |

**Caveats for the bookkeeper**

1. **Returns will grow.** The refund data ends September 5. Refunds for past months kept coming well into the next month: $45.7k of July's orders were refunded in August. Expect roughly $25–30k more refunds against August orders, which would reduce net sales. If the books record returns in the month the refund is issued instead, the returns line will be different.
2. **The export's own Subtotal and Total columns are inconsistent.** For partially refunded orders they already subtract some returned items; for fully refunded orders they don't. I built the figure from the individual line items and the refunded amounts instead. 24 small refunds that exactly matched the shipping charge are treated as shipping refunds, not product returns.
3. **Order volume roughly tripled from August 14**, when the SUMMER20 code started. I checked for duplicate orders and found none in August.

My scripts are in the session scratchpad folder if anyone wants to check the working.
