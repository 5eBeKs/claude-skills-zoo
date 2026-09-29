**No product lost money in July.** 28 products made money after their cost and payment fees. I can't tell for 3 products because we have no cost for them.

"Made money" here means July revenue without VAT, after discounts and refunds, minus product cost and payment fees. Shipping, packaging and ad costs aren't in the exports, so they aren't counted.

**Can't tell (no cost on file)**

| Product | Units | Revenue (no VAT) | Makes money only if it costs us under |
|---|---|---|---|
| Striped Picnic Blanket | 405 | €18,568 | €45.07/unit |
| Oak Serving Board | 443 | €15,391 | €34.12/unit |
| Gift Wrapping | 158 | €490 | €3.04/unit |

- **Picnic blanket:** it's not in the products export at all, so it was probably deleted.
- **Oak serving board:** it's in the export, but its "Cost per item" is blank.
- **Gift wrapping:** also has no cost entered.

If the board costs anything like our other wooden products (about 35% of price), it made money. For the other two I'd only be guessing.

**Made money (smallest profit first)**

| Product | Profit | Margin |
|---|---|---|
| **Stoneware Mug – Second Choice** | **€908** | **31%** |
| Unique Handthrown Bowl | €2,363 | 65% |
| Olive Wood Spoon Set | €3,236 | 54% |
| Coir Doormat | €3,384 | 56% |
| Brass Candle Holder | €4,521 | 56% |
| Espresso Cup Set of 2 | €4,561 | 58% |
| Terracotta Planter | €4,712 | 56% |
| Linen Apron | €4,770 | 55% |
| Glass Carafe | €4,995 | 55% |
| Reed Diffuser | €5,732 | 59% |
| Round Wall Mirror | €6,719 | 54% |
| Rattan Basket | €6,845 | 58% |
| Linen Pillowcase Set | €7,554 | 54% |
| Linen Tea Towel Set | €7,601 | 55% |
| Walnut Cutting Board | €7,586 | 52% |
| Stoneware Bowl | €8,320 | 59% |
| Stoneware Dinner Plate | €8,610 | 59% |
| Tumbler Set of 4 | €9,208 | 57% |
| Bouclé Cushion Cover | €9,427 | 57% |
| Stoneware Mug | €9,550 | 55% |
| Linen Napkins Set of 4 | €13,803 | 53% |
| Ceramic Table Lamp | €13,898 | 56% |
| Ceramic Vase | €14,278 | 60% |
| Jute Rug | €16,581 | 53% |
| Wool Throw | €17,563 | 54% |
| Linen Tablecloth | €18,602 | 52% |
| Soy Candle | €22,732 | 59% |
| Linen Duvet Cover | €27,484 | 52% |

Every other product has a margin above 50%. The only one close to losing money is the **Second Choice mug**. It makes about €2.45 per unit, and 92 of its July orders contained nothing else. Our own shipping cost for those orders isn't in the data, but even a small shipping subsidy could turn that product into a loss.

**How I handled the data**
- **VAT:** order prices include VAT, so I removed it using each order's tax rate.
- **Discounts:** many discounts were recorded only on the whole order, so I spread each order's discount across its lines.
- **Refunds:** I took each refund off in proportion to the order's lines. I kept the product cost on refunded orders, since the export doesn't say whether goods came back. Counting that cost as recovered would add up to about €750 per product and changes no result.
- **Left out:** test orders (including the two paid with Shopify's test gateway), duplicate orders, cancelled orders, and gift-card sales (these aren't revenue until they're spent).
- **Replacements:** free replacement orders count as a cost against the product.
- **SKU mismatches:** the Oat and Sage linen napkins have different SKUs in the two files, so I matched them by name. I matched the handthrown bowl by size.
- **Payment fees:** the fees come from `payment_transactions_export.csv` in the same folder, which covers Shopify Payments only. PayPal and Klarna fees aren't in any export. I tested them at an estimated 3.4% and no product changed column.
- **Costs are today's:** the products export only has current costs, so if a cost changed since July, that product's figure will be off.
