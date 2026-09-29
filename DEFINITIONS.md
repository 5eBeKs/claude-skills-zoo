# Your definitions, written down once

The same month-end question, every month, on accounts built by separate Claude sessions that never saw the skills, each with an answer key worked out from its own events: a Stripe account (case F), an Amazon seller account (case G) and a subscription business on Stripe Billing (case H: MRR, churn, billings and recognised revenue). Each month's answer ends with the lines a bookkeeper asks for, graded to the cent against the answer key. The owner asks in three ways: the question alone (no plugin); the question and a file with the owner's definitions (no plugin); the question alone with a pinned calculation (the plugin, and the pin the owner keeps). August and September, three runs each; Opus 5.5.

| Account | The question alone | With a definitions file | With the pin | Turns, file / pin | Cost a month, file / pin | The pin's own check passed |
|---|---|---|---|---|---|---|
| Stripe account (F) | 3–4 of 11 | 10 of 11 every run | 10 of 11 every run | 11–15 / 6–9 | $0.67 / $0.46 | 6 of 6 |
| Amazon seller account (G) | 6–7 of 10 | 10 of 10 every run | 10 of 10 every run | 9–16 / 6–9 | $0.63 / $0.55 | 4 of 6 |
| SaaS on Stripe Billing (H) | 2–4 of 12 | 5–6 of 12 | 7 of 12 every run that answered (1 of 6 stopped and asked for a file) | 22–42 / 7–16 | $2.53 / $0.73 | 3 of 6 |

