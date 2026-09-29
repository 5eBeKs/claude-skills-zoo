# Numbers Claude gives about your business, with the work shown

*Claude skills for the numbers a business asks every month, from Shopify, Stripe, Amazon or another export,
and for checking the report someone else sends you. Tested on stores and accounts built apart from the skills;
every answer the tables count is published with its grades. Version 1.4, September 2026.*

I set up Claude to answer a recurring numbers question the way the business counts: its definitions asked
once and written down; the calculation pinned; every figure from a script and checked against its results,
an answer that does not match sent back or flagged; anything left out named. I also check the skills and
plugins you already use.

**Tested on eight synthetic datasets: five Shopify stores, a Stripe account, an Amazon seller account, and an
agency's report on the Stripe account. Five of them were built by separate Claude sessions that never saw the
skills.**

- **The step that matters: your definitions, written down once.** On a Stripe account and an Amazon seller
  account built apart, the owner's month-end question asked plainly: Opus matched the owner's own definitions
  on 3 or 4 of 11 bookkeeper lines (Stripe) and 6 or 7 of 10 (Amazon), on its own readings (the month in local
  time, payouts by the day they reached the bank, the reserve inside what is owed). With the definitions
  written once, in a file or in a pinned calculation, the same plain question gave 10 of 11 and 10 of 10 in
  every run. What the pin adds over a file: the same figure in every run where a file's runs differed by
  cents, fewer turns, the plugin's own check on every answer (it passed 7 of 12 and flagged the others,
  mostly for leaving out the open questions about Claude's readings), and a refusal to pin a month on
  incomplete exports until the owner decides. [CASE-F.md](CASE-F.md), [CASE-G.md](CASE-G.md)
