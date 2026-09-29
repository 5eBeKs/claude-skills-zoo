# Checking the report you already get

An agency's month-end report on the Stripe account of [DEFINITIONS.md](DEFINITIONS.md#the-stripe-account-f), checked figure by figure against the account's own exports: right, wrong (and what it should be), or cannot be checked from these files.


A separate session wrote the August report a bookkeeping agency would send (22 figures: 13 right, some rounded or as a percentage; 2 no Stripe export can check; 7 wrong, each a different kind: the wrong month, gross as net, two digits swapped, a total missing a part, a failed payout counted as paid, a percentage on the wrong base, a balance on an unstated definition) and kept the answer key apart. Both sides got the report, the exports, the owner's definitions and the same instruction: one line per figure, right, wrong or cannot check. With the skills: report-tie-out and the pin from above.

| | Right verdicts | Mistakes caught | False alarms on right figures | Said cannot check | Turns | Cost | The plugin's own check passed |
|---|---|---|---|---|---|---|---|
| no plugin | 16, 16, 16 of 22 | 6, 6, 6 of 7 | 2, 2, 2 of 13 | 2, 2, 2 of 2 | 12–13 | $0.68–$0.75 |  |
| the skills, 0.11.6 | 16, 16, 16 of 22 | 6, 6, 6 of 7 | 2, 2, 2 of 13 | 2, 2, 2 of 2 | 19–24 | $1.04–$1.15 | 3 of 3 |
| the skills, 0.11.5 (figures the pin lacks: computed or left unconfirmed) | 16, 12, 16 of 22 | 6, 4, 6 of 7 | 2, 0, 0 of 13 | 2, 2, 2 of 2 | 22–27 | $0.90–$1.09 | 3 of 3 |
| the skills, 0.11.4 (a value written with its currency refused) | 16, 16, 16 of 22 | 6, 6, 6 of 7 | 0, 0, 0 of 13 | 2, 2, 2 of 2 | 21–24 | $1.02–$1.08 | 1 of 3 |
| the skills, 0.11.1 at b989585 (the closing lines retyped) | 16, 16, 16 of 22 | 6, 6, 6 of 7 | 2, 2, 0 of 13 | 2, 2, 2 of 2 | 24–26 | $1.04–$1.24 | 0 of 3 |
| the skills, 0.11.1 (its result kept where the answer check did not look) | 16, 16, 16 of 22 | 6, 6, 6 of 7 | 2, 0, 2 of 13 | 2, 2, 2 of 2 | 26–32 | $0.92–$1.22 | 0 of 3 |
| the skills, first runs (the answer check failed every tie-out then) | 12, 16, 16 of 22 | 4, 6, 6 of 7 | 0, 0, 0 of 13 | 2, 2, 2 of 2 | 19–25 | $0.73–$0.95 | 0 of 3 |

What this shows, plainly: on this report the tie-out skill did no better than plain Opus. The runs on 0.11.6 give the same verdicts as plain Opus in every run: 16 of 22 right, the same six mistakes caught, the same two figures called wrong and the same two said to be uncheckable, at about 1.6 times the turns and a higher cost. Neither side caught the two swapped digits in MRR. The two figures both call wrong while the answer key has them right are subscription counts read another way (renewals with the first charge after a trial counted in; unpaid invoices counted with another cut for the voided ones): arguable readings. What the skill adds is not accuracy but a checked answer: on 0.11.6 the plugin's own check passed every tie-out answer, with every figure of the report accounted for (the one written in words is listed as not checked) and the closing lines rendered, not retyped.

That took six rounds of runs, all in the table. The check flagged every answer of the first three: it held a tie-out to the pin's month-end list (0.10.1); the tie-out's result was kept where the check did not look (0.11.1); the closing lines the prompt asks for retyped figures (0.11.1 at b989585). 0.11.2 rendered those lines, and a review found six faults in it (a right percentage read wrong, a sign not compared, figures that could be set aside quietly); 0.11.3 and 0.11.4 fixed them and what a second review found. On 0.11.4 the tie-out refused a value written with its currency ("$139,409.16", as the skill asked), and two runs of three gave it up and answered by hand; on 0.11.5 one run of three marked ten figures the files can give as unconfirmed, because the pin does not compute them. 0.11.6 says to compute such figures from the files, and its three runs are the ones above.

How it was graded: the grader was fixed after the first runs with the skills came in (a figure the report writes as "about $139k" was not found when an answer wrote "$139k"). The fix moved only those first runs, from 10, 14 and 14 right verdicts to 12, 16 and 16; every version's runs are kept. After the sixth review it also reads a figure written without its unit ("6.5" for "6.5 hours"), which moved one run of 0.11.1 from 15 to 16.

## Files

- `stores/stripe_f/`: the account's five exports and its answer key;
- `stores/stripe_f_report/`: the agency's report and its answer key;
- `results/tieout-f-runs.json`, `results/tieout-f-answers/`: every run's grades, turns, cost and final answer.
