I've stopped before computing anything: the margin script needs to know what VAT rate is included in your prices. I can't find a `store_definitions.json` that records it, and I'd rather not guess, because the rate I remove changes every product's revenue and margin.

The export suggests the answer isn't simple:

- The store sells in USD, and the `Taxes` column is filled in.
- On at least one UK order (#79066), the tax already seems to be part of the price. The subtotal (58.11) plus shipping (13.41) equals the total (71.51, give or take a cent). The 11.93 of tax is about 1/6 of that, which is what 20% UK VAT looks like when it's included in the price.

**What VAT rate, if any, is included in your listed prices?**

- **If prices never include tax (US-style, tax added at checkout), the rate is 0.** The script still takes the tax out of orders like the UK one above, using the tax recorded on each order.
- **If your prices include VAT, give me the rate** (for example 0.20).

Once you tell me, I'll run it for July 2026. You'll get a list of products that made money, products sold below cost, and products I can't judge because the products export has no cost for them. I'll also show which orders were left out and why.
