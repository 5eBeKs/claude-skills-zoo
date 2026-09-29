> **Published here:** `report.md` and `key.json` (the answer key); `check.py` is not published, and the account it names as `../stripe-f` is `../stripe_f` here. This README was written by the session that built the data and describes its whole folder; the generator, its list of traps and its manifest stay private.

# Planted-mistake client report: Gridloft Studio, August 2026

A realistic month-end summary that a small bookkeeping agency would send a client, with seven mistakes planted on purpose. It is test input for tools that check such reports against Stripe data. Everything is fictional: the agency (Ledgerline Bookkeeping), the client (Gridloft Studio LLC) and its Stripe account, which is the synthetic account in `../stripe-f`.

## Files

| File | What it is |
|---|---|
| `report.md` | The report exactly as the client receives it. Nothing in it marks which figures are wrong. |
| `key.json` | **The answer key.** One entry per figure, in report order: `quote` (the passage word for word), `value` (as written), `verdict` (`right`, `wrong` or `not checkable`), `kind` (which of the seven mistake kinds, for wrong ones; otherwise null) and `truth` (the right figure and where it comes from in `truth.json`). |
| `check.py` | Self-check, Python standard library only. `python check.py [path/to/truth.json]` (default `../stripe-f/truth.json`). |

Give a tool under test only `report.md` and the `../stripe-f/exports` CSVs. Keep `key.json` for scoring.

## What the report contains

22 figures: 13 right, 7 wrong, 2 not checkable. A figure is any amount, count or percentage, written in digits or in words. Dates (the title month, the send date) are not figures, and `check.py` skips them. Five of the right figures are written differently from `truth.json`: two rounded amounts, two percentages and one count in words.

The two figures that cannot be checked (agency hours, Google Ads spend) come from outside Stripe. A good checker should say it cannot verify them, not call them right or wrong.

## How the mistakes were chosen

There are seven kinds, each a slip that really happens in month-end reporting, and each is used once:

1. a figure copied from the wrong month;
2. a gross amount given where the label says net;
3. two adjacent digits transposed;
4. a total that leaves out one of the parts its label names;
5. a payout total that counts a failed payout as paid;
6. a percentage computed on the wrong base, labelled with the usual base;
7. a figure that is right on a different, unstated definition.

Rules followed:

- Each wrong value is made from real `truth.json` values by one recipe for its kind, so it looks plausible and is wrong for exactly one reason. `check.py` rebuilds each wrong value from its recipe.
- Each wrong value differs from the truth at the precision the report shows it.
- The mistakes are spread over the table and the payouts, disputes and subscriptions paragraphs. Some leave the report inconsistent with itself, as real mistakes do. Others can only be caught against the exports or the definitions.
- Everything else follows `truth.json` and `meta.definitions`: August 2026 as a UTC month, amounts in USD, payouts counted by the month they left Stripe, and the balance excluding reserved funds.

## Precision rule

A right figure matches the truth when rounded the way the report writes it (half-up): cents for exact amounts, $1k for "about $139k", $0.1k for "about $10.1k", and the shown decimals for percentages.

## Judgement calls

- "Net of Stripe's processing fees" for euro payments means `by_currency.eur.gross_usd - fees_usd`. `truth.json` has no ready-made net figure per currency. The same figure can be rebuilt from the balance file: 562 charges, $17,641.65 gross, $1,117.64 fees.
- Dispute counts come from `lists.disputes_open_at_month_end`: 14 entries including one inquiry, two with status `needs_response`.
- MRR growth is measured against July's `subscriptions.mrr_closing`.
- "Paid out in August" follows `payouts.paid`: payouts created in August that did not fail, including the one still in transit at month end.

## What check.py verifies

- Every quote appears in `report.md` exactly once, contains its value, and the entries are in report order.
- Every `right` figure matches the truth at the shown precision, every `wrong` one does not and matches its recipe, and each `truth` text states the right figure.
- There is exactly one wrong figure of each kind 1 to 7, exactly two not-checkable figures, and at least three right figures written differently.
- Every number in `report.md`, in digits or in words and outside dates, falls inside some key quote.
