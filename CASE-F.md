# Case F: the same Stripe month-end, pinned

A separate Claude session that never saw the skills built a Stripe account for testing month-end tools: Gridloft Studio LLC, US, customers paying in USD, EUR, GBP, CAD, July to September 2026, one-off purchases and a subscription with trials, coupons, dunning and credit, disputes won, lost and open, a rolling reserve, a failed payout, test-mode rows glued under a live export. It wrote five exports as Stripe gives them (the payments, invoices, subscriptions and payouts lists and the itemized balance report) and an answer key computed from its own events, never from the files. The data and the answer key are in `stores/stripe_f/`.

The owner's question each month: what did we sell, what did Stripe keep, what reached the bank and what is still on its way, ending with 11 lines for the bookkeeper. The runs with the definitions got the owner's definitions in words, word for word, with the plugin or without it: they are the answer key's own definitions, so both sides count the same thing. The runs marked "the question alone" got the question and the bookkeeper lines only. Graded to the cent against the answer key (a sign is layout, not a figure).

## Pinning July

The first session, with the pinned-calculation skill, wrote the calculation and tried it on July. One of its own checks failed: 43 July charges have their sales tax in no file, because the payments and invoices exports start at 05:00 UTC on July 1 (midnight in the account's time zone), $1,176.69 of gross charges. It did not pin, and asked for the two files again from before July 1 in UTC. On the way it found a bug in the plugin's own pin.py (a pin over several files crashed); an edit to the plugin was refused, so it said so and ran a fixed copy. The bug is fixed in the plugin, with a test.

Plain Opus on July saw the same gap and filled it: it took the tax of 31 subscription payments from the same subscription's other invoices, assumed no tax on 11 whole-dollar US orders, worked out the tax of the 12th (a Canadian order) from its amount, and said so.

The owner's answer to the first session: the files cannot be exported again; count the tax the files give, name those charges, and pin. A second session, given the first one's draft, pinned it:

- pin `d8c663a3d3cd`: the calculation (522 lines of Python), the answer template and the definitions in one file, which the owner keeps;
- the payments v1 definitions pack: 30 definitions decided and recorded before the pin (the first session wrote them after trying its calculation on the months), 16 from the owner's words, 2 not applicable with the reason and 12 as Claude's readings, which stay open questions in every answer until the owner answers them; 24 traps of the pack, 22 bound to a check the calculation computes and the rest marked not applicable with the reason;
- broken copies of the owner's files (rows twice, amounts in cents, a decimal comma, times shifted, a new kind of row, amounts a cent off, the last days missing): 25 caught, 7 no effect. The breaks with no effect: rows exported twice (every 50th) (subscriptions.csv), the last three days missing (balance_transactions_itemized.csv), the last three days missing (invoices.csv), the last three days missing (subscriptions.csv), the last three days missing (unified_payments.csv), times written eight hours later (another time zone) (payouts.csv), times written eight hours later (another time zone) (subscriptions.csv).

Pinning took the two sessions: 37 turns, 803 s, $3.02 and 19 turns, 404 s, $0.85, with the plugin's hooks off (pinning asks the owner in a dialog `claude -p` cannot show; the prompt carried the owner's yes). July's pinned answer carries the definitions and readings, not the checks' lines, which came in a later version.

## The months

| Month | Runs with | Runs | Lines right | Lines alike in every run | Missed | Turns | Time | Cost | The plugin's own check passed |
|---|---|---|---|---|---|---|---|---|---|
| 2026-07 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 10 of 11 | Sales tax collected | 15–21 | 173–193 s | $0.93–$1.02 |  |
| 2026-07 | the pin, definitions in the prompt (the setup) | 1 | 10 of 11 | 11 of 11 | Sales tax collected | 19 | 404 s | $0.85 |  |
| 2026-08 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 12–16 | 112–137 s | $0.63–$0.77 |  |
| 2026-08 | the pin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 7–8 | 94–123 s | $0.43–$0.59 |  |
| 2026-08 | no plugin, the question alone | 3 | 4, 4, 4 of 11 | 11 of 11 | Gross charges, Held in reserve at month end, Net volume, Paid out to the bank, Sales tax collected, Stripe balance at month end, Stripe fees | 9–13 | 127–144 s | $0.70–$0.84 |  |
| 2026-08 | no plugin, the question and a definitions file | 3 | 10, 10, 10 of 11 | 10 of 11 | Sales tax collected | 11–15 | 107–148 s | $0.60–$0.85 |  |
| 2026-08 | the pin, the question alone | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6–8 | 97–125 s | $0.47–$0.62 | 2 of 3 |
| 2026-08 | the pin, the question alone (0.11.0: its answer check checked nothing) | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6 | 34–91 s | $0.29–$0.47 |  |
| 2026-09 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 9–12 | 86–123 s | $0.55–$0.69 |  |
| 2026-09 | the pin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6 | 87–88 s | $0.46 |  |
| 2026-09 | no plugin, the question alone | 3 | 3, 3, 3 of 11 | 10 of 11 | Gross charges, Held in reserve at month end, Net volume, Paid out to the bank, Refunds, Sales tax collected, Stripe balance at month end, Stripe fees | 13–15 | 134–166 s | $0.68–$0.98 |  |
| 2026-09 | no plugin, the question and a definitions file | 3 | 10, 10, 10 of 11 | 10 of 11 | Sales tax collected | 11–15 | 104–153 s | $0.50–$0.78 |  |
| 2026-09 | the pin, the question alone | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6–8 | 57–131 s | $0.38–$0.64 | 2 of 3 |
| 2026-09 | the pin, the question alone (0.11.0: its answer check checked nothing) | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6 | 87–92 s | $0.47–$0.48 |  |

