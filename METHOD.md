# How the bench works

## The question it answers

A Claude skill for a business fails in two ways that nobody sees. Either it never runs (or the
wrong skill runs), or it runs and the answer is wrong in a way that looks right: a test order
counted as a sale, VAT-inclusive money called revenue without VAT, a refund blamed on product
quality. The bench plants such defects one at a time and records which layer stops each one, and
which nothing stops.

What it found changes the question. The strongest model rarely gets the arithmetic wrong any more;
it gets the context wrong, or leaves it unsaid: which orders count, what "sales" includes, which
month a refund or a payout belongs to. So the bench also reads every answer for what the owner can
see: whether it gives the figure the skill gives on its stated definitions, whether every order left
out, disputed or not yet paid out is named, and whether the answer says it added the figures up by hand
or could not run code.

## Four parts

| Part | What is planted | Layers measured | Model runs |
|---|---|---|---|
| **Stores** | Three synthetic stores with real-export traps; store C at a real store's size | the skills' scripts against each generator's own truth | none |
| **Skill zoo** | 11 defects in a skill's frontmatter or files, one per plugin copy | `claude plugin validate --strict`, the linter, the routing eval | 6 questions × 3 runs per defect |
| **Answer zoo** | 24 defects in 7 classes in correct answers | the number check, the coverage check, a reviewer model | 3 runs per defect and per clean answer, per reviewer |
| **Models** | the owner's questions on the three stores | Opus 5.5 with the plugin and without it: the graders (figures on the summary and payout questions, products named on margins), and what the owner can see | 3 runs per arm per case |

### Stores

Store A (`data/` in the code, `stores/store_a/` in the public case) is an EU tea shop: VAT inside the prices, a test order tagged `test`, a PayPal
order, a chargeback, payouts in transit. Store B is a US candle shop
built to differ: sales tax added on top, test orders paid through Shopify's test gateway with no
tag, an order paid partly with a gift card, a dispute the shop won, a payout adjustment, a cost
sheet typed by hand. Each generator computes `truth.json` from its own order records, not from
the CSV files it writes, so a match between script and truth is two independent paths agreeing.
Store C is a UK skincare shop at a real store's size: three months, 4,470 orders, 9,074 export
rows and 4,133 payout lines, and the question is one month. Its owner has answered the definitions
(`store_definitions.json`, next to the exports, written so a person can read it): a sale counts once
it is shipped, revenue is reported without VAT and without shipping. So August's 70 pre-orders,
paid and charged, are not August sales. It also has test orders both ways, orders cancelled after
payment, refunds of July orders paid out in August, disputes lost, won and still open (no dispute is
won in August, so the August questions do not test a won one), and gift cards.
The bench can run the same comparison on the scripts of any earlier commit; `results/stores-at-ad8b48e.json` is its first run, before the fixes it led to.

### Skill zoo

Each defect is applied to `shopify-monthly-summary` in its own copy of the plugin. The routing
eval then asks the owner questions (the summary and margins questions twice: once naming the
Shopify export, once indirectly, "last month's numbers for my accountant") and a copywriting
request, three runs each, and records whether the summary skill fires on its own question,
whether it stays out of the margins question, and whether anything fires on the unrelated request. A defect that no static layer flags but that
changes routing is the kind that reaches a client.

### Answer zoo

The correct answers are rendered from templates and store A's results, the way the skills render theirs. Each
defect changes one thing in one answer. The machine layers are free and deterministic:

- **numbers**: every figure traces to the results, every order reference exists, the currency is
  the store's;
- **coverage**: every item the results list for the owner (left-out orders, disputes, orders paid
  outside Shopify Payments, payouts in transit, products below cost or without a cost, open
  questions) is named in the answer (same file).

A defect the machine lets through goes to the **reviewer**: the same answer, the owner's question
and the results, shown to a model three times, each in a fresh session.
The reviewer must answer `VERDICT: PASS` or `VERDICT: FAIL` and list problems. **B**: FAIL and it
named the defect (a pattern per defect); **F**: FAIL for something else; **M**: PASS; **E**: the run
failed. A reviewer catches a defect when most of its three runs are B. The three untouched answers
are the clean control, also three runs each: a FAIL there is an objection to an untouched answer, read like any other.
ZOO.md counts the final reviewer run. Earlier runs, on reference answers since corrected, are not
counted: in the first (one run per answer) Opus 5.5 and Fable 5.1 failed all three untouched answers and
Sonnet 5 passed one defect; in the second Sonnet passed that defect in 2 of 3 runs and failed 3 of 6
untouched payout and margin runs.

