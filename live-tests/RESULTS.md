# Live tests: the same questions, with and without the skills

*Run in September 2026 inside Claude Code, on a subscription (no API). Each run is a fresh subagent
that sees only the store's CSV files and the owner's message; it does not see the generator, the
planted traps or the expected numbers. Answers are saved unedited in `answers/`, the correct
figures (produced by the skills' scripts) in `truth/`.*

## Result

| Model | Question | Without the skill | With the skill |
|---|---|---|---|
| Haiku 4.5 | Monthly summary | **Wrong, 2 of 2 runs.** Test order counted as a sale (€2,999.72 charged instead of €2,918.82); units 139–140 instead of 134; run 1's average order value divides 59 orders' money by 58. Run 1 calls €2,929.22 "your actual deposit amount". | **Correct.** Number check passed on the first try. |
| Haiku 4.5 | Why less reached the bank | **Wrong, 2 of 2 runs.** Run 1: calls the test order "missing from the payout file, contact Shopify Support", counts the dispute fee twice in its list. Run 2: "charged €2,840.22", "landed in your bank €2,553.54" (both wrong), full refund and PayPal order missing. | **Correct.** Passed on the second try (the check tripped on "August 31", since fixed). |
| Sonnet 5 | Monthly summary | **Wrong, 2 of 2 runs.** Test order counted (59 orders, €2,999.72, AOV €50.84). Run 1 says this total "matches what actually settled through your payment processor" (it does not) and "three orders used WELCOME10" (six did). Run 2 notices the test tag but leaves it in the totals. | **Correct.** Passed on the first try. |
| Sonnet 5 | Why less reached the bank | **Bridge right, explanation wrong, 2 of 2 runs.** Run 1 counts the €99 PayPal order as a "permanent gap". Run 2 says 54 card charges (there are 57), and its table of causes does not add up to its stated gap. | Run 1: figures right, **currency wrong** ("$" for a EUR store), and two totals added after the check had passed. Both are skill bugs, fixed. Run 2 on the fixed skill: **correct**, checked text shipped unchanged. |
| Opus 5.5 | All three questions | **Correct** apart from one count ("56 charges"; there are 57). Deeper than the skills: spread discounts and fees over products, flagged shipping as a possible leak. | Not needed on this data. |

## What this shows

- The two cheaper models make the **same silent mistake** without the skill: the order tagged
  `test` is counted as revenue. The answers look confident and well formatted.
- With the skill, the numbers come from the script and every run of both models was right on
  the figures.
- The strongest model did not need the skill on this data. The skill's value there is a fixed,
  checkable format and definitions that stay the same month to month, not accuracy.
- The live runs found **four bugs in the skill itself** that the offline tests had missed:
  1. the payout result carried no currency, so a model wrote "$";
  2. a model checked its draft, then added two totals and shipped unchecked text;
  3. those totals were legitimate but not in the script output, so the check pushed the model
     around it; the script now reports the totals owners ask about;
  4. the check read "August 31" as a figure.
  Each fix has a test in the suite.

## How to read the number check here

`check_numbers.py` confirms that every figure in an answer comes from the script's JSON.
Run on an answer written **without** the skill, it flags nearly everything, including correct
derived figures (Opus's "€2,393.55 ex-VAT" is right, but no script printed it). So the verdicts
above for runs without the skill are my manual review against `truth/`, not the checker's.
With the skill, the checker's verdict is the verdict.

## Limits

- One or two runs per cell. That is enough to see a repeated mistake, not to give an error rate.
- Synthetic data with planted traps. A real store will have traps nobody planted.
- These runs followed the skill because the prompt pointed to it. Whether Claude **picks** the
  skill on its own from its description is a separate test: skills load at session start, so
  it needs a fresh session with the skills installed.