Cost is what Claude Code reports per session at list prices. Plugin versions: the pin with definitions ran 0.10.1, the pin with the question alone 0.11.1 (its 0.11.0 runs are kept and marked: that version's answer check did not read a pin's results); the runs without the plugin ran none.

With the definitions written into the prompt, plain Opus and the pin give the same lines: 10 of 11 in every run. The one line both miss is sales tax, by cents: 2026-07: the answer key $8,034.81, the runs $7,991.58, $8,033.76, $8,034.90; 2026-08: the answer key $8,405.00, the runs $8,404.78, $8,404.87; 2026-09: the answer key $8,411.00, the runs $8,410.74, $8,410.83. The answer key converts and rounds each charge's tax in a way neither side reproduces; July's pinned figure is also short by the tax of the 43 charges the owner accepted.

An owner does not write eleven definitions into every month's question, so three more arms ask the question alone (with the bookkeeper lines):

- **no plugin:** 4 of 11 lines in 2026-08 and 3 of 11 lines in 2026-09 match the owner's definitions, the same in every run, on its own readings, as its answers state them: the month in the account's local time rather than UTC, and a payout dated by the day it reached the bank rather than the day it left Stripe. Both are defensible; they are not the owner's;
- **no plugin, the definitions in a file** the question points to: 10 of 11 lines, as with the definitions in the prompt; the tax line differs by cents between its runs;
- **the pin:** 10 of 11 lines in every run, the tax line the same in every run.

So the step that matters is having the owner's definitions written down once: 3 or 4 lines of 11 become 10, whether they sit in a file or in a pin. What the pin adds over the file, measured here: fewer turns (6–8 against 11–15); a cost per month of $0.53 on average against $0.67, after the one-time $3.86 of pinning (at that difference, the pinning pays for itself against the file in about 27 months); the plugin's own check on every answer, which passed 4 of 6 and flagged the others at the end, for leaving out the open questions about Claude's readings; and, at pin time, the refusal to pin July on incomplete files.

## The same account: checking the agency's report

A separate session wrote the August report a bookkeeping agency would send (22 figures: 13 right, some rounded or as a percentage; 2 no Stripe export can check; 7 wrong, each a different kind: the wrong month, gross as net, two digits swapped, a total missing a part, a failed payout counted as paid, a percentage on the wrong base, a balance on an unstated definition) and kept the answer key apart. Both sides got the report, the exports, the owner's definitions and the same instruction: one line per figure, right, wrong or cannot check. With the skills: report-tie-out and the pin from above.

| | Right verdicts | Mistakes caught | False alarms on right figures | Said cannot check | Turns | Cost |
|---|---|---|---|---|---|---|
| no plugin | 16, 16, 16 of 22 | 6, 6, 6 of 7 | 2, 2, 2 of 13 | 2, 2, 2 of 2 | 12–13 | $0.68–$0.75 |
| the skills, latest | 16, 16, 16 of 22 | 6, 6, 6 of 7 | 2, 2, 0 of 13 | 2, 2, 2 of 2 | 24–26 | $1.04–$1.24 |
| the skills, 0.11.1 (its result kept where the answer check did not look) | 16, 16, 16 of 22 | 6, 6, 6 of 7 | 2, 0, 2 of 13 | 2, 2, 2 of 2 | 26–32 | $0.92–$1.22 |
| the skills, first runs (the answer check failed every tie-out then) | 12, 16, 16 of 22 | 4, 6, 6 of 7 | 0, 0, 0 of 13 | 2, 2, 2 of 2 | 19–25 | $0.73–$0.95 |

What this shows, plainly: on this report the tie-out skill did no better than plain Opus. The latest runs give as many right verdicts and catch the same six mistakes, at about twice the turns and a higher cost; one of them said "cannot check" where plain Opus said wrong. Neither side caught the two swapped digits in MRR. Plain Opus's two "false alarms" are subscription counts it read another way (renewals with the first charge after a trial counted in; unpaid invoices counted with another cut for the voided ones): arguable readings, and the skill made the same two in two of its three latest runs. The check refused the one figure the report writes in words ("two"), and the runs dropped it: they checked 21 of the report's 22 figures.

The plugin's own check flagged every tie-out answer, in all three versions. First, because it held a tie-out to the pin's month-end list (fixed in 0.11.1); then because the tie-out's result was kept where the check did not look; in the latest runs, because the closing lines the prompt asks for retyped figures and the report's percentages did not trace (all three runs), one answer also typed a figure in its prose, and in one the tie-out's result was again not where the check looked. The version after these runs rendered the closing lines itself, but in a form of its own (no $, % or hours, counts written as money); 0.11.2 renders them in the report's own form, sends back any closing line that is not the rendered one, and keeps the result and its claim map where the check looks. Neither is re-run here.

How it was graded: the grader was fixed after the first runs with the skills came in (a figure the report writes as "about $139k" was not found when an answer wrote "$139k"). The fix moved only those first runs, from 10, 14 and 14 right verdicts to 12, 16 and 16; every version's runs are kept. After the sixth review it also reads a figure written without its unit ("6.5" for "6.5 hours"), which moved one run of 0.11.1 from 15 to 16.

## Files

- `stores/stripe_f/`: the five exports, the answer key and the generator's notes;
- `stores/stripe_f_report/`: the agency's report and its answer key;
- `results/pinned-f-runs.json`, `results/tieout-f-runs.json`: every run's grades, turns and cost;
- `results/pinned-f-answers/`, `results/tieout-f-answers/`: every final answer.