### Models

The numbers cases run each owner question on the three stores, three times with the plugin and
three times without it, on Opus 5.5 (earlier runs of Sonnet 5 and Fable 5.1 used graders and
references since corrected, and are not reported). Stores A and B run in `claude plugin eval`.
Without the plugin the model can read the files but has no shell: on Windows plugin eval's sessions
have none, which is what a chat with the file attached gives. Store C is too big to add up by
reading, and the fair comparison there is the plugin's scripts against code the model writes
itself, so its cases run in plain `claude -p` sessions with a shell, in a fresh folder holding the
files, with no MCP servers (none of the user's connectors, and `--strict-mcp-config` keeps the
plugin's own server off too, so the skills run their scripts), no web, publishing, notification or
scheduling tools, and no user settings; with the plugin, it is loaded from a fresh copy. Those
sessions run code on the machine without a sandbox. A run passes when every grader passes. On the
summary and payout questions that is the headline figures and the traps named; on the margins
questions it is the products that must be named (the one below cost, the one with no known cost),
and no margin figure is graded. Where only
one form of the right answer exists (an order number, a total), the grader is a pattern. Where a
right answer can take several forms (a margin per unit or for the month, a bridge that starts from
card sales or from every order), the grader is a model judge given the correct figures, and a test
checks that every figure a judge is given comes from the scripts' results. The payout cases are
patterns only: the figure on the bank statement, the money in transit (net or gross), the refunds
(all, or only those paid out in the month), the disputes and the orders that never reach payouts. A
judge given the correct bridge failed right answers there, so it was dropped. The price: a pattern does
not see a misleading sentence around a right figure (in the live tests, Sonnet without the skill
called the PayPal order a permanent gap). That is graded only in the live tests, by reading. Not
every planted trap has a grader: VAT inside store A's prices, store B's sales tax and payout
adjustment, and on store C the refunds of July orders, the gift cards and PayPal orders and the cost
sheet's spellings are graded by nothing. The test on the graders' figures checks that each figure
appears in the scripts' results or the CSVs, not that it is the right one for its grader.

### The data zoo

A monthly skill breaks in the month the export changes. Eight changes are made, one at a time, to a
copy of store A whose shape the owner confirmed the month before (a new payment gateway, a new tag, a
pending payment, a new financial status, a second currency, a renamed column, an export that stops on
the 20th, a new payout line), and the scripts run on each as they were before the export checks and as
they are now. Each outcome is stopped, named, crashed or silent, with the headline figure beside it
(`results/data-zoo.json`).

### The answer hook

The skills tell the model to show the owner exactly the text that the renderer returned and the
number check passed. A Stop hook in the plugin (`hooks/check_answer.py`) holds that rule: every script
run keeps its result next to the exports (`.monthend/`), and when Claude is about to finish a turn in
which the scripts ran, the hook checks the final message against those results. Figures that trace to
no result, unknown order numbers or another currency, or items the owner should see and the message
does not name (unless it points to a saved answer that passes the whole check), send Claude back once
with the list. If the second answer fails too, the turn ends with a warning to the reader and a record
of the failed answer next to the exports. Other sessions are left alone. `results/hook-check.md` has
three live sessions with hook events recorded, and what the bench's own runs with the hook show. Up to
0.10.1 the second warning went wrong in a session that keeps a transcript, as an interactive one does
(the hook took its own feedback for the start of a new turn); the bench's sessions keep none. Fixed in
0.11.0: a turn starts at the person's own message. Every answer also ends with the fingerprints of what it was computed from
and by (each file's rows and SHA-256, the plugin's version).

## Checking the checks

A bench that only confirms its author is worth little, so after each model run every failure was
read, and so were the answers the plugin got right, except at 0.10.1, where the checks a reader judges
were not read. What that turned up:

- **Graders that failed right answers.** On the first run, four patterns failed answers written
  without the plugin that were right: a margin given per unit instead of for the month, a payout
  bridge that started from every order in the export instead of card sales. They became judges.
  On the second run the payout judge failed right answers too, with and without the plugin (the
  kept answers show a bridge that closes to the cent), so the payout cases went back to patterns,
  now accepting each right way to split the bridge. The patterns were tried on the kept answers
  before the re-run (`regrade`), so the re-run measured the models, not the graders.
- **A definition the skill, the truth and the graders shared.** Store B's truth is computed by its
  generator, independently of the scripts, but on the same definition: money paid out for this
  month's sales. Opus without the plugin reconciled to what the bank statement shows, which also
  holds the previous month's last sales, paid out in the first days of this one, and it was right:
  the skill's "paid out this month" would not match the owner's bank. Independent arithmetic is not independent
  definitions. The bridge now ends at the bank; `results/stores-at-b445df1.json` is the skills the
  first model runs used, measured against the corrected truth.
- **Reviewers that were right about the references.** On the first run Opus as a reviewer failed all
  three untouched answers; on the summary: "left after refunds" read as money kept, and VAT, shipping and the month basis were
  missing. Later Sonnet failed the untouched payout and margin answers: the figures rest on answers
  the owner has not confirmed, and the question at the end reads as cut off from them. Both were
  right; the references and the skills' instructions changed before the final run. On the final run
  Opus objected again, in 3 of 9 runs, to what the untouched answers leave unsaid or put loosely; those
  answers were not changed after it.
- **A defect nothing static saw.** `disable-model-invocation: true` passes `claude plugin
  validate` and passed the linter, and the summary skill stopped firing (0 of 6: its question
  asked plainly and indirectly, three runs each). The linter now warns on it (W06).
- **A question that said less than the script did.** The questionnaire asked about orders "tagged
  'test'"; the scripts also left out orders paid through Shopify's test gateway. Opus with a shell,
  given store C's answered definitions and no plugin, kept four test-gateway orders in the sales and
  asked the owner about them. By the words of the definition it was right. The question now names
  the gateway, and every definition is printed in words under "How this was counted".
- **A size the answer format could not carry.** A placeholder names one figure; store C leaves out
  85 orders in August and has 87 payments in transit. Lists now render whole (`|list`, `|by_reason`,
  `|count`), so every one of them is still named.
- **Half a penny.** The scripts rounded money half to even; store C's truth, like the stores' own
  figures, rounds half up, and one figure differed by a penny. All three scripts now round half up.
- **A penny that is not a definition.** Opus without the plugin on store C took VAT out of the
  month's sum; the store takes it out order by order. Over 1,555 orders the two differ by about a
  pound, and both are right. The revenue grader there now accepts a figure within two pounds of any
  of the three defensible revenues (before refunds, after refunds without VAT, after only the product
  part of refunds); the store C runs were graded again from their kept answers (`regrade`).

## What is published

The skills, the checks and the bench are private: they are the working tool. The case publishes
what its pages count:

- `ZOO.md`, generated from the results, not edited by hand;
- `results/`: the results the pages count, as recorded, including the `claude plugin eval` and
  `claude -p` runs (local paths removed, run times cut to the month), and `hook-check.md`;
- `live-tests/`: every model answer, unedited, and the figures they were checked against;
- `results/evals/answers/`: the final answer of every numbers and reviewer run the pages count, with
  and without the plugin, next to its grades, with the saved answer it points to when it saved one.
  The answers are as the model wrote them, with one change: where a model mentioned the day of the
  run, it reads `[run date]`;
- `stores/`: eight datasets: stores A to E, the Stripe account (F) and the agency's report on it, and the
  Amazon seller account (G); their exports, store C's definitions and every answer key (`truth.json`, and
  the report's `key.json`), so anyone can
  recount the truth from the CSVs; for store C also its August books (QuickBooks Online's transaction
  list and profit and loss, Shopify's payout list, and `ledger_truth.json`, what a close of those books
  must find), used by the small business case;
- `gallery/`: the case in pictures and a four-page PDF, every figure read from the results: the
  Stripe and Amazon accounts, where the skills did not beat plain Opus, then stores A to D;
- `examples/`: what the linter and the number check print on the examples.

Not published: the runs of 0.9.0 and 0.10.1 on stores A to C, two repeat runs of the store C
comparison with the same setup, and the earlier reviewer runs.

Model runs used Claude Code on the author's machine; `claude plugin eval` reports a list-price
estimate next to each run, not a charge. On Windows,
Git's `bash.exe` must come before the WSL launcher on `PATH`, or the scaffold scripts that copy the
store files into each run fail.

Running the bench on your own skills is part of an engagement: the same four parts, with your
skills, your exports and the defects your processes can produce.

## What it is not

- **Not a model ranking.** Three runs per cell (six in the skill zoo: a question asked two ways) show a
  repeated behaviour, not a rate.
- **Not a benchmark of real stores.** The three stores are synthetic, with the traps named above; a
  real store has traps nobody planted, which is what the first week of an engagement looks for.
- **Not a blind test.** The same person wrote the skills, planted the defects and chose the
  patterns a reviewer must use to name them. What makes the numbers checkable is that every
  answer and grade is kept, and every store's data and truth are public, so any figure can be
  recounted from the CSV files.
