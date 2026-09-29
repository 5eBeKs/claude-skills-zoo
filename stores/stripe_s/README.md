> **Published here:** the sixteen CSV exports (flat: there is no `exports/` folder here), `truth.json` (the answer key) and `NOTES.md`; `questions.md` is not published. This README was written by the session that built the data and describes its whole folder; the generator, its list of traps and its manifest stay private.

# Synthetic Stripe account - Brindlepost, Inc. (fictional)

A realistic, fully synthetic Stripe Billing account built to test month-end and subscription-metrics reporting tools.
Nothing here is real: company names are invented, e-mails use `example.com` / `example.net`, card numbers are 4 random digits.

## The business

- **Brindlepost, Inc.**, a US B2B SaaS selling a team collaboration tool on Stripe Billing. Account country US, settlement
  currency USD, account time zone **America/New_York**.
- Plans: **Starter** (per seat), **Team** (per seat), **Business** (flat base fee + per-seat item), monthly and annual,
  priced in USD, EUR and GBP. One-off items: onboarding package, workspace setup fee, admin training workshop.
  Eight enterprise customers are invoiced manually (send_invoice, net 30, paid by bank transfer, one by check).
- Stripe Tax from 2026-06-01 (US sales tax in NY, WA, TX, PA; EU reverse charge for VAT-registered customers).
- Automatic payouts in USD: daily until 2026-08-14, weekly (Wednesday) from 2026-08-19; one payout failed in July.
- Account settings changed during the period (see `TRAPS.md`, first section) - several traps come from those changes.

## The period

- Simulation starts **2026-03-01** with a zero balance; the existing customer base is migrated on 2026-03-02
  (subscriptions created with `trial_end` = old renewal date), then ~230-265 organic sign-ups a month.
- **Reporting period: July, August, September 2026.** Months are calendar months in America/New_York.
- Exports taken on **2026-10-03** (10:00 New York), so a few October objects are present.

## Volumes

- Customers: 2338 in `customers.csv` (+3 deleted), 1961 with a subscription live at some point in July-September, 1470 paid something in July-September.
- Subscriptions: 2335 (2703 rows in `subscriptions.csv`); at export: active 1580, past_due 23, trialing 92, unpaid 0, paused 72, canceled 545, incomplete 0, incomplete_expired 23.
- Invoices: 8728; at export: draft 5, open 28, paid 8576, uncollectible 27, void 92.
- Payments: 7739 live rows (succeeded and failed) + 5 test-mode rows; 59 refunds, 56 credit notes, 13 disputes, 119 payouts.
- MRR (primary definition) at month end: 2026-07 175,733.17 USD, 2026-08 197,365.93 USD, 2026-09 220,270.98 USD.

## Files

| file | rows | what it is |
|---|---|---|
| `exports/customers.csv` | 2338 | Dashboard > Customers > Export. Deleted customers are absent. `Balance` negative = credit owed to the customer. |
| `exports/subscriptions.csv` | 2703 | Dashboard > Subscriptions > Export, all statuses, one row per subscription item (Business = 2 rows). |
| `exports/invoices.csv` | 8728 | Dashboard > Invoices > Export, all statuses incl. drafts and voids. |
| `exports/invoice_line_items.csv` | 11258 | Invoice line items (not a standard Dashboard export - see NOTES.md). Carries the real service period of each line. |
| `exports/credit_notes.csv` | 56 | Credit notes (no documented Dashboard export - see NOTES.md). |
| `exports/payments.csv` | 7744 | Dashboard > Payments > Export (unified payments), live rows newest first, then 5 test-mode rows glued at the end. |
| `exports/balance_change_from_activity_itemized.csv` | 7036 | Reports > Balance > "Balance change from activity" itemized (balance_change_from_activity.itemized), 2026-03-01 to 2026-10-03, time zone America/New_York. No payouts in it. |
| `exports/payouts_itemized.csv` | 120 | Reports > Balance > "Payouts" itemized (payouts + payout reversals), same interval and time zone. |
| `exports/payouts.csv` | 119 | Dashboard > Payouts > Export. |
| `exports/disputes.csv` | 13 | Dashboard > Disputes > Export. |
| `exports/balance_summary_2026-07.csv` | 4 | Reports > Balance > Balance summary for July 2026 (America/New_York). |
| `exports/balance_summary_2026-08.csv` | 4 | Balance summary for August 2026. |
| `exports/balance_summary_2026-09.csv` | 4 | Balance summary for September 2026. |
| `exports/coupons.csv` | 10 | Product catalog > Coupons > Export. |
| `exports/promotion_codes.csv` | 9 | Promotion codes list. |
| `exports/prices.csv` | 32 | Product catalog > Prices export (catalog prices only; one-off enterprise prices are inline). |

Other files:

- `truth.json` - the answer key for 2026-07, 2026-08 and 2026-09 (plus a short summary of March-June), with every
  definition written in words in `meta.definitions` and alternatives where more than one definition is common.
  Computed from the event model inside `generate.py`, never from the CSVs.
- `questions.md` - 12 month-end questions a bookkeeper asks, each mapped to its place in `truth.json`.
- `TRAPS.md` - every trap with the ids it lives in.
- `NOTES.md` - every point where the Stripe format or behaviour was uncertain, with a confidence level; which
  timestamps are UTC and which are New York time.
- `MANIFEST.sha256` - SHA-256 of every file (including `generate.py`).

## Rebuild

```
python generate.py            # rebuilds every file above byte for byte (seed 20260301) and runs the self-checks
python generate.py --verify   # rebuilds into ./_verify_tmp, compares every file byte for byte, deletes ./_verify_tmp
```

Python 3 standard library only. Self-checks (run on every build): MRR roll-forward closes every month (USD with an FX
line, and per currency exactly); cash collected ties to the charge balance transactions (both time zones); fees and
refunds tie; every payout equals the net of the balance transactions it swept; every invoice's lines add up to its
subtotal, discount, tax and total, and amount due / paid / remaining are consistent with credit balance and credit notes;
credit notes add up; customer balances equal their ledger; the Stripe balance identity (start + activity - payouts = end)
and the deferred-revenue roll-forward hold every month.