- **The step that matters is the definitions, written down once.** Asked plainly, Opus answers on readings of its own (the month in local time, a payout by the day it reached the bank, the reserve inside what is owed): each defensible, not the owner's. The same question pointing to a file of the owner's definitions gets the owner's lines in every run on F and G. On H it gets the money right and not the subscriptions: the export gives each subscription's status on the day it was taken, and only the pin, whose pack asks how the month-end state is found, rebuilt it.
- **What the pin adds over the file:** the same figure in every run (on Stripe the file's tax line moved by cents), fewer turns, and the plugin's own check on every answer; at pin time, broken copies of the owner's files to show which checks fire, and a refusal to pin a month on incomplete exports until the owner decides. It costs a setup session once.
- **What it does not do:** the line both miss on Stripe is sales tax, by cents. On H no run reaches MRR to the cent: the answer key knows the moment a seat change or a retention coupon took effect, which no export records. The data is synthetic.

How a pin is made (definitions asked with a pack of questions for the kind of export, the calculation written and tried with the owner, then frozen in one file the owner keeps) and every month's runs are in the sections below.

## The Stripe account (F)

A separate Claude session that never saw the skills built a Stripe account for testing month-end tools: Gridloft Studio LLC, US, customers paying in USD, EUR, GBP, CAD, July to September 2026, one-off purchases and a subscription with trials, coupons, dunning and credit, disputes won, lost and open, a rolling reserve, a failed payout, test-mode rows glued under a live export. It wrote five exports as Stripe gives them (the payments, invoices, subscriptions and payouts lists and the itemized balance report) and an answer key computed from its own events, never from the files. The data and the answer key are in `stores/stripe_f/`.

The owner's question each month: what did we sell, what did Stripe keep, what reached the bank and what is still on its way, ending with 11 lines for the bookkeeper. The runs with the definitions got the owner's definitions in words, word for word, with the plugin or without it: they are the answer key's own definitions, so both sides count the same thing. The runs marked "the question alone" got the question and the bookkeeper lines only. Graded to the cent against the answer key (a sign is layout, not a figure).

### Pinning July

The first session, with the pinned-calculation skill, wrote the calculation and tried it on July. One of its own checks failed: 43 July charges have their sales tax in no file, because the payments and invoices exports start at 05:00 UTC on July 1 (midnight in the account's time zone), $1,176.69 of gross charges. It did not pin, and asked for the two files again from before July 1 in UTC. On the way it found a bug in the plugin's own pin.py (a pin over several files crashed); an edit to the plugin was refused, so it said so and ran a fixed copy. The bug is fixed in the plugin, with a test.

Plain Opus on July saw the same gap and filled it: it took the tax of 31 subscription payments from the same subscription's other invoices, assumed no tax on 11 whole-dollar US orders, worked out the tax of the 12th (a Canadian order) from its amount, and said so.

The owner's answer to the first session: the files cannot be exported again; count the tax the files give, name those charges, and pin. A second session, given the first one's draft, pinned it:

- pin `d8c663a3d3cd`: the calculation (522 lines of Python), the answer template and the definitions in one file, which the owner keeps;
- the payments v1 definitions pack: 30 definitions decided and recorded before the pin (the first session wrote them after trying its calculation on the months), 16 from the owner's words, 2 not applicable with the reason and 12 as Claude's readings, which stay open questions in every answer until the owner answers them; 24 traps of the pack, 22 bound to a check the calculation computes and the rest marked not applicable with the reason;
- broken copies of the owner's files (rows twice, amounts in cents, a decimal comma, times shifted, a new kind of row, amounts a cent off, the last days missing): 25 caught, 7 no effect. The breaks with no effect: rows exported twice (every 50th) (subscriptions.csv), the last three days missing (balance_transactions_itemized.csv), the last three days missing (invoices.csv), the last three days missing (subscriptions.csv), the last three days missing (unified_payments.csv), times written eight hours later (another time zone) (payouts.csv), times written eight hours later (another time zone) (subscriptions.csv).

Pinning took the two sessions: 37 turns, 803 s, $3.02 and 19 turns, 404 s, $0.85, with the plugin's hooks off (pinning asks the owner in a dialog `claude -p` cannot show; the prompt carried the owner's yes). July's pinned answer carries the definitions and readings, not the checks' lines, which came in a later version.

### The months

| Month | Runs with | Runs | Lines right | Lines alike in every run | Missed | Turns | Time | Cost | The plugin's own check passed |
|---|---|---|---|---|---|---|---|---|---|
| 2026-07 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 10 of 11 | Sales tax collected | 15–21 | 173–193 s | $0.93–$1.02 |  |
| 2026-07 | the pin, definitions in the prompt (the setup) | 1 | 10 of 11 | 11 of 11 | Sales tax collected | 19 | 404 s | $0.85 |  |
| 2026-08 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 12–16 | 112–137 s | $0.63–$0.77 |  |
| 2026-08 | the pin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 7–8 | 94–123 s | $0.43–$0.59 |  |
| 2026-08 | no plugin, the question alone | 3 | 4, 4, 4 of 11 | 11 of 11 | Gross charges, Held in reserve at month end, Net volume, Paid out to the bank, Sales tax collected, Stripe balance at month end, Stripe fees | 9–13 | 127–144 s | $0.70–$0.84 |  |
| 2026-08 | no plugin, the question and a definitions file | 3 | 10, 10, 10 of 11 | 10 of 11 | Sales tax collected | 11–15 | 107–148 s | $0.60–$0.85 |  |
| 2026-08 | the pin, the question alone | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6–8 | 90–97 s | $0.44–$0.47 | 3 of 3 |
| 2026-08 | the pin, the question alone (0.11.1) | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6–8 | 97–125 s | $0.47–$0.62 |  |
| 2026-08 | the pin, the question alone (0.11.0: its answer check checked nothing) | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6 | 34–91 s | $0.29–$0.47 |  |
| 2026-09 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 9–12 | 86–123 s | $0.55–$0.69 |  |
| 2026-09 | the pin, definitions in the prompt | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6 | 87–88 s | $0.46 |  |
| 2026-09 | no plugin, the question alone | 3 | 3, 3, 3 of 11 | 10 of 11 | Gross charges, Held in reserve at month end, Net volume, Paid out to the bank, Refunds, Sales tax collected, Stripe balance at month end, Stripe fees | 13–15 | 134–166 s | $0.68–$0.98 |  |
| 2026-09 | no plugin, the question and a definitions file | 3 | 10, 10, 10 of 11 | 10 of 11 | Sales tax collected | 11–15 | 104–153 s | $0.50–$0.78 |  |
| 2026-09 | the pin, the question alone | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6–9 | 71–91 s | $0.44–$0.47 | 3 of 3 |
| 2026-09 | the pin, the question alone (0.11.1) | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6–8 | 57–131 s | $0.38–$0.64 |  |
| 2026-09 | the pin, the question alone (0.11.0: its answer check checked nothing) | 3 | 10, 10, 10 of 11 | 11 of 11 | Sales tax collected | 6 | 87–92 s | $0.47–$0.48 |  |

Cost is what Claude Code reports per session at list prices. Plugin versions: the pin with definitions ran 0.10.1, the pin with the question alone 0.11.6 (its 0.11.1 and 0.11.0 runs are kept and marked; 0.11.0's answer check did not read a pin's results); the runs without the plugin ran none.

With the definitions written into the prompt, plain Opus and the pin give the same lines: 10 of 11 in every run. The one line both miss is sales tax, by cents: 2026-07: the answer key $8,034.81, the runs $7,991.58, $8,033.76, $8,034.90; 2026-08: the answer key $8,405.00, the runs $8,404.78, $8,404.87; 2026-09: the answer key $8,411.00, the runs $8,410.74, $8,410.83. The answer key converts and rounds each charge's tax in a way neither side reproduces; July's pinned figure is also short by the tax of the 43 charges the owner accepted.

An owner does not write eleven definitions into every month's question, so three more arms ask the question alone (with the bookkeeper lines):

- **no plugin:** 4 of 11 lines in 2026-08 and 3 of 11 lines in 2026-09 match the owner's definitions, the same in every run, on its own readings, as its answers state them: the month in the account's local time rather than UTC, and a payout dated by the day it reached the bank rather than the day it left Stripe. Both are defensible; they are not the owner's;
- **no plugin, the definitions in a file** the question points to: 10 of 11 lines, as with the definitions in the prompt; the tax line differs by cents between its runs;
- **the pin:** 10 of 11 lines in every run, the tax line the same in every run.

So the step that matters is having the owner's definitions written down once: 3 or 4 lines of 11 become 10, whether they sit in a file or in a pin. What the pin adds over the file, measured here: fewer turns (6–9 against 11–15); a cost per month of $0.46 on average against $0.67, after the one-time $3.86 of pinning (at that difference, the pinning pays for itself against the file in about 18 months); the plugin's own check on every answer, which passed 6 of 6 on 0.11.6 (on 0.11.1, 4 of 6: the others had left out the open questions about Claude's readings); and, at pin time, the refusal to pin July on incomplete files.

### Anthropic's Finance plugin on the same question

Anthropic's free Finance plugin (version 1.3.0, about 1.8 million installs: month-end close, reconciliation, financial statements, variance analysis) was added in claude.ai, and the August question asked in Cowork with the same five exports, this plugin turned off; one run each, graded as above:

| Runs with | Lines right | Missed |
|---|---|---|
| the Finance plugin installed, the question alone | 4 of 11 | Gross charges, Net volume, Sales tax collected, Stripe fees, Paid out to the bank, Stripe balance at month end, Held in reserve at month end |
| Finance's /reconciliation, the question alone | 4 of 11 | Gross charges, Net volume, Sales tax collected, Stripe fees, Paid out to the bank, Stripe balance at month end, Held in reserve at month end |
| Finance's /reconciliation, the question and the definitions file | 10 of 11 | Sales tax collected |

Plain Opus without any plugin gave 4 of 11 in August with the question alone and 10 with the definitions file. The Finance plugin gave the same: asked plainly, no skill of it was used; called by its command, its reconciliation skill read the month in the account's local time and a payout by its arrival, as plain Opus does (its answer even gave the answer key's gross charges "on a UTC cut" and kept the other); with the owner's definitions attached it gave the owner's lines but sales tax, which every arm misses by cents. The plugin is written for a ledger (journal entries, a general ledger against a subledger, SOX testing), and on a Stripe month-end it neither helped nor hurt. What moved the figures was, again, the definitions written down. The answers are in `results/finance-f-answers/` (copied from the page as text).

**Files:** `stores/stripe_f/` (the five exports, the answer key and the generator's notes); `results/pinned-f-runs.json` and `results/pinned-f-answers/` (every run's grades, turns, cost and final answer).


## The Amazon seller account (G)

A third separate Claude session, which never saw the skills, built an Amazon seller account for testing month-end tools: a small US kitchen brand, mostly FBA, 60 SKUs, 9,130 orders from July to September 2026. It wrote the reports Seller Central gives: eight settlement reports (tab-separated, periods that cross month ends, a failed deposit, a negative settlement carried forward, a reserve), the monthly Date Range reports, the All Orders report (Windows-1252), and the bank's list of deposits, with an answer key from its own events. The data and the answer key are in `stores/amazon_g/`.

The owner's question each month: what did we sell, what did Amazon keep, what reached the bank and what does Amazon still owe us, ending with 10 lines for the bookkeeper. As in case F, some runs got the owner's definitions in words (the answer key's own) and some the question alone.

### Pinning July

The first setup session ran out of its 30 minutes: pin.py broke a copy of each of the 13 files seven ways and ran the whole calculation each time. pin.py now breaks one file of each kind (the largest). The same session also found that a pin wanted the very files it was pinned on, where a month brings as many settlement reports as it has; pin.py now treats files of one shape as one kind. A second session, given the first one's draft, pinned July in 19 turns (427 s, $0.97), with July's 10 lines all right:

- pin `ee1f712540ac`: 661 lines of Python over 13 files;
- the payments v1 definitions pack: 26 definitions decided, 14 from the owner's words, 6 as Claude's readings and 6 not applicable with the reason; 21 traps bound to checks or marked not applicable. The session noted that the pack is written for payment providers, so some of its wording reads oddly for Amazon: a marketplace pack was written after these runs, and has not run;
- broken copies: 19 caught, 3 no effect.

### The months

| Month | Runs with | Runs | Lines right | Lines alike in every run | Missed | Turns | Time | Cost | The plugin's own check passed |
|---|---|---|---|---|---|---|---|---|---|
| 2026-07 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 9–11 | 101–114 s | $0.49–$0.64 |  |
| 2026-07 | the pin, definitions in the prompt (the setup) | 1 | 10 of 10 | 10 of 10 | none | 19 | 427 s | $0.97 |  |
| 2026-08 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 10–13 | 113–148 s | $0.59–$0.79 |  |
| 2026-08 | the pin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 6–8 | 48–92 s | $0.39–$0.47 |  |
| 2026-08 | no plugin, the question alone | 3 | 6, 6, 7 of 10 | 9 of 10 | Net product sales, Orders, Owed by Amazon at month end, Refunds | 8–14 | 120–148 s | $0.51–$0.66 |  |
| 2026-08 | no plugin, the question and a definitions file | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 9–13 | 102–137 s | $0.51–$0.60 |  |
| 2026-08 | the pin, the question alone | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 6–8 | 98–133 s | $0.49–$0.63 | 2 of 3 |
| 2026-08 | the pin, the question alone (0.11.1) | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 8–9 | 118–188 s | $0.51–$0.83 |  |
| 2026-08 | the pin, the question alone (0.11.0: its answer check checked nothing) | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 6–7 | 53–98 s | $0.37–$0.47 |  |
| 2026-09 | no plugin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 10–14 | 105–159 s | $0.64–$0.96 |  |
| 2026-09 | the pin, definitions in the prompt | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 6–7 | 60–88 s | $0.37–$0.46 |  |
| 2026-09 | no plugin, the question alone | 3 | 6, 7, 7 of 10 | 8 of 10 | Net product sales, Orders, Owed by Amazon at month end, Refunds | 10–11 | 127–140 s | $0.54–$0.71 |  |
| 2026-09 | no plugin, the question and a definitions file | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 13–16 | 126–133 s | $0.59–$0.77 |  |
| 2026-09 | the pin, the question alone | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 7–9 | 48–145 s | $0.37–$0.68 | 2 of 3 |
| 2026-09 | the pin, the question alone (0.11.1) | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 9–10 | 72–129 s | $0.43–$0.72 |  |
| 2026-09 | the pin, the question alone (0.11.0: its answer check checked nothing) | 3 | 10, 10, 10 of 10 | 10 of 10 | none | 7–8 | 43–80 s | $0.31–$0.46 |  |

Cost is what Claude Code reports per session at list prices.

Plugin versions: the pin with definitions ran 0.11.0, the pin with the question alone 0.11.6 (its 0.11.1 and 0.11.0 runs are kept and marked); the runs without the plugin ran none.

With the definitions in the prompt, plain Opus got every line right in every run (on Stripe it got 10 of 11), and so did the pin. With the question alone:

- **no plugin:** 6/7 of 10 lines in 2026-08 and 6/7 of 10 lines in 2026-09 match the owner's definitions, and its runs did not all agree with each other. Its readings, as its answers state them: net product sales without shipping, gift wrap and promotions; in some runs the reserve counted inside what Amazon owes; in most, orders counted by the month their sale posted rather than their purchase date. Four of its six answers also flagged something the answer key does not grade: the failed deposit was followed by payouts to a new bank account, and they asked the owner to confirm the account was theirs;
- **no plugin, the definitions in a file:** 10 of 10 in every run;
- **the pin:** 10 of 10 in every run.

Here too the step that matters is the definitions written down once. Over the file, the pin took 6–9 turns against 9–16, at $0.55 a month on average against $0.63: cheaper, after $0.97 for the second setup session (the first ran out of time and reports no cost). Its own check passed 4 of 6 answers on 0.11.6; the two it flagged had retold the checked answer shorter or typed a settlement's amount by hand. On 0.11.1 it passed 3 of 6: the others left out Claude's open questions or three warnings about order columns emptied in a short settlement, which 0.11.4 no longer gives (the columns are filled in the month's other settlements), and one had a settlement number read as an amount (fixed in 0.11.1).

### The same account, pinned again with the marketplace pack

On 0.11.6, with a marketplace pack now in the plugin, a new setup session pinned July in one session (30 turns, 1335 s, $2.59); it chose the marketplace v1 pack itself. 20 definitions decided, 18 from the owner's words and 2 as Claude's readings (what counts as an order; which report a figure comes from when two cover the same lines); all 18 traps bound to a check the calculation computes; broken copies: 21 caught, 2 no effect.

August and September, the question alone, three runs each: 10 of 10 lines in every run, 8–10 turns, $0.47–$0.80 a run. The plugin's own check passed 1 of 6: the others typed figures the calculation did not give (a bank account's last digits, the broken-copy lines retold, settlement amounts in prose) or left out the month's cancelled orders, which this pin names one by one where the first pin gave only their count. The figures were right; the answers around them were not the checked text.

**Files:** `stores/amazon_g/` (the reports, the bank list, the answer key and the generator's notes); `results/pinned-g-runs.json`, `results/pinned-g-mkt-runs.json` and the answers next to them (`results/pinned-g-answers/`, `results/pinned-g-mkt-answers/`): every run's grades, turns, cost and final answer.


## The SaaS business on Stripe Billing (H)

A fourth separate Claude session, which never saw the skills, built a Stripe Billing account for testing subscription-metrics tools: Brindlepost, Inc. (fictional), a US business selling a team tool by the seat, monthly and annual, in USD, EUR and GBP, with trials, coupons (once, repeating, forever, 100% off, a retention offer), prorations, seat changes, paused collection, dunning, Stripe Tax, eight enterprise customers invoiced by hand, credit notes, disputes and a failed payout: 2,338 customers, 2,335 subscriptions and the invoices of March to September 2026. It wrote sixteen exports as Stripe gives them and an answer key computed from its own events. The data and the answer key are in `stores/stripe_s/`.

The owner's question each month: MRR and how it moved, paying customers and those lost, what was billed and collected, what Stripe kept, what reached the bank, and the revenue recognised, ending with 12 lines. The owner's definitions, with their month-end exchange rates, are the answer key's own. Graded to the cent, as on F and G; a second column counts the lines within a dollar, because the answer key converts and rounds each invoice and each customer on its own, which the definitions do not say.

### Pinning July

One session on 0.11.6 pinned July (53 turns, 2441 s, $5.71), with two packs together: subscriptions v1 + payments v1, the subscriptions pack's first run. 51 definitions decided, 32 from the owner's words, 15 as Claude's readings (most of them payments-pack questions the owner's definitions do not touch, each an open question in every answer) and 4 not applicable; 39 of 41 traps bound to a check the calculation computes; 898 lines of Python over 17 files; broken copies: 74 caught, 14 no effect. July's pinned answer: 6 of 12 lines to the cent, 9 within a dollar.

Two things this setup got wrong, both answered in 0.11.7:

- the owner wrote that revenue is spread "evenly by the second"; the pack's option says "day by day", and the pin records the option's words as the owner's answer (its calculation does spread by the second). 0.11.7 records a rule the options do not say as the owner's own, in their words, checked against what any rule for that question must settle, and asks what it leaves open with options fitted to it;
- the owner's exchange rates were in their definitions, and the calculation reads them from a file the setup session wrote. In one month's run of six that file was not among the month's files: the run stopped and asked for it, and did not work the month out another way, as the skill says. 0.11.7 says such a figure is an argument, never a file only the setup wrote.

### The months

| Month | Runs with | Runs | Lines right | Within a dollar | Lines alike in every run | Missed | Turns | Time | Cost | The plugin's own check passed |
|---|---|---|---|---|---|---|---|---|---|---|
| 2026-07 | the pin, definitions in the prompt (the setup) | 1 | 6 of 12 | 9 of 12 | 12 of 12 | Billings, Churned MRR, Deferred revenue at month end, MRR at month end, Net new MRR, Revenue recognised | 53 | 2441 s | $5.71 |  |
| 2026-08 | no plugin, definitions in the prompt | 3 | 6, 6, 7 of 12 | 9, 7, 8 of 12 | 7 of 12 | Billings, Deferred revenue at month end, MRR at month end, Net new MRR, Paying customers at month end, Revenue recognised | 29–45 | 691–1139 s | $2.45–$3.41 |  |
| 2026-08 | no plugin, the question alone | 3 | 2, 2, 2 of 12 | 2, 2, 2 of 12 | 3 of 12 | Billings, Cash collected, Churned MRR, Customers lost, Deferred revenue at month end, MRR at month end, Net new MRR, Paying customers at month end, Refunds, Revenue recognised, Stripe fees | 18–32 | 288–544 s | $1.18–$2.12 |  |
| 2026-08 | no plugin, the question and a definitions file | 3 | 5, 5, 6 of 12 | 6, 6, 7 of 12 | 6 of 12 | Billings, Deferred revenue at month end, MRR at month end, Net new MRR, Paying customers at month end, Refunds, Revenue recognised | 22–34 | 476–883 s | $2.03–$2.50 |  |
| 2026-08 | the pin, the question alone | 3 | 7, 7, 7 of 12 | 8, 8, 8 of 12 | 12 of 12 | Billings, Deferred revenue at month end, MRR at month end, Net new MRR, Revenue recognised | 12–16 | 117–141 s | $0.73–$0.79 | 1 of 3 |
| 2026-09 | no plugin, definitions in the prompt | 3 | 5, 6, 5 of 12 | 6, 7, 6 of 12 | 8 of 12 | Billings, Churned MRR, Customers lost, Deferred revenue at month end, MRR at month end, Net new MRR, Revenue recognised | 27–55 | 597–1332 s | $2.88–$4.60 |  |
| 2026-09 | no plugin, the question alone | 3 | 4, 4, 3 of 12 | 4, 4, 3 of 12 | 3 of 12 | Billings, Churned MRR, Customers lost, Deferred revenue at month end, MRR at month end, Net new MRR, Paying customers at month end, Revenue recognised, Stripe fees | 27–32 | 414–569 s | $2.02–$2.44 |  |
| 2026-09 | no plugin, the question and a definitions file | 3 | 5, 5, 6 of 12 | 6, 6, 9 of 12 | 6 of 12 | Billings, Churned MRR, Customers lost, Deferred revenue at month end, MRR at month end, Net new MRR, Revenue recognised | 31–42 | 488–862 s | $2.27–$3.60 |  |
| 2026-09 | the pin, the question alone | 3 | 7, stopped, 7 of 12 | 8, stopped, 8 of 12 | 12 of 12 | Billings, Deferred revenue at month end, MRR at month end, Net new MRR, Revenue recognised | 7–14 | 48–199 s | $0.36–$1.05 | 2 of 3 |

Cost is what Claude Code reports per session at list prices. The pin ran 0.11.6; the runs without the plugin ran none.

- **The question alone, no plugin:** 2/3/4 of 12 lines, on its own readings, which its answers state and which differ from run to run: the exchange rates of Stripe's charges, the month's average or its last day; in some runs the enterprise contracts invoiced by hand counted in MRR, which the owner leaves out (MRR above the owner's by $16,054.64 to $28,884.97); in August an invoice of $18,000.00 paid outside Stripe counted as cash, and flagged to check against the bank. One run noted that some seat changes could not be dated from the exports.
- **With the definitions, no plugin** (in the prompt or in a file): 5/6/7 and 5/6 of 12. Cash, fees and payouts come right in every run (in two August runs with the file, refunds net off a refund that failed and came back, which the definitions show apart). The subscriptions do not: the export gives each subscription's status on the day it was taken, and five of the six August runs took it for the month end, so the 16 subscriptions unpaid at the end of August counted as paying (1,403 to 1,408 paying customers against 1,387), and in four of the six September runs as lost (58 customers lost against 42). One August run, with the definitions in the prompt, rebuilt the month-end state and came out with the pin's figures.
- **The pin:** 7 of 12 lines in every run that answered (5 of 6), the same figures in every run, paying customers and customers lost right: the subscriptions pack asks how the month-end state is found, and the pin rebuilds it from the dates and the invoices. 7–16 turns against 22–42 with the file, $0.73 a month against $2.53, after $5.71 for the setup (it pays for itself in about 3 months).

What no run reaches from these exports is MRR to the cent, and with it net new MRR. The pin is above the answer key by $216.42 in August and $123.87 in September. A separate session compared the pin with the generator customer by customer for July and August: the answer key lowers a subscription's seats, and starts a retention coupon, at the moment the change took effect, and no export records that moment (a seat decrease without proration makes no invoice line; the coupon shows only on the next invoice). That is eight customers in July and five in August; September was not traced this way. It also found one fault of the pin's own code, which drops a coupon still running at the end of June (read from the invoice that billed the latest line, where it had just lapsed). The lines a few cents off (billings, churned MRR, deferred revenue) are the answer key's rounding of each converted invoice and customer; revenue recognised differs by one to four dollars, in the runs without the plugin too.

The plugin's own check passed 3 of 6 answers. The 3 it flagged each left out some of the 16 open questions this pin carries in every answer; one also typed the owner's exchange rates, which were in no computed result (0.11.7 counts the figures of the owner's definitions as theirs). One it passed is the run that stopped: its answer gives no figure, so there was nothing to check.

### Pinned again on 0.11.7

The same owner and the same words, a new setup session on 0.11.7, which records a rule the pack's options do not say as the owner's own and takes a figure the owner gives in words as an argument (47 turns, 1751 s, $6.13):

- 53 definitions decided, 35 from the owner's words; 7 of those are the owner's own rules in their words, where no option said them (revenue spread "evenly by the second", a proration over its own period caught up when invoiced, a credit note as a negative revenue line, seats at the last second of the month, the currencies, test rows), with the points each leaves open asked or kept as open questions; 13 Claude's readings; 16 open questions in every answer;
- the owner's month-end rates are arguments of the calculation (`--rate 2026-06:EUR=1.180562` and so on), not a file only the setup had;
- broken copies: 76 caught, 8 no effect, 1 NOT caught (the last three days of every month missing (credit_notes.csv): figures change and nothing warns; the answers say so).

July's pinned answer: 5 of 12 lines to the cent, 7 within a dollar. Where the owner's words allow two readings, this setup took the other one: "a month is the calendar month in New York time" and "payouts whose arrival date is in the month" let a payout's arrival be read in New York time, so one stamped at midnight UTC on the 1st arrived the evening before, and this pin counts it in the month before ($218,954.63 for July against the answer key's $231,154.90, which reads the arrival date as a date, as the first setup did). The pinned answer says so under "How this was counted". It also counts one paying customer more at each month end than the answer key (not traced). A setup is a new session: the pin holds what that session decided, and the owner sees it in the answer.

| Month | Runs with | Runs | Lines right | Within a dollar | Lines alike in every run | Missed | Turns | Time | Cost | The plugin's own check passed |
|---|---|---|---|---|---|---|---|---|---|---|
| 2026-07 | the pin, definitions in the prompt (the setup) | 1 | 5 of 12 | 7 of 12 | 12 of 12 | Billings, Deferred revenue at month end, MRR at month end, Net new MRR, Paid out to the bank, Paying customers at month end, Revenue recognised | 47 | 1751 s | $6.13 |  |
| 2026-08 | the pin, the question alone | 3 | 6, 6, 6 of 12 | 7, 7, 7 of 12 | 12 of 12 | Billings, Deferred revenue at month end, MRR at month end, Net new MRR, Paying customers at month end, Revenue recognised | 13–16 | 112–125 s | $0.54–$0.80 | 0 of 3 |
| 2026-09 | the pin, the question alone | 3 | 4, 4, 4 of 12 | 5, 5, 5 of 12 | 12 of 12 | Billings, Churned MRR, Customers lost, Deferred revenue at month end, MRR at month end, Net new MRR, Paid out to the bank, Revenue recognised | 14 | 98–105 s | $0.52–$0.71 | 0 of 3 |

August and September, the question alone: 6 of 12 lines in 2026-08 and 4 of 12 lines in 2026-09 in every run (6 of 6 answered), 13–16 turns, $0.52–$0.80 a run, the same figures in every run. No run stopped: each took the month's rates from the pinned definitions as arguments. The payout line follows this pin's reading: right in August, over in September by a payout that arrived at midnight UTC on October 1. The plugin's own check passed 0 of 6: this pin names 210 to 370 records for the owner in each answer (every new customer, every free subscription, every voided invoice); the answers gave the long lists by their count and kept every id in the saved answer, as the skill says for long lists, and the check wants each id named in the chat. That conflict is the plugin's own, to settle in its next version.

What 0.11.7 changed here: the owner's rules the pack does not offer are recorded in their words, and the rates no longer need a file. What it did not change: a setup session still reads what the owner's words leave open, and a second setup read two things differently from the first. The pin makes a month repeat exactly; it does not make the first reading right. That is what the open questions in every answer are for.

The grader read a count written without a thousands separator ("1226") by its first three digits; it was fixed before these runs were graded, and no earlier grade on this page changed.

**Files:** `stores/stripe_s/` (the sixteen exports, the answer key and the generator's notes); `results/pinned-h-runs.json` and `results/pinned-h-answers/` (the first pin), `results/pinned-h-0117-runs.json` and `results/pinned-h-0117-answers/` (0.11.7): every run's grades, turns, cost and final answer.
