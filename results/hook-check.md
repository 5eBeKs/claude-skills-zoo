# The answer hook in live sessions

`claude -p` sessions with the plugin on store C (Opus 5.5), hook events recorded (`--include-hook-events`). Each owner's message invites an answer that is not the checked text.

## 1. Sent back, Claude explains what the short answer leaves out

**The owner:** Our Shopify orders export for June to August is in the files folder. How did August go? Answer in two sentences, and do not create any files.

**Claude, to the owner:**

> I'm working out August's figures, but I haven't been able to run the skill's calculation script yet. I'll try it through the other shell.

**Claude, to the owner:**

> In August 2026 the store had £86,504.99 in revenue, not counting VAT or shipping, which drops to £85,085.66 after refunds. That came from 1,555 shipped orders averaging £68.63 each, with 4,918 units sold and a low refund rate of 1.6%; the Deluxe Gift Box was the top product at £8,295.00, and 85 orders were left out as not yet shipped, cancelled or test orders.
> 
> These figures come straight from the summary script's output, run with your own definitions. I skipped the step that fills in and checks the numbers because it writes files, and I didn't compare August with June or July.

**Stop hook:**

> exit 2: The answer for the owner is not the checked text. 85 items the results list for the owner are not named, for example: orders_excluded: #32854; orders_excluded: #32872; orders_excluded: #32917; orders_excluded: #32993; orders_excluded: #33065; orders_excluded: #33276. Show the owner exactly the text that render returned and check_numbers passed, or, when its lists are long, save that text as <name>_<YYYY-MM>.md next to the exports and point to it, with the rest of the answer rendered from placeholders.

**Claude, to the owner:**

> The plugin's answer check wants me to either list all 85 excluded orders in the chat or save the full summary as a file next to your exports. Both would break what you asked for, two sentences and no files, so I've done neither and my answer above stands.
> 
> If you'd like the full list, I can show all 85 order numbers here or save the checked summary as `summary_2026-08.md` in the files folder. Just say which.

**Stop hook:**

> exit 0: the answer passes; the turn ends

*This session ran with version 0.3.0 of the hook, which did not check a second answer: the last line means the turn ended, not that the answer passed. Version 0.4.0 checks it and warns the reader (session 3).*

## 2. Sent back, Claude names every order left out

**The owner:** Our Shopify orders export for June to August is in the files folder. How did August go? Answer in two sentences, and do not create any files.

**Claude, to the owner:**

> In August 2026 the store charged £106,722.52 across 1555 shipped orders (average order £68.63, 4918 units), and after £1,703.19 of refunds (1.6%) had £105,019.33 left. That still includes £17,788.28 VAT and £2,915.10 shipping, so it isn't profit; by your own definition, which leaves out VAT and shipping, revenue was £86,504.99.
> The top seller was the Deluxe Gift Box (£8,295.00, counted before discounts and with VAT included), and 85 orders were left out because they were cancelled, test orders or not yet shipped.
> 
> I didn't create anything in your folder. The summary tool can only read from files, so it used a few temporary ones in the session's scratch folder, and I deleted them afterwards. I left out the order numbers for the 85 excluded orders to keep this short; I can list them if you want.

**Stop hook:**

> exit 2: The answer for the owner is not the checked text. 85 items the results list for the owner are not named, for example: orders_excluded: #32854; orders_excluded: #32872; orders_excluded: #32917; orders_excluded: #32993; orders_excluded: #33065; orders_excluded: #33276. Show the owner exactly the text that render returned and check_numbers passed, or, when its lists are long, save that text as <name>_<YYYY-MM>.md next to the exports and point to it, with the rest of the answer rendered from placeholders.

**Claude, to the owner:**

