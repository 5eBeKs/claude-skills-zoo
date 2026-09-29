> **Published here:** the five CSV exports (flat: there is no `exports/` folder here), `truth.json` (the answer key) and `NOTES.md`. This README was written by the session that built the data and describes its whole folder; the generator, its list of traps and its manifest stay private.

# Synthetic Stripe account: Gridloft Studio LLC (Q3 2026)

A made-up but realistic Stripe account for testing month-end reporting and reconciliation tools. Every name, id, customer and amount is fictional.

- **Business:** sells digital design assets through Stripe Checkout, plus the "Gridloft Pro" subscription through Stripe Billing: $19/month or $190/year, with prices in EUR, GBP and CAD too. There are also a few team licences on manual invoices paid by ACH. No Shopify.
- **Account:** `acct_1Qm7cT9fHvRz2kWb`, country US, default and settlement currency USD, customers pay in USD/EUR/GBP/CAD, account timezone America/Chicago.
- **Period:** July to September 2026, about 12,200 successful payments. Exports were taken on **2026-10-04 15:42:10 UTC** (10:42 in Chicago).
- **Simulation:** starts 2026-05-01 with a zero balance, so the July opening balance, June refunds and disputes, and the June payout that arrives on July 1 are all real.

## Files

| File | What it is |
|---|---|
| `exports/unified_payments.csv` | Dashboard payments export, "Jul 1 to Sep 30" in the account timezone, state as of export. A test-mode export was appended at the bottom (`Mode=Test`). |
| `exports/balance_transactions_itemized.csv` | Itemized balance transactions, 2026-07-01 00:00 UTC to 2026-10-04 00:00 UTC, all reporting categories (charge, refund, refund_failure, dispute, dispute_reversal, fee, other_adjustment, risk_reserved_funds, payout, payout_reversal). |
| `exports/payouts.csv` | Dashboard payouts export (arrival on or after July 1), including one failed and one in-transit payout. |
| `exports/invoices.csv` | Dashboard invoices export (created from Jul 1 Chicago time to the export moment). |
| `exports/subscriptions.csv` | Dashboard subscriptions export (everything not ended before July 1). |
| `truth.json` | Expected month-end figures computed from the event model, never from the CSVs. Definitions are in `meta.definitions`. |
| `TRAPS.md` | Every trap with the ids it lives in (generated). |
| `NOTES.md` | Every point where I was unsure how Stripe writes something, with a confidence level (hand-written). |
| `MANIFEST.sha256` | SHA-256 of every generated file. |
| `build.py`, `gen/` | The generator (Python 3 standard library only, fixed seed `20261004`). |

## Rebuild

```
python build.py            # regenerates exports/, truth.json, TRAPS.md, MANIFEST.sha256 and runs self-checks
python build.py --verify   # builds a second copy in .verify/ and compares byte for byte (then deletes it)
```

The build takes a few seconds. It prints each self-check and exits non-zero if one fails. README.md and NOTES.md are hand-written and are not regenerated.

The self-checks:
- every payout equals the sum of its balance transactions, both in the model and in the file (the first July payouts also sweep late-June rows, which are outside the file window, and the check accounts for them);
- for each month, opening + activity - payouts = closing, in the model and again from the balance file using truth's opening and closing balances;
- charge gross and fees in the balance file match truth;
- every live successful row in the payments export matches its charge balance transaction;
- test-mode ids never appear in the balance file;
- no event and no file timestamp is after the export moment (future-dated fields such as arrival date, period end and next retry are exempt), and no balance row is after the report's data end.

## truth.json in one paragraph

`months["2026-07"|"2026-08"|"2026-09"]` has `volume`, `fees`, `payouts`, `balance`, `subscriptions`, `excluded` and `lists` exactly as specified. `extra` adds the full balance bridge (opening, each activity component, payouts, closing, difference = 0), the successful payment count, active and trialing subscription counts, and the ids of in-transit payouts. `meta` holds the account, timezones, currencies, export moment, file row counts, each export's window, month-end FX rates and the definition of every figure. Months are UTC. Refunds, disputes and reversals are in USD at the rate of the day they happened (see NOTES.md, G4 to G6).

## Generator layout

`gen/config.py` holds the parameters. `world.py` builds customers, cards, FX, charges, refunds and disputes. `sim_onetime.py` covers Checkout purchases and the test-mode rows. `sim_subs.py` covers subscriptions, dunning, trials, coupons, credit and upgrades. `scenarios.py` places the guaranteed trap events and the B2B invoices. `ledger.py` builds balance transactions, usage fees, the reserve, the adjustment and payouts. `export_csv.py` writes the CSVs, `truth.py` writes truth.json, `traps.py` writes TRAPS.md and `checks.py` runs the self-checks.