- **Checking the report you already get: no better than plain Opus yet.** An agency's August report on the
  Stripe account, with 7 mistakes planted by a separate session: with the skill 6, 6, 6 of 7 caught in three runs and 2, 2, 0 right figures called wrong; plain Opus 6, 6, 6 of 7 and 2, 2, 2 (both sides' "wrong" ones are subscription counts read another way). The skill gave as many right verdicts
  at about twice the turns, and its own check flagged every answer: the closing lines the owner asks for
  retyped figures in every run, one run also typed a figure in its prose, and in one the result was not where
  the check looked. Version 0.11.2 renders the closing lines in the report's own form and sends back any other;
  it has not been run on the report.
  No side caught two swapped digits in MRR. [CASE-F.md](CASE-F.md#the-same-account-checking-the-agencys-report)
- **A second Shopify store, blind, and the skills did not win.** A separate session built a Dutch store in EUR
  with VAT inside its prices (21,241 orders, 65 traps). The Shopify skills were not changed for it. On the
  five graders any right answer passes, plain Opus passed 9 of 9 answers and the skills 6 of 9: the three misses
  are gift cards sold, where their script is short (40 of 55 of the store's figures matched the scripts, which
  also cannot cost renamed products). On graders that ask for more (the money in transit as one total, test orders by number) the skills
  did better. Both counts and every answer: [STORE-E.md](STORE-E.md)
- **A Shopify store built apart, used to develop.** A 30,251-order store: the scripts' blind run matched 18 of
  50 of its figures, 55 of 56 after fixing what it found on the same store; on three owner questions 4 of 9
  answers at the first graded version and 7 of 9 after, against 0 of 9 without. [STORE-D.md](STORE-D.md)
- **The plugin as a client installs it.** Version 0.11.0 on the first three stores with the plugin's own tool
  server running: 27 of 27 answers passed their pattern graders (the graders a reader judges are marked as not
  scored), every one went through the scripts and the answer check rather than the tool server,
  and the check passed all 27 at the end. [The answers](results/installed-0110-answers/)
- **Works where the owner is.** The Shopify skills run in claude.ai chat, uploaded as skills: tried there with
  Opus 5.5 on store A ([the three answers](live-tests/claude-ai/)); the pinned calculation not yet. Each
  answer ends with a seal line: `answer.py --verify` on the saved file shows it was not edited after the check,
  not that the figures are right. Team accounts: documented by Anthropic, not tried here.

![The owner's definitions, written down once](gallery/01-definitions-written-once.png)

**Fixed-price work, quoted per export:** your definitions written down and one recurring question pinned on
your export (Stripe, Amazon or another export, quoted first; for Shopify, the Shopify skills with your
definitions file), a check of the report your bookkeeper or agency
sends you, or a check of skills that misfire. [Message me on Upwork](https://www.upwork.com/freelancers/ilyashkura)
with the question you ask Claude and a sample export (test data is fine).

![What the owner can see](gallery/03-what-the-owner-can-see.png)

The comparison, 27 runs with the skills and 27 without, every answer kept in
[`results/evals/answers/`](results/evals/answers/). My tests and my graders: every answer is here to
re-grade.

| | with the skills | without |
|---|---|---|
| The skill's "How this was counted" section under the answer: each definition in words, marked as the owner's answer or the usual one | 25/27 | 0/27 |
| On the skill's stated basis: the figure the skill gives on its stated definitions (the usual answers on stores A and B, the owner's on store C) | 27/27 | 13/27 |
| Everything the owner should see, named (orders left out, disputed, not paid out) | 27/27 | 21/27 |
| Says it added the figures up by hand | 0/27 | 9/27 |
| Passed every grader (the figures on the summary and payout questions; on margins, the products that must be named) | 27/27 | 26/27 |

Where the graders check figures (the summary and payout questions), the arithmetic is right either way,
but for one plain answer; the margins graders check which products are named, not the margin. What
changes is what was counted and whether the answer says so. Without the skills Opus often says what it
left out and on what basis, in its own words; several plain answers have a section of their own on how
they counted, which the first row does not count, because it looks for the skill's heading. Which basis
differs from question to question and from store to store (the second row). On store C, where the
owner's definitions were in a file, the three plain runs of each question kept one basis. On its summary
and payout questions the second row still counts one plain run each as off it: one is an error (see "Own
code slips" below), the other gives the revenue on the owner's definitions only as "roughly £85k". Plain
Claude's 9 "by hand"
answers are on stores A and B, where it had no shell.

The same 27 questions on 0.6.0, with the answer hook (and the plugin's tool server off, so the skills ran
their scripts): right by the graders, on the stated basis and everything named in 27 of 27, the
definitions and the files' fingerprints under every answer. The hook sent 7 first
answers back: 4 had left the owner's open questions out, 1 gave wrong counts (86 orders left out where
the results have 85), 1 showed sums the model had added itself; the seventh was the check's own
mistake, a list of days read as figures, fixed in 0.6.1. Every final answer passed. Each stop is read in
[ZOO.md](ZOO.md#the-later-versions-answer-hook-included).
On 0.10.1 the same 27 questions with the skills, answer hook included, pass their pattern graders 27 of
27 on the chat alone (the checks a reader judges were not read, and these 27 answers are kept with the
private runs, not here). The claim map (each figure under its own words and sign) is in that version, but
in most of those runs it was saved where the answer hook does not look, so the hook applied only the
number check. A review in a fresh Claude session found this; 0.11.0 saves it where the hook looks.

## What you can order

| You have | You get | Evidence here |
|---|---|---|
| A task your team does with Claude every week or month: numbers from an export, a report, a reconciliation | Skills that ask your definitions once, in plain words, and print them under every answer; figures from scripts, checked against the scripts' results; every excluded record named. A plugin for Claude Code (tested here; the 27 runs of the version as installed had its tool server on, and never called it); the Shopify skills in claude.ai chat (tried; the pinned calculation and the tie-out not yet); for a whole team's account and in Cowork (documented by Anthropic, not tried yet) | [What the owner can see](#what-the-owner-can-see) |
| Skills you already have that sometimes do not fire, or fire on the wrong request | Your skills through the skill zoo: `claude plugin validate`, a linter for silent mistakes, and a routing eval on how your people actually ask | [The skill zoo](#the-skill-zoo-does-the-right-skill-run) |
| Answers Claude writes from your data that nobody checks | Your answers with defects planted one at a time, and a record of which layer stops each: the number check, the coverage check, a reviewer model | [The answer zoo](#the-answer-zoo-it-ran-and-the-answer-is-wrong) |

Every model answer and grade is kept and handed over. Contact: [Upwork](https://www.upwork.com/freelancers/ilyashkura).

## What was built

| Skill | The owner's question | What computes it |
|---|---|---|
| `shopify-monthly-summary` | How did the month go? The numbers for my accountant | a script over the orders export |
| `payout-reconciliation` | Why did less reach the bank than we sold? | a script over the orders and the payout transactions: a bridge from card sales to the bank statement that must close to 0.00 |
| `sku-margin-check` | Which products lose money? | a script over the orders and the cost sheet |
| `pinned-calculation` | The same question every month on another system's exports (Stripe, Amazon, a bank), counted my way | the owner's definitions asked once (packs of questions for payment providers and marketplaces), then a calculation, its answer template and its checks pinned in one file the owner keeps, tried on broken copies of the owner's files |
| `report-tie-out` | Are the figures in the report my bookkeeper or agency sent right? | every figure of the report quoted and given a status against a figure computed from the owner's files: matches, does not match, or cannot be confirmed and why |

Around them:

- **Definitions, asked once and shown every time.** A short questionnaire (test orders, when a sale
  counts, VAT, shipping, refunds), answered by the owner in a file a person can read. Every answer
  ends with "How this was counted": each definition in words, marked as the owner's answer or as
  the usual one still to be confirmed, and the files it was computed from (rows and SHA-256) with the
  plugin's version. See [`examples/answer-correct.md`](examples/answer-correct.md). The comparison
  below was made on earlier versions (`22b4986` for stores A and B, `0a61aaa` for store C), before
  the fingerprints and the export check; the same questions on 0.6.0 show both in every answer.
- **Figures from placeholders.** The model writes a draft with placeholders (`{{net_after_refunds|money}}`);
  a renderer fills them from the script's results, lists included, however long. A model can still type a
  figure into its chat answer; the claim map flags it when the hook finds the map (on store D at 0.10.1,
  two answers typed figures and were flagged).
- **The number check.** Every figure in the answer traces to the script's results, every order
  number exists, the currency is the store's.
- **The coverage check.** Everything the results list for the owner is named in the answer: orders
  left out and why, disputes, orders paid outside Shopify Payments, payouts in transit, products
  below cost or without a cost, open questions.
- **The export checked first.** A renamed column stops the script; a new gateway, tag, status or
  currency is named, and orders that are not sales yet are left out with the reason; the answer says
  whether the export covers the month and what it was checked against
  ([The data zoo](#the-data-zoo-the-export-changes)).
- **An answer hook.** An answer that is not the checked text is sent back once; if it fails again,
  the reader is warned. Up to 0.10.1 that warning went wrong in an interactive session; fixed in 0.11.0
  (see [The answer hook](#the-answer-hook)).
- **A tool server** (MCP) with the same scripts, for a place that loads the plugin but has no terminal,
  such as Cowork (not tried yet; the desktop app's Chat tab ignores plugin tool servers). The `claude -p`
  runs here had it off, so the skills ran their scripts; the first comparison's runs on stores A and B
  allowed it, and which path they took was not recorded; the 27 runs of 0.11.0 as installed had it on, with a
  shell, and never called it. And **a linter** for the mistakes that make a
  skill fail without a word.

## How the bench works

Four parts; the full method is in [METHOD.md](METHOD.md), every table in [ZOO.md](ZOO.md).

| Part | What is planted | What is measured |
|---|---|---|
| **Stores** | Three synthetic stores with the traps of real exports, store C at a real store's size; stores D and E, a Stripe account (F) with an agency's report on it, and an Amazon seller account (G), each built by a separate Claude session that never saw the skills | the scripts against truth computed by each generator from its own records |
| **Models** | The owner's questions on stores A to C, and three more on store D | Opus 5.5 with the skills and without them: the figures, and what the owner can see |
| **Answer zoo** | 24 defects in 7 classes, one per copy of a correct answer | the number check, the coverage check, reviewer models |
| **Skill zoo** | 11 defects in a skill's frontmatter or files, one per copy of the plugin | `claude plugin validate --strict`, the linter, the routing eval |

- **Store A**, an EU tea shop: VAT inside prices, a test order tagged `test`, a PayPal order, a chargeback.
- **Store B**, a US candle shop built to differ: sales tax on top, test orders through Shopify's
  test gateway with no tag, a gift card split, a dispute won, a payout adjustment, a cost sheet
  typed by hand, the previous month's last sales paid out in this one.
- **Store D**, a US clothing store built by a separate Claude session that never saw the skills: four
  currencies, 30,251 orders, 68 traps, its own truth. See [STORE-D.md](STORE-D.md).
- **Store E**, a Dutch home goods store, **account F** (Stripe) with **an agency's report** on it, and
  **account G** (Amazon): each built apart; see [STORE-E.md](STORE-E.md), [CASE-F.md](CASE-F.md) and
  [CASE-G.md](CASE-G.md).
- **Store C**, a UK skincare shop at a real store's size: three months, 4,470 orders, and the
  question is one month. Its owner has answered the definitions: a sale counts once it is shipped,
  revenue is reported without VAT and shipping. So 70 pre-orders, paid and charged, are not
  August sales. Without the skills the model has a shell there and writes its own code.

Not every trap has a grader of its own: VAT inside store A's prices, store B's sales tax and payout
adjustment, and on store C the refunds of July orders, the gift cards and PayPal orders and the cost
sheet's spellings are graded by nothing.

## What the owner can see

The model is not the problem. On the summary and payout questions, where the graders check figures,
Opus 5.5 got them right in 35 of 36 runs, with the skills or without them (on margins the graders check
which products are named, not the margin). What changes without the skills is what the owner is shown,
and whether it is the same next month:

- **The basis moves.** For the same margins question Opus led with a loss per unit on store A (€1.64,
  and a month's loss "of about €34" on another basis), the month's loss on store B, and a loss after
  spreading discounts and refunds over products on store C. Each is
  defensible; none is fixed or written down, so next month's answer can differ. For the payouts it
  started, in all six runs on stores A and B, from every order placed in August (€3,022.62 and
  $4,335.23), test and cancelled ones included, and explained them away below. With the skills, every answer is on the stated basis (27 of 27).
- **The orders behind the counts go unnamed.** Store C leaves 85 orders out of August's sales and has
  400 payout items to account for. Without the skills Opus named them in none of the six summary and
  payout runs; with them every answer named all of them, in the chat or in the checked file it saved.
- **Own code slips.** Without the skills on store C the model wrote its own code, read the owner's
  definitions file and applied it. In one run of three it labelled a total as after discounts when it
  was before them, and August revenue came out about £1,000 high. The skills' scripts gave the same
  figures in every run.
- **Hand-added figures.** Where it had no shell (stores A and B, like a chat with the file attached)
  Opus said in 9 of 18 answers that it had added the figures up by hand. Most of these say they checked
  the totals another way; one suggests comparing them with Shopify's own report before sending.

Per store, passed every grader with / without the skills: 9/9 and 9/9 (A), 9/9 and 9/9 (B), 9/9 and 8/9 (C);
everything named 9/9 and 9/9 (A), 9/9 and 9/9 (B), 9/9 and 3/9 (C). The full tables are in
[ZOO.md](ZOO.md).

## The answer zoo: it ran, and the answer is wrong

24 defects planted one at a time into correct answers, in seven classes named for what the owner
would get wrong. The number check stops 6, the coverage check 5, and the other 13 go to a reviewer
model, three runs each in a fresh session:

| Layer | Stops |
|---|---|
| Number check (every figure traces to the results) | 6 |
| Coverage check (everything listed for the owner is named) | 5 |
| Sonnet 5 as a reviewer | 13 of the other 13 |
| Opus 5.5 as a reviewer | 13 of the other 13 |
| Nothing | 0 |

On the three untouched answers Sonnet raised no objection in 9 runs; Opus objected in 3 of 9, each time
to something the answer left unsaid or put loosely (whether unshipped orders count; how much VAT the net
still holds). I agree with each. The answers the zoo tests were not changed after this run, so these
objections still stand against them. Earlier reviewer runs, on reference answers since corrected, are
not in the table ([Checking the checks](#checking-the-checks), item 4).

## The skill zoo: does the right skill run

11 defects in the summary skill's frontmatter or files, each in its own copy of the plugin. On this
plugin, routing held up: a vague description, one with no trigger, one that also claims margins, a
wrong name — the summary skill still fired on its question, asked plainly and indirectly (6 of 6), and
stayed out of the margins question. Three defects stop it cold (0 of 6): a misspelled `description`
field, a line before the frontmatter, and `disable-model-invocation: true`. `claude plugin validate`
flags the first two; the third it passes, and so did the linter until the bench showed it (W06).

## The answer hook

The skills say "show the owner exactly the checked text". On store C a model once showed a retelling
instead. A Stop hook in the plugin now holds the rule: when the month-end scripts ran in a turn, the
final message must pass the number check against their results, and anything it leaves out must be in
a checked file it points to; otherwise Claude is sent back once with the list, and if the second answer
fails too, the reader is warned. In live sessions where the owner asked for two sentences and no files,
the hook sent Claude back: once Claude told the owner what the short answer leaves out and offered the
checked version, once it named all 85 orders left out. An answer made to fail twice ended with the
warning, on version 0.4.0 ([`results/hook-check.md`](results/hook-check.md)).

From 0.6.0 the hook checks only the current turn, and up to 0.10.1 it takes its own feedback, which
Claude Code records as a message from the user, for the start of a new turn. So in a session that keeps
a transcript, as an interactive one does, a second failed answer gets the warning that no month-end
script ran, not the one above, and the failed answer is not kept. Fixed in 0.11.0: a turn starts at the
person's own message. The bench's
own runs with the hook kept no transcript and never met this: on 0.5.1, 0.5.2 and 0.6.0 (the nine
questions, three runs each) the hook sent back 5, 4 and 7 first answers of 27, none twice, and every
last answer passed.

## The data zoo: the export changes

A monthly skill breaks in the month the export changes. Eight changes to an export the owner had
confirmed, each run through the scripts before and after the export checks:

| Change | Before | Now |
|---|---|---|
| Two orders paid with a gateway the store never used | silent | named |
| An order tagged 'wholesale' | silent | named |
| An order whose payment is still pending | silent, counted as a sale | named, left out |
| An order with a status the store never had | silent, counted as a sale | named, left out |
| An order in US dollars in a euro store | silent, added to the euro total | named, left out |
| The 'Lineitem price' column renamed | crashed | stopped: "the export has 'Lineitem unit price': renamed?" |
| The export taken on the 20th | silent: a month at half its sales | named: "the export may stop early" |
| A 'reserve' line in the payouts | named | named |

The answer now also says on how many days of the month there are records, and what it was checked
against: the owner's figures from Shopify or the bank, or nothing. Up to 0.10.1 a month with no records
at all gave zeros with no warning, only that line ("records on 0 of 30 days"); from 0.11.0 it is a warning,
and so is a gap inside the month.

## Three stores against independent truth

Each store's generator computes `truth.json` from its own order records, not from the CSV the scripts
read. Now: store A 26 of 26 figures, store B 33 of 33, store C 47 of 47; three more figures in the
truth files (store B's lost and won dispute apart, store C's revenue after product refunds only) are
not reported by the scripts on their own. The skills of earlier commits,
measured against the same truth, show what the bench found: at `ad8b48e` store B got 9 of 21 and store
C 18 of 41; at `b445df1` both ended the payout bridge short of the bank.

## Checking the checks

A bench that only confirms its author proves little. After each model run every failure was read,
and so were the answers the skills got right, except at 0.10.1, where the checks a reader judges were
not read. Each finding changed the tools, not the story:

1. **Graders that failed right answers, twice.** The first patterns failed right answers written
   without the skills (a margin per unit instead of for the month; a payout bridge from every order
   instead of card sales). They became model judges; on the next run the payout judge failed right
   bridges too, so the payout cases went back to patterns that accept every right way to split the
   bridge, tried on the kept answers before the re-run. A test checks that every figure a grader
   looks for appears in the scripts' results or is recounted from the CSV files; it checks that the
   figure is there, not that it is the right one for its grader.
2. **A definition shared by the skill, the truth and the graders.** Store B's truth is computed
   independently of the scripts, but on the same definition: money paid out for this month's
   sales. Opus 5.5 without the skills reconciled to what the bank statement shows, which also holds
   the previous month's last sales, paid out in the first days of this one. It was right; the
   skill's "paid out this month" would not have matched the owner's bank. Independent arithmetic
   is not independent definitions. The bridge now ends at the bank
   ([`results/stores-at-b445df1.json`](results/stores-at-b445df1.json): the old skill against the corrected truth).
3. **A question that said less than the script did.** The questionnaire asked about orders "tagged
   'test'"; the scripts also left out orders paid through Shopify's test gateway. Opus with a shell,
   given store C's answered definitions and no skills, kept four test-gateway orders in the sales
   and asked the owner about them. By the words of the definition it was right. The question now
   names the gateway, and every definition is printed in words under the answer.
4. **Reviewers that were right about the reference answers.** On the first reviewer run, one run per
   answer, Opus 5.5 and Fable 5.1 failed all three untouched answers (the summary: "left after refunds"
   reads as money kept; VAT, shipping and the month basis missing), and Sonnet 5 passed one defect,
   advice to drop a product on one month's data. On the second, Sonnet failed the untouched payout and
   margin answers in 3 of 6 runs (their figures rest on answers the owner has not confirmed, and the
   question reads as cut off from them) and passed that defect in 2 of 3. I agreed, and the reference
   answers and the skills' instructions changed before the final run, the one the table counts. There
   Opus again objected, in 3 of 9 runs, to what the untouched answers leave unsaid or put loosely; I
   agree, and those answers were not changed after it.
5. **A defect nothing static saw.** `disable-model-invocation: true` passes `claude plugin
   validate` and passed the linter, and the skill stopped firing. The linter now warns on it.
6. **Size.** Store C leaves out 85 orders in August; a placeholder names one figure, so lists now
   render whole. The scripts rounded money half to even and one of store C's figures differed from
   its truth by a penny; they now round half up. And a grader that asked for revenue to the penny
   failed right answers that took VAT out of the month's sum instead of order by order (about a pound
   over 1,555 orders); it now accepts two pounds either way.
7. **Right figures under wrong labels, found by a separate audit.** A separate Claude session audited this
   repository's data, recounting from the CSV files, and found what no check here reads: labels.
   Store C's payout answers with the skills called 2,762.41 "refunds on August orders" when 1,093.51
   of it was refunds on July orders processed in August, and one set the gap against the wrong line.
   One such answer is run 1 of store C's payouts question in the comparison above, counted there as
   right and on basis: its graders check the figures, not the words next to them.
   The number check traces figures, not the words next to them. The script now splits refunds by the
   month of the order, and the skill gives the model each line's label word for word. The same audit
   found the number check refusing the skill's own words ("Mineral SPF 50", "VAT at 20%"), which a
   live session got past by hiding product names; that is fixed in 0.5.1. And it found this
   repository's own readings wrong in places, corrected here: a range of orders ("#1998–#2000")
   counted as not naming the middle one.

This is also the answer to "how would you test a system you did not design": plant what the owner
could get wrong, read every failure and every pass, and let what you find change the checks.

## What is in this repository

| Path | What it holds |
|---|---|
| [`ZOO.md`](ZOO.md) | Every table, generated from the results, not edited by hand |
| [`METHOD.md`](METHOD.md) | How each part works, what is published, what the bench is not |
| [`results/`](results/) | The recorded results the pages count: store comparisons, the answer zoo, the skill zoo, the model runs with their grades. Not published: the runs of 0.9.0 and 0.10.1 on stores A to C, two repeat runs of the store C comparison with the same setup (30 sessions), and the earlier reviewer runs |
| [`results/evals/answers/`](results/evals/answers/) | The final answer of every model run the tables count, with the skills and without, next to its grades |
| [`live-tests/`](live-tests/) | The first live tests (Haiku, Sonnet, Opus): 16 answers, unedited, and the figures they were checked against; and the three answers from claude.ai chat (`live-tests/claude-ai/`) |
| [`stores/`](stores/) | Eight datasets: stores A to E, the Stripe account F and the agency's report on it, the Amazon account G. Their exports, store C's definitions and every answer key (`truth.json`; the report's `key.json`): recount any figure from the files. Store C also has its August books, used by the [small business case](https://github.com/5eBeKs/small-business-audit), not by the comparisons here: QuickBooks Online's transaction list and profit and loss (`qbo_*.csv`), Shopify's list of the month's 21 payouts (`shopify_payouts_aug.csv`), and what a close of those books must find (`ledger_truth.json`) |
| [`examples/`](examples/) | A correct answer with its definitions in words, a plausible wrong one, and what the linter and the number check say |
| [`gallery/`](gallery/) | The case in pictures and a PDF: the definitions on the Stripe and Amazon accounts, where the skills did not win (store E, the report), then stores A to D |

## What this does not claim

- **Not a model ranking.** Three runs per cell show a repeated behaviour, not an error rate; the
  final answer runs are Opus 5.5 only, and Sonnet 5 is one of the answer zoo's reviewers.
- **Not real stores.** The stores are synthetic, with the traps named above. A real store has traps
  nobody planted; finding them is the first week of an engagement.
- **Blind only in parts.** Stores A to C, the planted defects and the graders were written by the same
  person as the skills. Stores D and E, the Stripe and Amazon accounts and the agency's report were each
  built by a separate Claude session that never saw the skills, with its own answer key; the scripts' first
  run on store D and every run on store E were blind, and everything after store D's first run was developed
  on store D. What makes the results checkable is that every answer and grade is kept, and the data and
  answer keys are public.
- **Not a guarantee that a definition is right.** The checks prove a figure came from the script and
  every listed item is named; whether the definition is the owner's is the owner's answer, which is
  why it is printed under every answer.

## The code

The skills, the checks, the tool server and the bench are private: they are the working tool, and a
client's skills are built with it. In an engagement the client gets the skills and checks built for
them, with their tests and eval cases.

Model runs: Claude Code 2.1.280, September 2026 (`claude plugin eval` for the first comparison on stores
A and B, the reviewers and the routing runs; `claude -p` sessions with a shell for store C, store D and
the later versions). The cost figures in the results are the tool's
list-price estimates, not charges.

## License

The text and the data in this repository are under [CC BY 4.0](LICENSE): quote them, recount them,
publish them further, and name the source. The code is not in this repository, and the license does
not reach it. `gallery/case.pdf` embeds subsets of the Segoe UI and Consolas fonts, which are Microsoft's
and not under that license.

Not affiliated with Shopify, Stripe, Amazon, Intuit or Anthropic.
