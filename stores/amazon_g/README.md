> **Published here:** the eight settlement reports, the three Date Range reports, the All Orders report and the bank's deposits (flat: no subfolders here), `truth.json` (the answer key) and `NOTES.md`. This README was written by the session that built the data and describes its whole folder; the generator, its list of traps and its manifest stay private.

# amazon-g: synthetic Amazon seller settlement data for month-end testing

Brambleford Kitchen Co. is a fictional small US brand selling kitchen goods on amazon.com. It is mostly FBA,
with some merchant-fulfilled (MFN) items, and has 60 SKU codes on 59 ASINs. About 9,100 orders were placed
from July to September 2026, and every report was taken on 2026-10-06 at 09:14 PDT. The seller keeps books
by calendar month in America/Los_Angeles.

## Rebuild

```
python generate.py            # rebuild every generated file byte for byte, then run the self-checks
python generate.py --check    # only run the self-checks against the files on disk
python generate.py --verify   # rebuild in a scratch sub-folder, compare every byte, delete the scratch folder
```

Python 3 standard library only, fixed seed (`SEED` in `generate.py`). The output does not depend on
`PYTHONHASHSEED` or the platform, and `MANIFEST.sha256` lists the hash of every generated file.
`README.md` and `NOTES.md` are written by hand; everything else is generated.

## Files

| path | what it is |
|---|---|
| `settlements/settlement_<id>.txt` (8) | Settlement report Flat File V2, tab-separated, one per settlement period that touches Jul-Sep: S1 (Jun 22 - Jul 6 PDT) to S7 (Sep 14 - Sep 28), plus the 3.5-hour negative stub S6a. The open settlement S8 (from Sep 28 20:15 PDT) has no file |
| `date_range/2026JulMonthlyTransaction.csv`, `...Aug...`, `...Sep...` | Date Range (unified) transaction report, one per Pacific calendar month, CSV with a preamble |
| `orders/all_orders_2026-07-01_2026-09-30.txt` | All Orders report (by purchase date, Pacific Jul 1 - Sep 30), tab-separated, Windows-1252 |
| `bank/disbursements.csv` | deposits as the seller's bank shows them, Jul 1 - Oct 6 (settlement id, bank date, amount, account) |
| `truth.json` | the answer key, computed from the event model inside `generate.py`, never from the files |
| `TRAPS.md` | every trap with the ids where it occurs (44 traps), plus a table of all settlement periods |
| `traps_ids.json` | the same traps with complete id lists |
| `NOTES.md` | what I was unsure about in Amazon's formats, with confidence, and which date puts each item in a month |
| `MANIFEST.sha256` | sha256 of every generated file |
| `generate.py` | the event model, the writers, truth, traps and self-checks |

## truth.json

`months["2026-07" | "2026-08" | "2026-09"]` has `sales`, `amazon_fees`, `advertising`, `reimbursements`,
`tax`, `disbursements` (bank-dated deposits plus `failed`), `owed_by_amazon_at_month_end`, `orders`,
`excluded` and `lists` (claims open at month end, orders refunded in a later month). Money is in USD, using
the settlement sign (money to the seller is positive). `meta` holds the seller, the time zones, the report
time, file counts, definitions, the opening balance at 2026-06-30, a month roll-forward and the list of
settlements. The month rules are in NOTES.md, section 1.

## Self-checks (run on every build)

- Each settlement file's `total-amount` equals the sum of its lines, and each file has 24 columns.
- Every positive settlement is either in the bank list at exactly its total, or is the failed one. The
  failed one is absent from the bank and comes back as a `Failed disbursement` line in a later file. A
  non-positive settlement has no deposit.
- No posted-date-time, settlement end, deposit-date, bank date or order date falls after the report time.
- Consecutive files chain: end = next start, `Previous Reserve Amount Balance` = previous
  `Current Reserve Amount`, and a negative total comes back as `Payable to Amazon`.
- Months roll forward: opening owed + activity - deposits = closing owed, for July, August and September.
- In each Date Range report, the total of all non-Transfer rows equals truth's activity for that month. Each
  row sums across its columns, and every row falls inside its Pacific month.
- The orders report's order and cancellation counts per Pacific month equal truth.
- Truth's parts sum to its totals, and facilitator tax nets to zero.

## How the account behaves (short)

- Settlements run every 14 days from 03:15:44 UTC (20:15 PDT the previous evening). Order lines are paid
  under DD+7, in the settlement where they are released, but keep their original posted date. Every
  settlement has reserve lines.
- S4 (Aug 3-17) could not be paid: the old bank account was closed, so the ACH was returned. The money comes
  back in S5 as a `Failed disbursement` line.
- The seller clicked Request Transfer on Aug 31 at 16:42 PDT. That closed S5 early and left a 3.5-hour stub,
  S6a, holding only the subscription fee, the month-end ads invoice and a few refunds. S6a is negative and is
  carried into S6 as `Payable to Amazon`.
- S7's deposit was started Sep 29 PDT but reached the bank Oct 1, so it is in transit at September month end.
- Lines posted after Sep 28 20:15 PDT, and September orders not yet released under DD+7, are in no settlement
  file. Only the September Date Range report has them.
