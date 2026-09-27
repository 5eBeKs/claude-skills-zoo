<!-- numbers-claude-opus-5-5 / numbers-margins / with the plugin / run 1: passed -->

The Steel Strainer is the one product I can confirm lost money in August. The Gift Set has no cost in `cogs.csv`, so I can't tell yet whether it made or lost money. Every amount below is in EUR. All 49 figures in the report were checked against the calculation, and the check passed.

## August 2026: which products lose money

**Sold below cost: Steel Strainer (STR-STL-001).** It's the only product with a negative margin. 20 units brought in 109.24 without VAT but cost 142.00, a margin of -32.76 (-30.0%). Its unit cost is 7.10.

**Margin unknown: SET-GFT-001 (Gift Set).** It has no cost in `cogs.csv`. Its 17 units brought in 700.00 without VAT, but I can't tell whether it makes or loses money. Its margin is unknown, not zero. Please send its unit cost.

All other products made money.

| SKU | Product | Units | Revenue ex VAT | Cost | Margin | Margin % |
|---|---|---|---|---|---|---|
| STR-STL-001 | Steel Strainer | 20 | 109.24 | 142.00 | -32.76 | -30.0% |
| SET-GFT-001 | Gift Set | 17 | 700.00 | unknown | unknown | unknown |
| CUP-CER-001 | Ceramic Cup | 14 | 211.76 | 105.00 | 106.76 | 50.4% |
| POT-GLS-600 | Glass Teapot 600ml | 19 | 542.86 | 302.10 | 240.76 | 44.4% |
| TEA-BLK-100 | Black Tea 100g | 27 | 260.92 | 102.60 | 158.32 | 60.7% |
| TEA-GRN-100 | Green Tea 100g | 13 | 140.92 | 53.30 | 87.62 | 62.2% |
| TEA-MAT-030 | Matcha 30g | 8 | 161.34 | 77.60 | 83.74 | 51.9% |
| TEA-OOL-050 | Oolong 50g | 16 | 215.13 | 99.20 | 115.93 | 53.9% |

These amounts don't belong to any one product: 20.28 in order-level discounts and 70.50 in refunds. The product margins above don't include them.

VAT removed from prices: 0.19. Orders counted: 58.

**How this was counted**
- Orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm).
- A sale counts once it is paid, whether or not it has shipped (the usual answer; please confirm).
- Prices include VAT at 19% (as you said).

**To confirm**
- Test orders (tagged 'test', or paid through Shopify's test gateway): should they stay out of sales (the usual choice), or be counted?
- Does a sale count when it's paid, or only once it has shipped?

Until you confirm, the figures use the usual answers to these questions. A different answer would change them.
