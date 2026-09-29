**Short answer: on the data you have, no product lost money in July.** Every product with a known cost made money, and the lowest margin was about 51%. Five items can't be judged because they have no cost recorded.

"Made money" here means what a product earned after refunds, its unit cost, card fees and chargebacks. Shipping labels, ads, packaging and overhead aren't in these files, so they aren't included. A product could still lose money once those are counted, and I can't check that.

### Made money (31 products)
| Product | Units | Profit | Margin |
|---|---|---|---|
| Heavyweight Hoodie* | 848 | ~$40.2k | 60% |
| Classic Crew Tee | 2,036 | $30.7k | 58% |
| Summer Wrap Dress | 589 | $29.0k | 57% |
| Relaxed Jeans | 463 | $22.6k | 53% |
| Merino Crew Socks 3-Pack | 1,024 | $19.9k | 58% |
| Linen Shorts | 688 | $19.7k | 58% |
| Slim Chino | 544 | $19.1k | 54% |
| Denim Jacket | 277 | $17.8k | 53% |
| Linen Button-Up, Zip Hoodie, Polarized Sunglasses, Pocket Tee, Swim Trunks, Oxford Shirt, Boxer Briefs | — | $13.5–14.3k each | 54–63% |
| Crewneck Sweatshirt, Rolltop Backpack, Packable Rain Jacket, Midi Slip Skirt, Everyday Ankle Socks, Organic Longsleeve, Ribbed Tank, Canvas Weekender, Canvas Cap, Leather Card Wallet, Leather Belt | — | $7.2–10.7k each | 51–63% |
| Canvas Tote Bag, Sock Club Subscription, Sun Hat, Wool Beanie, Kids Tee | — | $2.5–6.5k each | 54–68% |

Margin is profit as a share of revenue before refunds. The weakest are Rolltop Backpack and Packable Rain Jacket at 51%.

\*The Forest colour of the Heavyweight Hoodie (128 units) has no cost in the catalog. Even if each one cost the full $84 price, the hoodie still clears about $29k.

### Lost money
None.

### Can't tell (no cost recorded)
To lose money, each unit would have had to cost more than the "break-even" figure below:

| Item | July units | Break-even unit cost | Why |
|---|---|---|---|
| Linen Bucket Hat | 148 | $28.25 | Not in the products export at all (probably deleted) |
| Silk Bandana | 228 | $26.19 | No SKU and no cost |
| Enamel Pin Set | 234 | $10.34 | No SKU and no cost |
| Gift Wrap | 133 | $5.31 | No cost |
| Custom embroidery (initials) | 6 | $12.15 | Not a catalog product; a custom line item |

If you tell me what these cost you, I can finish the picture. The Silk Bandana and the Bucket Hat matter most. The Recycled Water Bottle and the Sherpa Fleece Vest (still a draft) also have no cost, but neither sold in July.

### How I counted
- **July** means orders placed July 1–31, store time. Refunds, including ones issued in August, are counted against the July order they belong to.
- **Left out:** cancelled or voided orders (278 lines, restocked and never shipped), 7 test orders, tips, and gift card sales (money you owe customers, not a product sale).
- **Revenue** is the price actually paid after discounts. VAT is taken out of UK and EU orders, where prices include tax.
- **Refunds** were matched to the refunded item where the amount made it clear, and otherwise spread across the order. I assumed refunded items that weren't restocked did not come back into stock, so their cost still counts.
- **Kept in, with their cost:** replacement orders and SEED100 influencer freebies (sold at $0), staff discounts, and wholesale orders.
- **Old SKUs:** about 930 Classic Crew Tee units were sold under old `CT-*` SKUs. I matched them to the tee by name ($7.40 cost).
- **Fees:** card fees and chargeback losses come from the payment transactions export. PayPal fees aren't in any file. On about $48k of PayPal sales they'd be roughly $1.7k spread across products, which doesn't change any answer.

The analysis script is at `scratchpad/july.py` if you want to rerun it with the missing costs.
