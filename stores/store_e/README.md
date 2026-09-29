> **Published here:** the four CSV exports, `truth.json` (the answer key) and `NOTES.md`; the orders export holds 21,241 orders, 709 of them in October. This README was written by the session that built the data and describes its whole folder; the generator, its list of traps and its manifest stay private.

# store-e: synthetic Shopify store for testing month-end reporting

A fictional Dutch home-goods store ("Kade & Klei Wonen", shop currency EUR, prices include VAT, OSS)
selling in EUR, GBP, USD and CHF, with Shopify Payments (cards, iDEAL, Apple Pay), Klarna, PayPal,
bank transfer, gift cards and a POS showroom. Period July-September 2026, about 20,500 orders; exports taken
Sunday 4 Oct 2026 10:15 Europe/Amsterdam. All data is invented.

## Files

| File | What it is |
|---|---|
| `orders_export.csv` | Admin > Orders > Export, one row per line item, created on/after 1 Jul (1-4 Oct included) |
| `payment_transactions_export.csv` | Shopify Payments transactions, from 26 May |
| `payouts_export.csv` | Shopify Payments payouts, from 1 Jun (5 Oct payout scheduled) |
| `products_export.csv` | Products, old CSV template (Handle, Title, Variant SKU, ..., Cost per item) |
| `truth.json` | The correct month-end figures for 2026-07/08/09, computed from the event model, never from the CSVs |
| `TRAPS.md` | Table of every trap, then each trap's orders (or payouts) under a `### T<nn>` heading |
| `NOTES.md` | Every format / definition decision with its confidence |
| `SHA256SUMS` | Hashes of the six generated files |
| `generate.py`, `sim/` | The generator (Python 3 standard library only) |

## Rebuild

```
python generate.py            # rebuilds the six files byte for byte, runs self-checks, writes SHA256SUMS
python generate.py --verify   # rebuilds in memory and compares with the files on disk
```

Seed 20261004, about 15 s. Output does not depend on `PYTHONHASHSEED`, locale or time zone of the machine
(no system time-zone data is used; the store offset is asserted for every moment). The files are UTF-8
without BOM with LF line endings.

## Self-checks (run on every build; the build fails if any fails)

- no event after the export moment, none before the order it belongs to; no unit returned twice and no
  refund above the money captured
- every payout equals its transactions + Retried Amount, in the model and re-read from the written CSVs
  (and Charges/Refunds/Adjustments/Reserved Funds/Fees each tie to the rows)
- money in transit rolls forward Jul -> Aug -> Sep (closing = opening + net activity − deposited) and equals the
  unsettled transactions at each month end, computed a second, independent way
- sales identities (net = gross + discounts + returns; total = net + shipping + duties + fees + taxes),
  margin by SKU ties to net sales, order counts in truth equal the orders export minus test orders
- every trap in TRAPS.md has at least one order or payout

## Generator layout

| Module | Role |
|---|---|
| `sim/core.py` | seed streams, cents, store clock, FX rates, business days, export filters |
| `sim/refdata.py` | countries and VAT, names/addresses, catalog, discount codes, shipping |
| `sim/entities.py` | variants with SKU/cost/title history and deletion, customers |
| `sim/specs.py` | daily order arrivals plus the explicitly injected scenarios |
| `sim/orders.py` | order/line pricing (tax-inclusive, discounts, shipping, duties) and state at any moment |
| `sim/build.py` | lifecycle: payments, fulfilment, edits, exchanges, refunds, cancellations, chargebacks, reserve |
| `sim/payments.py` | Shopify Payments ledger, fees, payout grouping, failed payout and retry |
| `sim/analytics.py` | Shopify-Analytics-style sales ledger (reversals on their own day) |
| `sim/truth.py` | truth.json |
| `sim/exports.py` | the four CSV layouts |
| `sim/traps.py` | trap detection and TRAPS.md |
| `sim/checks.py` | self-checks |

## truth.json in short

`meta` (store, timezone, shop_currency, presentment_currencies, exports_taken_at, file_counts, export filters)
and `months["2026-07" | "2026-08" | "2026-09"]` with `sales`, `orders`, `shopify_payments`, `payouts`,
`money_in_transit`, `other_payment_methods`, `receivables_closing`, `margin`, `excluded_orders`.
Amounts are EUR numbers; discounts, returns, refunds, chargebacks and fees are negative. Definitions are
in NOTES.md sections 7-8.
