<!-- numbers-c-claude-opus-5-5 / numbers-summary-c / without the plugin / run 1: passed -->

August was the best month of the summer. **Net sales were £85,116.48 excluding VAT.** That's up about 7% on July (£79,434) and about 11% on June (£76,555).

**August 2026: the numbers for your accountant**

| | Amount |
|---|---|
| Orders counted | 1,555 |
| Gross product sales, ex VAT (after discount codes) | £86,506.18 |
| Less refunds, ex VAT | −£1,389.70 |
| **Net sales, ex VAT** | **£85,116.48** |
| Output VAT on those net sales (20%) | £17,023.30 |
| Shipping charged to customers, incl. VAT (not in revenue) | £2,915.10 |
| Average order value, net ex VAT | £54.74 |

Refunds came from 17 fully refunded orders and 28 partly refunded ones. This was August's lowest refund total of the three months; July's was £2,952.

**What's left out of the August figure**, following the rules in `store_definitions.json`:
- **8 test orders** worth £912.85. These were tagged "test" or paid through Shopify's test gateway.
- **70 unshipped pre-orders** worth £3,863.42 ex VAT. A sale only counts once it has shipped, so these will appear once they go out.
- **7 cancelled orders** (6 voided and 1 refunded before it shipped).

**Things your accountant should know:**
1. **VAT on shipping:** The shipping figure includes VAT, so shipping carries about £485.85 of output VAT on top of the £17,023.30. If shipping needs to go on the VAT return, that VAT has to be added.
2. **Dates:** Each order is placed in the month it was created. The export doesn't show when an order shipped or when a refund was made, so any August refunds of July orders are counted in July.
3. **Refunds:** I treated all refunds as refunds of products, including VAT. The export doesn't say whether any of them covered shipping.
4. **One June order (#30677)** is marked "refunded" but only £30 of its £55 was actually refunded. I counted just the £30, which is why June shows £76,555.00. August isn't affected.
