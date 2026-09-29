# The skills in claude.ai chat: three live answers

September 2026. Each skill uploaded as a ZIP in claude.ai (Customize > Skills > Upload a skill), a new chat,
Opus 5.5, store A's files attached, the owner's question typed as below. No plugin, no hooks, no MCP server:
only the skill and its scripts in claude.ai's sandbox. The answers are copied from the chat page as text, so
Markdown formatting (tables, headings, bold) is lost and the seal line cannot be verified from these copies;
the saved file the chat offered is the answer of record there.

| Chat | Skill that fired | Build (from the answer's own lines) | File |
|---|---|---|---|
| "How did August go? I need the numbers for my accountant." | shopify-monthly-summary | an earlier build: the seal says v0.9.0, the fingerprints "vunknown" (the version fallback came in 0.10.1) | [summary.md](summary.md) |
| "We sold more in August than reached the bank. Where did the money go?" | payout-reconciliation | the same earlier build (v0.9.0, "vunknown") | [payouts.md](payouts.md) |
| "Which of our products lose money?" | sku-margin-check | 0.10.1 | [margins.md](margins.md) |

What they show: each skill fired on a plain question, ran its scripts in claude.ai's sandbox, gave the
definitions it used and the files' fingerprints, named every left-out order, and ended with the seal line
from `answer.py`, the skill's last step. What they do not show: the summary and the payout reconciliation at
0.10.1 (only the margins were asked again after the skills were replaced), a team account, or Cowork.
