# Store E: a second store built apart, the skills unchanged

A second separate Claude session, which never saw the skills, the bench or store D, built a Dutch home goods store: prices in EUR with VAT inside, sales also in GBP, USD and CHF, Shopify Payments, Klarna, PayPal, bank transfer and gift cards, 21,241 orders from July to early October 2026 (709 of them in October), 65 traps, and an answer key from its own events. The skills were not changed for it: both measures below are blind. The data and the answer key are in `stores/store_e/`.

## The scripts against the answer key

40 of 55 judged figures match. What differs: a won chargeback written as a positive dispute row is netted into the chargebacks instead of shown apart; SKUs renamed mid-period are not recognised, so their products read as having no cost; gift cards sold are short by 100 to 225 euros a month; tips are not found; in September the bridge does not close although the bank figure is right. Store D's rows, as in STORE-D.md: `results/store-e-blind-at-a3202a7.json`.

## Opus on three owner questions

Three runs each, claude-opus-5-5, `claude -p` with a shell and the store's four exports, the plugin (0.10.1, the whole plugin, answer hook included, its MCP server off) against no plugin. The graders were written from the answer key alone and committed before the first run. A separate Claude review session then read them against the answers: five of them ask for a figure any right answer gives (the bank, the failed payout, the reserve, gift cards sold, the products without a cost), and four ask for more than that (the money in transit as one total, the renamed SKUs' old codes written out, the test orders' numbers, and Analytics' net and total sales to the cent, which the orders export cannot give: it does not date refunds). Both counts are below.

| Question | Checks | With the skills | Without | The plugin's own check passed at the end |
|---|---|---|---|---|
| Less reached our bank from Shopify in August than we sold. The Shopify exports are in the `files` folder: orders (July to early October), the Shopify Payments transactions and the payouts list. How much reached the bank in August, and where did the rest go? | bank-figure, failed-payout, in-transit, reserve | 3 of 3 | 0 of 3 | 3 of 3 |
| What did we sell in September? Our bookkeeper needs the sales figures as Shopify reports them, and to know what is in them. The Shopify orders export (July to early October) is in the `files` folder. | gift-cards-sold, net-sales, test-orders, total-sales | 0 of 3 | 0 of 3 | 2 of 3 |
| Which of our products made money in July, which lost money, and which can you not tell? The Shopify orders export (July to early October) and our products export are in the `files` folder. | no-cost-named, renamed-skus | 3 of 3 | 1 of 3 | 2 of 3 |

All three questions, every grader: **6 of 9** answers passed with the skills, **1 of 9** without. On the five graders any right answer passes: **6 of 9** with the skills, **9 of 9** without. On a second store built apart, the Shopify skills did not do better than plain Opus.

What the answers show, read by hand:

- **The bank question.** Every answer on both sides gave the bank figure, the failed payout and the reserve. The skills gave the money in transit as one total; one plain answer gave it to the cent in two lines, and two gave the same money before fees.
- **The sales question.** No answer on either side gave Analytics' net or total sales to the cent, and none could from this export. The skills were short on gift cards sold (their script's error, above); plain Opus got them right. The skills' saved reports named the three staff test orders by number (one chat answer did not); two plain answers named them as the store's staff orders without numbers.
- **The margins question.** The skills put the renamed napkins among the products whose margin they could not tell, though the products export gives their cost (the script's renamed-SKU gap, above), and with them three handmade bowls that have no SKU in either export; the plain answers matched the napkins by name and costed them. The renamed-SKU grader, which asks for the old codes, passed the skills for naming them while leaving them uncosted.

What this means for the skills: the Shopify scripts were developed on stores A to D, and a store built apart finds what they still get wrong (the won chargeback's format, renamed SKUs, gift cards, tips). What held: every report the skills saved carried its definitions, its fingerprints and every left-out order (the chat answers published here do not always repeat them), and the plugin's own check passed most of them.

## Files

- `stores/store_e/`: the four exports, the answer key and the generator's notes;
- `results/store-e-blind-at-a3202a7.json`: the scripts' blind run, row by row;
- `results/store-e-runs.json`, `results/store-e-answers/`: every run's grades and final answer, and the reports the runs saved (`*-saved-*.md`), which the graders read with the chat.
