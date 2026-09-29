# The plugin in Cowork: three live answers

September 2026. The whole plugin at 0.11.7 uploaded in claude.ai as a ZIP (Customize > Plugins > Upload plugin:
`.claude-plugin/`, `skills/`, `hooks/`, `mcp/`, `checks/`), then a new Cowork session per question, Opus 5.5
High, store A's files attached, the owner's question as the bench asks it (with "attached" for "in the `files`
folder"). One run each. The answers are copied from the page as text, so Markdown formatting is lost; the saved
file each session offered is the answer of record there.

| Question | Skill that fired | Build (from the answer's own lines) | Figures against store A's answer key | File |
|---|---|---|---|---|
| "How did the month go? I need the key numbers for my accountant." | shopify-monthly-summary | 0.11.7, seal | total charged €2,918.82, net €2,848.32, 58 orders, 134 units: as the key | [summary.md](summary.md) |
| "We sold way more in August than landed in our bank. Where did the money go?" | payout-reconciliation | 0.11.7, seal | gap €371.08, in transit €209.69, paid out €2,448.74, the bridge closing to €0.00: as the key | [payouts.md](payouts.md) |
| "Which of our products actually lose money?" | sku-margin-check | 0.11.7, seal | the Steel Strainer at -32.76 (-30.0%), the Gift Set with no cost named as unknown, not zero: as the key | [margins.md](margins.md) |

What they show: in Cowork each skill fired on the plain question, found and ran its scripts in the session's
sandbox (the first session's first command failed and it found the scripts on disk), rendered the answer from
the results, checked and sealed it with `answer.py`, and saved it to the session's outputs. The session's
"Used in this session" panel lists the uploads and the skill; it lists no connector, so the plugin's tool server
was not used (the scripts ran directly). Whether the plugin's hooks ran cannot be seen from the page: they
speak only when an answer fails, and none of these did.

What went wrong first: the account also had the three Shopify skills uploaded one by one the day before, at
an older build. With two copies of a skill, the payouts session loaded the older one (its answer said v0.10.1).
With those copies turned off, it loaded the plugin's. An account should hold one copy of each skill.

What they do not show: more than one run per question, a team account, or the pinned calculation and the
tie-out in Cowork.
