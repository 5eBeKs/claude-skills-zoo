August net sales were **$1,252,676**. That's product sales from orders placed in August (store time, UTC−4), after discounts and returns, and excluding sales tax/VAT and shipping.

**How the figure is built (orders placed Aug 1–31)**

| | Amount |
|---|---|
| Gross product sales, excluding tax (15,127 orders) | $1,433,669 |
| Less discounts | −$102,196 |
| Less returns and cancellations on those orders (tax removed) | −$78,796 |
| **Net sales** | **$1,252,676** |

**What's in it**
- Online store sales ($1.26M), the Brooklyn store's in-person sales ($44k), subscription orders ($9k) and manually created orders ($16k).
- Seven wholesale orders ($13,332). Five of them ($8,949) are unpaid Net 30 invoices, so this is money owed to you, not cash received yet.
- About $10k of other orders that aren't fully paid yet: pending bank transfers, card payments approved but not yet collected, and part-paid orders.
- $1,634 of gift wrap.
- UK/EU prices include VAT, so I took the VAT out of them ($234k of the net sales). Without this step the figure would be overstated.

**What's left out**
- Sales tax and VAT: about $117k.
- Shipping charged, after shipping discounts: $97k.
- Gift cards sold: $15,475. That money is owed to customers until the cards are used. Purchases paid with gift cards are counted as normal sales.
- Tips ($1,853) and import duties ($16,125).
- 8 internal test orders: checkout tests by the QA account. None of them charged real money.
- 37 orders that were never paid: 30 voided and 7 expired, $3,148.
- 11 free replacement orders, which have no value.

**For the bookkeeper**
1. **When returns are counted.** I subtracted returns on August orders, including $19k refunded in early September. The other common convention subtracts refunds in the month they're issued. Card refunds issued in August were $110.5k including tax, across all order months. The export doesn't date PayPal or cash refunds, so the second convention can't be calculated exactly from these files.
2. **The returns figure is estimated.** The export gives each refund only as one total including tax and shipping, so I split out the product portion in proportion to each order. The estimate should be within a few hundred dollars.
3. **A quirk in the export.** On 27 partly refunded orders, the export already shows the reduced total. I rebuilt those from their individual items so the refund isn't subtracted twice.

As a cross-check, every order's total matches its parts (products, shipping, tax, tips, duties, gift cards) to within a cent or two. Across all August orders, the rebuilt totals differ from the export by $33, from those same refund-quirk orders.
