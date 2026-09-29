# Case G: an Amazon seller's month-end, pinned

A third separate Claude session, which never saw the skills, built an Amazon seller account for testing month-end tools: a small US kitchen brand, mostly FBA, 60 SKUs, 9,130 orders from July to September 2026. It wrote the reports Seller Central gives: eight settlement reports (tab-separated, periods that cross month ends, a failed deposit, a negative settlement carried forward, a reserve), the monthly Date Range reports, the All Orders report (Windows-1252), and the bank's list of deposits, with an answer key from its own events. The data and the answer key are in `stores/amazon_g/`.

The owner's question each month: what did we sell, what did Amazon keep, what reached the bank and what does Amazon still owe us, ending with 10 lines for the bookkeeper. As in case F, some runs got the owner's definitions in words (the answer key's own) and some the question alone.

## Pinning July

The first setup session ran out of its 30 minutes: pin.py broke a copy of each of the 13 files seven ways and ran the whole calculation each time. pin.py now breaks one file of each kind (the largest). The same session also found that a pin wanted the very files it was pinned on, where a month brings as many settlement reports as it has; pin.py now treats files of one shape as one kind. A second session, given the first one's draft, pinned July in 19 turns (427 s, $0.97), with July's 10 lines all right:

- pin `ee1f712540ac`: 661 lines of Python over 13 files;
- the payments v1 definitions pack: 26 definitions decided, 14 from the owner's words, 6 as Claude's readings and 6 not applicable with the reason; 21 traps bound to checks or marked not applicable. The session noted that the pack is written for payment providers, so some of its wording reads oddly for Amazon: a marketplace pack was written after these runs, and has not run;
- broken copies: 19 caught, 3 no effect.

## The months

| Month | Runs with | Runs | Lines right | Lines alike in every run | Missed | Turns | Time | Cost | The plugin's own check passed |
|---|---|---|---|---|---|---|---|---|---|
| 2026-07 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 9–11 | 101–114 s | $0.49–$0.64 |  |
| 2026-07 | the pin, definitions in the prompt (the setup) | 1 | 10 of 10 | 10 of 10 | none | 19 | 427 s | $0.97 |  |
| 2026-08 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 10–13 | 113–148 s | $0.59–$0.79 |  |
| 2026-08 | the pin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 6–8 | 48–92 s | $0.39–$0.47 |  |
| 2026-08 | no plugin, the question alone | 3 | 6, 6, 7 of 10 | 9 of 10 | Net product sales, Orders, Owed by Amazon at month end, Refunds | 8–14 | 120–148 s | $0.51–$0.66 |  |
| 2026-08 | no plugin, the question and a definitions file | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 9–13 | 102–137 s | $0.51–$0.60 |  |
| 2026-08 | the pin, the question alone | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 8–9 | 118–188 s | $0.51–$0.83 | 2 of 3 |
| 2026-08 | the pin, the question alone (0.11.0: its answer check checked nothing) | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 6–7 | 53–98 s | $0.37–$0.47 |  |
| 2026-09 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 10–14 | 105–159 s | $0.64–$0.96 |  |
| 2026-09 | the pin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 6–7 | 60–88 s | $0.37–$0.46 |  |
| 2026-09 | no plugin, the question alone | 3 | 6, 7, 7 of 10 | 8 of 10 | Net product sales, Orders, Owed by Amazon at month end, Refunds | 10–11 | 127–140 s | $0.54–$0.71 |  |
| 2026-09 | no plugin, the question and a definitions file | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 13–16 | 126–133 s | $0.59–$0.77 |  |
| 2026-09 | the pin, the question alone | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 9–10 | 72–129 s | $0.43–$0.72 | 1 of 3 |
| 2026-09 | the pin, the question alone (0.11.0: its answer check checked nothing) | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 7–8 | 43–80 s | $0.31–$0.46 |  |

Cost is what Claude Code reports per session at list prices.

Plugin versions: the pin with definitions ran 0.11.0, the pin with the question alone 0.11.1 (its 0.11.0 runs are kept and marked); the runs without the plugin ran none.

With the definitions in the prompt, plain Opus got every line right in every run (on Stripe it got 10 of 11), and so did the pin. With the question alone:

- **no plugin:** 6/7 of 10 lines in 2026-08 and 6/7 of 10 lines in 2026-09 match the owner's definitions, and its runs did not all agree with each other. Its readings, as its answers state them: net product sales without shipping, gift wrap and promotions; in some runs the reserve counted inside what Amazon owes; in most, orders counted by the month their sale posted rather than their purchase date. Four of its six answers also flagged something the answer key does not grade: the failed deposit was followed by payouts to a new bank account, and they asked the owner to confirm the account was theirs;
- **no plugin, the definitions in a file:** 10 of 10 in every run;
- **the pin:** 10 of 10 in every run.

Here too the step that matters is the definitions written down once. Over the file, the pin took 8–10 turns against 9–16, at $0.64 a month on average against $0.63: no cheaper on this account, after $0.97 for the second setup session (the first ran out of time and reports no cost). Its own check passed 3 of 6 answers and flagged the others: they left out Claude's open questions or the export's shape warnings, retold the checked answer shorter or retyped its figures; one of them also had a settlement number read as an amount, which the check no longer does (fixed after these runs).

## Files

- `stores/amazon_g/`: the reports, the bank list, the answer key and the generator's notes;
- `results/pinned-g-runs.json`, `results/pinned-g-answers/`: every run's grades, turns, cost and final answer.
