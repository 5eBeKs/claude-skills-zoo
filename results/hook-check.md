# The answer hook in a live session

One `claude -p` session with the plugin on store C (Opus 5.5), with hook events recorded (`--include-hook-events`). The owner's message asked for a short answer and no files, which invites a retelling instead of the checked text. In order:

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

> exit 0: the turn ends (it sends Claude back at most once a turn)

The owner kept the last word: asked for two sentences and no files, the answer stayed short, and the owner was told what it leaves out and where the checked version comes from. In six more sessions with the hook (store C, the summary and the payouts questions, three each, the owner's usual message) the first answer already passed: each showed the checked text or pointed to the checked file it saved, and the hook let it stand. All six graded right.

