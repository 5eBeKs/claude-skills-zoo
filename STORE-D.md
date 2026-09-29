# Store D: a store built apart from the skills

Stores A to C were built by the same work that wrote the skills, so a wrong idea of Shopify's exports could sit in both and pass. Store D was built by a separate Claude session that was told to make a realistic Shopify store for testing month-end tools and never saw the skills, their checks or this bench. It wrote its own truth from its own events, not from the CSV files, and listed where it was not sure how Shopify writes a field.

- **The store:** a US clothing store (fictional), selling in USD, EUR, GBP, CAD; 30,251 orders June to August 2026 (58,166 rows), 32,249 Shopify Payments transactions, 68 payouts; exports taken on September 5 (`stores/store_d/`). The largest month holds about 15,164 orders.
- **The traps:** 68 in the 15 groups below (the generator's own list, in Russian, stays private; the orders each judged row needs are in the results files).
- **What is judged:** only figures that mean the same in its truth and in the skills. Its truth follows Shopify Analytics; the skills follow the owner's definitions. Where the two count differently on purpose, both are shown and neither is scored.
- **Blind, then not:** the first run (0.6.1) was blind. Everything after it was developed against this same store, so 0.10.1's figures show the fixes hold here, not that they would hold on a store nobody has seen. Store E was that check: [STORE-E.md](STORE-E.md).

| | 0.6.1, the first run (blind) | 0.10.1 |
|---|---|---|
| Figures that match the truth | 18 of 50 | 55 of 56 |
| On the 50 rows both runs have | 18 | 49 |
| Differ | 16 | 1 |
| Not reported | 16 | 0 |

12 of the 56 judged rows are a yes/no or a zero (the script ran, the bridge says what it should, nothing won back, no reserve, no failed payout): they count, but they are not money.

## Every judged figure

| Month | Skill | Figure | Truth | 0.6.1 | 0.10.1 |
|---|---|---|---|---|---|
| 2026-06 | payouts | paid out in the month (the bank) | 572,456.23 | ✗ 467,444.55 | ✓ 572,456.23 |
| 2026-06 | payouts | the bridge says it closes only when the bank figure is right | yes | ✗ no | ✓ yes |
| 2026-06 | payouts | in transit at month end | 117,366.90 | ✓ 117,366.90 | ✓ 117,366.90 |
| 2026-06 | payouts | refunds processed | 82,726.47 | ✓ 82,726.47 | ✓ 82,726.47 |
| 2026-06 | payouts | processing fees | 25,967.07 | ✓ 25,967.07 | ✓ 25,967.07 |
| 2026-06 | payouts | chargebacks | 1,212.93 | ✓ 1,212.93 | ✓ 1,212.93 |
| 2026-06 | payouts | chargebacks won back | 0.00 | — not reported | ✓ 0 |
| 2026-06 | payouts | chargeback fees, net of fees returned | 240.00 | — not reported | ✓ 240.00 |
| 2026-06 | payouts | reserve held at month end | 0.00 | — not reported | ✓ 0 |
| 2026-06 | payouts | Shopify Payments activity (paid out + in transit, net) | 584,811.45 | ✓ 584,811.45 | ✓ 584,811.45 |
| 2026-06 | payouts | failed payouts | 2026-06-30 | — not reported | ✓ 2026-06-30 |
| 2026-06 | summary | orders created in the month, test orders left out | 7,047 | ✗ 7,048 | ✓ 7,047 |
| 2026-06 | summary | test orders, left out or named for the owner | 5 items | ✗ 4 items | ✓ 5 items |
| 2026-06 | summary | cancelled orders | 121 | ✗ 122 | ✓ 121 |
| 2026-06 | summary | gift cards sold, kept out of sales | 6,125.00 | — not reported | ✓ 6,125.00 |
| 2026-06 | margins | the margins ran on Shopify's products export (Cost per item) | yes | ✗ no | ✓ yes |
| 2026-06 | margins | products sold without a cost | 7 items | — | ✓ 7 items |
| 2026-06 | margins | SKUs renamed mid-period, named as possible renames | 30 items | — | ✓ 30 items |
| 2026-07 | payouts | paid out in the month (the bank) | 723,870.37 | ✓ 723,870.37 | ✓ 723,870.37 |
| 2026-07 | payouts | the bridge says it closes only when the bank figure is right | yes | ✓ yes | ✓ yes |
| 2026-07 | payouts | in transit at month end | 72,442.46 | ✓ 72,442.46 | ✓ 72,442.46 |
| 2026-07 | payouts | refunds processed | 80,598.77 | ✓ 80,598.77 | ✓ 80,598.77 |
| 2026-07 | payouts | processing fees | 29,470.93 | ✓ 29,470.93 | ✓ 29,470.93 |
| 2026-07 | payouts | chargebacks | 3,202.05 | ✓ 3,202.05 | ✓ 3,202.05 |
| 2026-07 | payouts | chargebacks won back | 268.13 | — not reported | ✓ 268.13 |
| 2026-07 | payouts | chargeback fees, net of fees returned | 330.00 | — not reported | ✓ 330.00 |
| 2026-07 | payouts | reserve held at month end | 0.00 | — not reported | ✓ 0 |
| 2026-07 | payouts | Shopify Payments activity (paid out + in transit, net) | 678,945.93 | ✗ 697,078.33 | ✓ 678,945.93 |
| 2026-07 | payouts | failed payouts | none | — not reported | ✓ none |
| 2026-07 | summary | orders created in the month, test orders left out | 8,023 | ✗ 8,024 | ✓ 8,023 |
| 2026-07 | summary | test orders, left out or named for the owner | 4 items | ✗ #61399, #61407, #61410 | ✓ 4 items |
| 2026-07 | summary | cancelled orders | 141 | ✗ 142 | ✓ 141 |
| 2026-07 | summary | gift cards sold, kept out of sales | 7,925.00 | — not reported | ✓ 7,925.00 |
| 2026-07 | margins | the margins ran on Shopify's products export (Cost per item) | yes | ✗ no | ✓ yes |
| 2026-07 | margins | products sold without a cost | 12 items | — | ✓ 12 items |
| 2026-07 | margins | SKUs renamed mid-period, named as possible renames | 30 items | — | ✓ 30 items |
| 2026-08 | payouts | paid out in the month (the bank) | 986,756.77 | ✓ 986,756.77 | ✓ 986,756.77 |
| 2026-08 | payouts | the bridge says it closes only when the bank figure is right | yes | ✓ yes | ✓ yes |
| 2026-08 | payouts | in transit at month end | 312,160.86 | ✓ 312,160.86 | ✓ 312,160.86 |
| 2026-08 | payouts | refunds processed | 110,526.53 | ✓ 110,526.53 | ✓ 110,526.53 |
| 2026-08 | payouts | processing fees | 53,410.28 | ✓ 53,410.28 | ✓ 53,410.28 |
| 2026-08 | payouts | chargebacks | 2,184.93 | ✓ 2,184.93 | ✓ 2,184.93 |
| 2026-08 | payouts | chargebacks won back | 677.51 | — not reported | ✓ 677.51 |
| 2026-08 | payouts | chargeback fees, net of fees returned | 210.00 | — not reported | ✓ 210.00 |
| 2026-08 | payouts | reserve held at month end | 25,000.00 | — not reported | ✓ 25,000.00 |
| 2026-08 | payouts | Shopify Payments activity (paid out + in transit, net) | 1,226,475.17 | ✓ 1,226,475.17 | ✓ 1,226,475.17 |
| 2026-08 | payouts | failed payouts | none | — not reported | ✓ none |
| 2026-08 | summary | orders created in the month, test orders left out | 15,164 | ✗ 15,167 | ✗ 15,165 |
| 2026-08 | summary | test orders, left out or named for the owner | 8 items | ✗ 5 items | ✓ 8 items |
| 2026-08 | summary | cancelled orders | 264 | ✗ 266 | ✓ 264 |
| 2026-08 | summary | gift cards sold, kept out of sales | 15,475.00 | — not reported | ✓ 15,475.00 |
| 2026-08 | margins | the margins ran on Shopify's products export (Cost per item) | yes | ✗ no | ✓ yes |
| 2026-08 | margins | products sold without a cost | 14 items | — | ✓ 14 items |
| 2026-08 | margins | SKUs renamed mid-period, named as possible renames | none | — | ✓ none |
| 2026-06..08 | summary | tips over the period, kept out of sales | 3,769.11 | — not reported | ✓ 3,769.11 |
| 2026-06..08 | summary | orders flagged as not adding up: exactly those where an edit removed an item and its line stayed in the export | 27 items | ✗ 12030 items | ✓ 27 items |

Where 0.6.1 stopped, the row says so: the margins would not read Shopify's products export.

What still differs:

- 2026-08, orders created in the month, test orders left out: counted until the owner says: #67254 has no test tag or test gateway, only a note or an e-mail says test, and the answer names it and asks

How the rows changed: after the 0.7.0 run, the monthly tips became a definition row (an order cancelled the next month moves $3.78 of tips between June and July; the period total is judged), and the monthly 'orders that do not add up' rows, whose truth of 0 was wrong, gave way to one row for the 27 orders where an edit removed an item. The first run was read again with these rows; its commit message still says 18 of 54.

## Counted differently on purpose

| Month | Figure | Shopify Analytics (truth) | The skills | Why |
|---|---|---|---|---|
| 2026-06 | tips, kept out of sales | 748.28 | 744.50 | an order cancelled next month: its tip is the month's in Analytics and reversed later; the skill leaves the cancelled order out (the period is judged) |
| 2026-06 | sales (Shopify Analytics: gross, discounts, returns by their own day) | 582,638.72 | 687,315.88 | Analytics counts unpaid orders and dates returns by refund day; the skill counts paid orders and refunds in the month of the order, on its usual answers (store D has no definitions file) |
| 2026-07 | tips, kept out of sales | 1,193.16 | 1,196.94 | an order cancelled next month: its tip is the month's in Analytics and reversed later; the skill leaves the cancelled order out (the period is judged) |
| 2026-07 | sales (Shopify Analytics: gross, discounts, returns by their own day) | 664,373.26 | 764,287.41 | Analytics counts unpaid orders and dates returns by refund day; the skill counts paid orders and refunds in the month of the order, on its usual answers (store D has no definitions file) |
| 2026-08 | tips, kept out of sales | 1,827.67 | 1,827.67 | an order cancelled next month: its tip is the month's in Analytics and reversed later; the skill leaves the cancelled order out (the period is judged) |
| 2026-08 | sales (Shopify Analytics: gross, discounts, returns by their own day) | 1,218,849.78 | 1,442,109.13 | Analytics counts unpaid orders and dates returns by refund day; the skill counts paid orders and refunds in the month of the order, on its usual answers (store D has no definitions file) |

The skills' sales are money as charged, tax and shipping in, on the usual answers; each answer asks the owner to confirm them, and a definitions file changes them. For a US store that adds sales tax on top this default is the wrong headline for a bookkeeper; see the summary question below.

## The traps, by group

| Traps | Group | What is in the data | What the skills do | Judged here |
|---|---|---|---|---|
| T01-T03 | Dates and time zone | orders in the last and first minutes of a month; the last evening of a month is already the next month in UTC | counted by the store's own time; every monthly figure above rests on it | partly |
| T04-T10 | Refunds | refunds in a later month, September refunds of August orders, May orders refunded in June, partial, shipping-only and item-less refunds, exchanges | refunds processed each month match; the summary puts a refund in its order's month, the owner's definition, and says so | partly |
| T11-T14 | Order edits | items added or removed by an edit, an edit in another month, an added item not yet paid | the 27 orders whose removed item stayed in the export are flagged, and only those | yes |
| T15-T18 | Cancellations | cancelled before and after the payout, unpaid ones voided, cancelled in another month | cancelled orders counted exactly; each is named as left out | yes |
| T19-T22 | Chargebacks | won, lost with the order still 'paid', open, in another month | chargebacks, the amount won back and the fees net of fees returned all match | yes |
| T23-T26 | Gift cards | gift cards sold, orders paid only by gift card, gift card plus card, refunds to a gift card | gift cards sold are kept out of sales and match; split payments are named | partly |
| T27-T29 | Manual payments | bank deposit and cash on delivery paid later or never, a refused COD | left out as not yet paid, each named; money outside Shopify Payments named | no |
| T30-T34 | B2B | net-15/30 orders, paid later, part paid, overdue, refunded while unpaid | left out as not yet paid, each named with its reason | no |
| T35-T37 | Test and deleted orders | test orders through the test gateway, tagged, and one through the live gateway with no tag; deleted orders | seven left out; the untagged one named and asked about | yes |
| T38-T42 | Channels | point of sale in cash and by card, subscriptions, phone orders and custom items, PayPal | card fees at both rates match; PayPal and cash named as outside payouts | partly |
| T43-T48 | Order amounts | tips, duties, VAT inside UK and EU prices in a US store, four currencies exported in dollars, exchange-rate losses on refunds, cents lost converting field by field | tips kept out of sales and match over the period; VAT taken out order by order; cents tolerated, not flagged | partly |
| T49-T53 | Discounts | free orders, discounts with no code, a sale through compare-at prices, free shipping by code, even exchanges | the export's arithmetic reads a Subtotal after discounts; no false alarms | partly |
| T54-T58 | Products and SKUs | lines without a SKU, SKUs renamed mid-period, products with no cost, a product deleted before the export, a price change | products without a cost match; renamed SKUs named as possible renames, never costed on a guess | yes |
| T59-T62 | Authorisation and capture | authorised not captured, captured next month, expired, paid later than ordered | left out with the reason; the rest charged after the month end named with its date | no |
| T63-T68 | Payouts | transactions for orders not in the export, a failed payout paid again, a reserve, payouts after the month end, June's first payouts carrying May, an adjustment | the bank, in transit, the reserve and the failed payout match; May's transactions are their own line | yes |

What still reads badly: most of the 'charge does not match the order' items in June are exchanges (the order's total changed, the first charge did not); the answer lists them without saying so.

## What store D changed

In 0.7.0:

- **The bank:** June's first payouts carried May's transactions, which a transactions export starting June 1 does not have. The first run closed June's bridge on itself; now the payouts export is the bank, those transactions are their own line, and a warning says that part is not checked transaction by transaction.
- **The payout lines:** disputes won back and their fee, a reserve, a failed payout paid again and adjustments each have a line; the rest of an order charged after the month ends is named with its date.
- **Subtotal:** Shopify's help does not say whether it is before or after discounts; store D's is after, stores A to C before. Both are read, and the export's is named.
- **Not sales:** tips, gift cards sold and (since 0.10.1) duties; a cancelled test order is named as a test; an order only its note calls a test is named and asked about.
- **Margins:** Shopify's products export is a cost sheet; a product without a SKU is costed by its name; an old SKU is named as a possible rename; VAT inside UK and EU prices comes out order by order.

Later, after reviews in fresh sessions:

- **No alarm stays quiet:** every warning of a result must be in the answer word for word.
- **Each figure under its own words:** render records where every figure goes and under which label; a figure under other words, with another sign or typed by hand sends the answer back.
- **No needless question:** without a VAT rate the margins take each order's own tax.
- **The check travels with the skill:** where no hook runs (claude.ai), the skill's last step renders, checks and seals the answer.
- **The owner's files:** writing the definitions or recording the export's shape asks the owner; editing an export or the kept results is refused.

## Opus on the owner's questions

Three questions an owner asks, three runs each, claude-opus-5-5, in `claude -p` sessions with a shell and the store's files; the plugin with its answer hook against no plugin (its MCP server off, `--strict-mcp-config`, so the skills ran their scripts). Every final answer is kept in `results/store-d-answers/`, with the report it saved when it saved one.

Two ways of grading, both shown. **As written:** the graders fixed before any answer was read, on the chat alone. **As read:** two graders widened after reading the answers: the report an answer saved is read with it (the skills put lists longer than about 20 items there and give the count in the chat; plain answers saved none, so this helps only the skill side), and a renamed SKU may be named as a family (`CT-…`). The graders look for the figures and names the skills give (117,366.90 in one piece, the order numbers in the chat, the `CT-…` codes): written for this store and these skills, not a neutral test. The last column: whether the plugin's own answer check passed the final answer (its Stop hook's last word in the run).

| Answers that passed every grader | As written | As read | The plugin's own check passed at the end |
|---|---|---|---|
| 0.7.0, with the skills | 4 of 9 | 8 of 9 | 9 of 9 |
| 0.7.0, without | 0 of 9 | 1 of 9 | no plugin |
| 0.8.0, the margins question again, with the skills | 2 of 3 | 3 of 3 | 2 of 3 |
| 0.10.1, with the skills | 7 of 9 | 9 of 9 | 7 of 9 |

What the plain answers did find, read by hand (the graders look for exact figures): all three gave the bank figure for June and a bridge, line by line, that closes to it; all three said May's money came in June's first payouts, one with the exact amount; none gave the money in transit at the end of June as one figure (one gave it as two parts that add up to it). With the skills, May's transactions and the money in transit were lines of their own.

Where the plugin's own check did not pass (three answers: two of the payouts question at 0.10.1, where the model typed the payout rows into its chat answer instead of giving the checked text, and one of the margins question at 0.8.0, with four figures in no computed result), the check ended the turn with a warning. Those answers are counted as the graders found them, and the warning is kept at the end of each.

The one figure the summary question asks for ("one sales figure") is not graded. With the skills, on the usual definitions, the answers gave money as charged, sales tax, shipping and (before 0.10.1) duties in: about a fifth above Analytics net sales. Plain Opus gave a figure near Analytics net sales. The definitions file changes the skills' basis; the default for a store that adds tax on top is an open decision.

**numbers-payouts-d** (the 0.7.0 runs): "Less reached our bank from Shopify in June than we sold. The Shopify exports are in the `files` folder: orders (June to August), the Shopify Payments transactions and the payouts list. How much reached the bank in June, and where did the rest of June's sales go?"

| Check | What it looks for | With (as written / as read) | Without (as written / as read) |
|---|---|---|---|
| bank-figure | What reached the bank in June (the payouts export; truth.json months.2026-06.payouts.deposited_total). | 3 / 3 of 3 | 3 / 3 of 3 |
| failed-payout | The payout of June 30 failed and was paid again in July. | 3 / 3 of 3 | 3 / 3 of 3 |
| in-transit | Money in transit at the end of June, the failed payout of June 30 included (truth: money_in_transit.closing). | 3 / 3 of 3 | 0 / 0 of 3 |
| may-transactions | June's first payouts carried May's transactions, which the transactions export (from June 1) does not have. | 3 / 3 of 3 | 1 / 1 of 3 |

**numbers-summary-d** (the 0.7.0 runs): "What did we sell in August? Our bookkeeper needs one sales figure and to know what is in it. The Shopify orders export, June to August, is in the `files` folder."

| Check | What it looks for | With (as written / as read) | Without (as written / as read) |
|---|---|---|---|
| gift-cards-sold | Gift cards sold in August (not sales until used; truth: sales.breakdown.gift_card_sales_not_in_gross_sales). | 3 / 3 of 3 | 3 / 3 of 3 |
| test-orders | The seven test orders a tag or the test gateway marks, each named. | 0 / 3 of 3 | 0 / 0 of 3 |
| tips | Tips in August (not sales; truth: sales.breakdown.tips_not_in_total_sales). | 3 / 3 of 3 | 2 / 2 of 3 |
| unflagged-test-order | A checkout test through the live gateway with no tag: only its note and e-mail say test. | 3 / 3 of 3 | 1 / 1 of 3 |

**numbers-margins-d** (the 0.7.0 runs): "Which of our products made money in July, which lost money, and which can you not tell? The Shopify orders export (June to August) and our products export are in the `files` folder."

| Check | What it looks for | With (as written / as read) | Without (as written / as read) |
|---|---|---|---|
| no-cost-named | Products sold in July without a cost: three without a SKU, the Forest hoodies, and the bucket hat deleted before the export. (The pattern asks for Enamel Pin Set, Gift Wrap and Silk Bandana; the truth has a fourth product without a SKU or a cost in July, a custom embroidery line, which is not asked for.) | 2 / 2 of 3 | 2 / 2 of 3 |
| renamed-skus | Classic Crew Tee's SKUs were renamed on July 15 (CT-* to HP-TEE-CLS-*): the old ones sold before, with no cost in the products export under that name. | 1 / 2 of 3 | 0 / 1 of 3 |

## Files

- `stores/store_d/`: the four exports and `truth.json`, as the generator wrote them;
- `results/store-d.json` (0.10.1) and `results/store-d-at-6a8a6f0.json` (0.6.1, the blind run): every row above;
- `results/store-d-runs*.json`: every run's grades, as written and as read;
- the generator's code stays private; it rebuilds these files byte for byte from its seed.
