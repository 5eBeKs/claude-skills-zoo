<!-- numbers-c-claude-opus-5-5 / numbers-summary-c / without the plugin / run 2: failed: revenue-on-the-owners-definitions -->

August was your best month of the summer. **Net revenue was £86,104.92**, excluding VAT and shipping and after refunds. That's up 7.1% on July.

**August 2026 (orders created 1–31 Aug)**

| | Amount |
|---|---|
| Product sales, after discounts, incl. VAT | £105,004.50 |
| Less refunds (product part) | −£1,678.59 |
| Net sales incl. VAT | £103,325.91 |
| VAT at 20% | £17,220.98 |
| **Net revenue excl. VAT** | **£86,104.92** |
| Shipping charged to customers, incl. VAT (not in revenue) | £2,915.10 |
| Discounts given (already taken off sales) | £1,197.08 |
| Orders counted | 1,555 |
| Average order value excl. VAT | £55.37 |

**All three months, for comparison:**

| Month | Orders | Net revenue excl. VAT | Change |
|---|---|---|---|
| June | 1,339 | £77,481.07 | |
| July | 1,468 | £80,427.20 | +3.8% |
| August | 1,555 | £86,104.92 | +7.1% |

August refunds were also lower: £1.7k, against £3.6k in July.

**How I counted these**, following the rules in `store_definitions.json`:
- **Shipped orders only.** 70 August pre-orders were paid but not yet shipped, so they're left out. They'll add a noticeable amount once they ship.
- **Also left out in August:** 8 test orders (tagged "test" or paid through the test gateway) and 6 voided orders. One other order hadn't shipped yet, so it's out too.
- **Refunds:** partial refunds take off only the amount refunded, and each refund counts in the month of its order. Refunds made later on August orders will lower August's figure, so it may still drop slightly.
- **Shipping on refunds:** for full refunds I took off only the product part, because shipping isn't in revenue. The export doesn't split partial refunds between products and shipping, so I treated them as all product. That may make the refund figure slightly too high.
- **VAT:** the £17,220.98 is the VAT on product sales only. The export charges VAT on shipping as well, which adds about £486 for August. Your accountant may want the two combined for the VAT return.

The data itself looked clean: all orders are in GBP, there are no duplicates, and order totals and tax add up.
