The stop hook rejected my summary because I reworded the checked figures. Here is the checked text word for word. The long lists are only in the saved file.

---

# Shopify Payments reconciliation: June 2026

**Card sales in June were $119,106.04 more than what reached the bank in June.** Card orders placed in June: $691,562.27. Paid out to the bank in June: $572,456.23. The bridge closes: unexplained difference $0.00.

**Warning:**
- 105011.68 of the bank figure is taken from the payouts export for payouts that carry transactions from before the transactions export starts (2026-06-01): that part is not checked transaction by transaction.

## The bridge

| | USD |
|---|---:|
| Card orders placed in June (Shopify Payments, shipped yet or not) | 691,562.27 |
| − Refunds processed in June | 82,726.47 |
| of which on orders from earlier months | 45,616.95 |
| − Card fees | 25,967.07 |
| − Disputes: amount and fees | 1,212.93 and 240.00 |
| − Still in transit at month end | 117,366.90 |
| = Paid out for June's card transactions | 467,444.55 |
| + Paid out in June for transactions before the transactions export starts | 105,011.68 |
| = Paid out to the bank in June | 572,456.23 |

There were no reserves, Shopify adjustments or disputes won back in June. The disputes' net cost is $1,452.93.

**Where the rest went:** refunds, card fees and disputes are money that is gone for good. The amount still in transit was paid out in July (see below). Going the other way, the first June payouts (1 to 4 June) carried transactions from before 1 June, which the transactions export does not cover:

| Payout date | Payout total | In the transactions export | Not in it |
|---|---:|---:|---:|
| 2026-06-04 | 18,603.09 | 12,736.09 | 5,867.00 |
| 2026-06-03 | 60,256.61 | 0.00 | 60,256.61 |
| 2026-06-02 | 21,209.54 | 0.00 | 21,209.54 |
| 2026-06-01 | 17,678.53 | 0.00 | 17,678.53 |

## Failed payout

The payout of 2026-06-30, $18,132.40, failed and is not in the June bank figure. The payouts export shows it paid again in the 7 July payout. The bank figure was checked against the payouts export, payout by payout.

## Disputes

| Order | Amount | Fee |
|---|---|---|
| #45476 | 82.80 | 15.00 |
| #43139 | 202.09 | 15.00 |
| #42339 | 19.60 | 15.00 |
| #46132 | 99.94 | 15.00 |
| #48748 | 34.95 | 15.00 |
| #50960 | 85.00 | 15.00 |
| #46564 | 34.95 | 15.00 |
| #46016 | 85.96 | 15.00 |
| #47881 | 32.15 | 15.00 |
| #48462 | 191.89 | 15.00 |
| #43365 | 70.95 | 15.00 |
| #47863 | 71.86 | 15.00 |
| #42377 | 32.81 | 15.00 |
| #46314 | 52.58 | 15.00 |
| #43148 | 45.39 | 15.00 |
| #43258 | 70.01 | 15.00 |

---

The rest of the checked answer is too long for chat. It's saved in `files/reconciliation_2026-06.md` and covers:
- every order still in transit at month end, with its payout date;
- the orders paid outside Shopify Payments (PayPal, cash, bank deposit, manual payment or gift card), with their total — none of that money is in the payouts;
- orders paid partly by gift card;
- charges that don't match an order;
- orders charged after June ended;
- "How this was counted".

The file's last line is `Checked by shopify-month-end v0.10.1 · seal ef03bb75e1d3`.

**Questions for you:** the figures use the usual answer to each question until you confirm it. A different answer would change them.
- Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

---

*After this answer the plugin's own answer check ended the turn with:* Month-end check: the answer above did not pass the check against the computed results (against the checked answer: missing: '#55863' 93.66 (in the checked answer, not in this one); missing: '#55861' 306.22 (in the checked answer, not in this one); missing: '#55860' 79.63 (in the checked answer, not in this one); missing: '#55859' 95.28 (in the checked answer, not in this one); missing: '#55858' 81.47 (in the checked answer, not in this one); missing: '#55857' 94.47 (in the checked answer, not in this one); missing: '#55856' 72.74 (in the checked answer, not in this one); missing: '#55855' 63.54 (in the checked answer, not in this one)). Ask for the checked answer before using these figures.
