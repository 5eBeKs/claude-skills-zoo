I found no product that lost money in July. Most made money, and five can't be judged because the products export has no cost for them.

"Made money" here means what's left from a product's July sales after discounts, refunds, product cost, and card-processing fees and chargebacks. Shipping labels, ad spend and overheads aren't in these files, so this isn't full profit.

**Made money (31 products).** Every product with a known cost kept 58–72% of its sales after the costs above. So discounts and refunds would have to be much larger for any of them to go negative.

| Largest profit in July | Profit | Smallest profit | Profit |
|---|---|---|---|
| Heavyweight Hoodie | $41.5k | Kids Tee | $2.7k |
| Classic Crew Tee | $32.4k | Wool Beanie | $5.5k |
| Summer Wrap Dress | $30.1k | Sun Hat | $5.7k |
| Relaxed Jeans | $23.2k | Sock Club Subscription | $6.5k |
| Merino Crew Socks 3-Pack | $20.9k | Canvas Tote Bag | $7.0k |

- **Heavyweight Hoodie:** the Forest colour has no cost in the export (128 units in July). The other colours alone made about $32k, so the product was profitable whatever Forest costs.
- **Classic Crew Tee:** until mid-July, orders used older product codes (`CT-…` instead of `HP-TEE-CLS-…`). I matched them to the current tee so those sales are counted.

**Lost money: none.**

**Can't tell (no cost recorded):**

| Product | July sales after refunds | Loses money only if each unit cost more than | List price |
|---|---|---|---|
| Linen Bucket Hat (missing from the products export entirely) | $4.5k | ~$28 | $36 |
| Silk Bandana | $6.5k | ~$27 | $34 |
| Enamel Pin Set | $2.7k | ~$10.50 | $14 |
| Gift Wrap | $0.7k | ~$5 | $6 |
| Custom embroidery (initials) | $76 | ~$12 | $15 |

To lose money, each of these would have to cost about 75–80% of its price. Your other products cost 20–35% of price, so they probably made money, but I can't confirm it from the files. Adding their costs to Shopify would settle it.

How I counted:
- **July** means orders placed in July in the store's own time zone: 7,981 orders and about $693k in product sales after discounts and refunds.
- **Left out:** 4 test orders, 14 voided or expired orders, tips and gift-card sales.
- **Refunds:** all refunds on July orders are counted, including ones issued in August or September. I took off the tax and shipping part of each refund and assigned the rest to the items returned. Returned items that went back into stock carry no product cost.
- **Processing fees:** these come only from Shopify Payments. PayPal fees aren't in the files; PayPal orders were about 6.5% of sales, so this understates fees slightly.

The script is `scratchpad/july.py` if you want to re-run it or change any of these choices.