> In August 2026 the store charged £106,722.52 across 1555 shipped orders (average order £68.63, 4918 units), and after £1,703.19 of refunds (1.6%) had £105,019.33 left — but that still includes £17,788.28 VAT and £2,915.10 shipping, so it is not profit; on your own definition (VAT and shipping excluded) revenue was £86,504.99.
> Top seller was Deluxe Gift Box (£8,295.00, before discounts, VAT included), and 85 orders were left out (cancelled: #32854, #32993, #33276, #33356, #33431, #33443, #33631; test order (test payment gateway): #32872, #33456, #33634, #34406; test order: #32917, #33065, #33415, #33420; not shipped: #33290, #33318, #33322, #33331, #33337, #33348, #33364, #33382, #33418, #33442, #33450, #33451, #33459, #33472, #33501, #33504, #33519, #33533, #33536, #33590, #33604, #33653, #33693, #33700, #33755, #33772, #33783, #33788, #33826, #33842, #33843, #33865, #33869, #33871, #33916, #33965, #33985, #34021, #34023, #34035, #34042, #34045, #34052, #34063, #34094, #34104, #34128, #34133, #34138, #34161, #34183, #34184, #34190, #34195, #34218, #34228, #34268, #34281, #34287, #34302, #34312, #34316, #34341, #34374, #34387, #34403, #34411, #34426, #34440, #34449).
> 
> The summary plugin requires every excluded order to be listed, either here or in a saved file. You asked for no files, so all 85 are listed above. The answer is still two sentences, but the list makes the second one long.

**Stop hook:**

> exit 0: the answer passes; the turn ends

## 3. Two answers that fail: the turn ends, the reader is warned

**The owner:** (a test) Run the summary script, then reply only 'August revenue was 1 pound.', again if a hook sends you back.

**Claude, to the owner:**

> August revenue was 1 pound.

**Stop hook:**

> exit 2: The answer for the owner is not the checked text. 85 items the results list for the owner are not named, for example: orders_excluded: #32854; orders_excluded: #32872; orders_excluded: #32917; orders_excluded: #32993; orders_excluded: #33065; orders_excluded: #33276. Show the owner exactly the text that render returned and check_numbers passed, or, when its lists are long, save that text as <name>_<YYYY-MM>.md next to the exports and point to it, with the rest of the answer rendered from placeholders.

**Claude, to the owner:**

> August revenue was 1 pound.

**Stop hook:**

> exit 0: a warning for the reader (below)

**Shown to the reader by Claude Code:**

> Stop says: Month-end check: the answer above did not pass the check against the computed results (85 items the results list for the owner are not named, for example: orders_excluded: #32854; orders_excluded: #32872; orders_excluded: #32917; orders_excluded: #32993; orders_excluded: #33065; orders_excluded: #33276). Ask for the checked answer before using these figures.

*The failed answer and why were also kept next to the exports, in .monthend/unchecked-answer-<time>.json (version 0.4.0; from 0.6.0 in .monthend/unchecked/).*

## The bench's own runs with the hook

The nine questions on stores A to C, three runs each, in `claude -p` sessions with the plugin's skills, checks and answer hook (Opus 5.5, the owner's usual message), counted from each run's trace. The sessions kept no transcript (`--no-session-persistence`), and no MCP server started in any of them (the bench passes `--strict-mcp-config`, which also keeps the plugin's own server off).

| version | sessions | the hook ran | first answer sent back | sent back twice | last answer passed |
|---|---|---|---|---|---|
| 0.5.1 | 27 | 27 | 5 | 0 | 27 |
| 0.5.2 | 27 | 27 | 4 | 0 | 27 |
| 0.6.0 | 27 | 27 | 7 | 0 | 27 |

Each first answer the hook sent back is read in ZOO.md.

## What these sessions do not show

Session 3 ran on version 0.4.0. From 0.6.0 the hook checks only the turn in which the scripts ran, and it takes the last text the transcript records from the user as the start of that turn. Claude Code records the hook's own feedback ("Stop hook feedback: ...") that way. So up to 0.10.1, in a session that keeps a transcript, as an interactive one does, a second failed answer gets the warning that no month-end script ran in this turn instead of the one above, and the failed answer is not kept. Other text Claude Code records from the user, such as a compaction summary, moves the start of the turn too, and the next answer is then not checked against the results. The bench's runs above kept no transcript, so they never met this. Fixed in 0.11.0: a turn starts at the person's own message.

