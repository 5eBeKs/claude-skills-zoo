<!-- numbers-0.5.2-claude-opus-5-5 / numbers-payouts-c / with the plugin / run 2: passed -->

Card orders in August came to £99,582.82, but Shopify Payments paid only £94,396.54 into the bank that month. That's a gap of **£5,186.28**. All of it is accounted for, with £0.00 left unexplained. Neither export has any days missing in August.

## Where the money went

| | | GBP |
|---|---|---:|
| | Card orders placed in August (Shopify Payments, shipped yet or not) | 99,582.82 |
| plus | Card charge on an order not counted as a sale: #33431, cancelled (refunded in full below) | 12.95 |
| minus | Refunds processed in August | 2,762.41 |
| | of which on orders from earlier months | 1,093.51 |
| minus | Card fees | 2,019.03 |
| minus | Disputes: amount and fees | 268.95 |
| plus | Other payout transactions (adjustment) | 2.35 |
| minus | Still in transit at month end | 6,075.32 |
| **equals** | **Paid out for August's card transactions** | **88,472.41** |
| plus | Paid out in August for earlier months' transactions | 5,924.13 |
| **equals** | **Paid out to the bank in August** (check this against your bank statement) | **94,396.54** |

- **Still in transit: £6,075.32.** This is the biggest item. It's the money from August's last sales (87 transactions), which pays out in early September. The money isn't lost, it just arrives later.
- **Refunds: £2,762.41.** £1,093.51 of this was refunds on orders from earlier months, taken out of August's payouts.
- **Card fees: £2,019.03.** These are the fees shown in the export. I checked that they add up, not that they match the rates in your Shopify Payments contract.
- **Disputes: £268.95.** There were three chargebacks: £223.95 in disputed amounts plus £45.00 in fees.

  | Order | Amount | Fee |
  |---|---:|---:|
  | #32603 | 41.95 | 15.00 |
  | #32955 | 116.00 | 15.00 |
  | #33706 | 66.00 | 15.00 |
- **Working the other way:** £5,924.13 of what reached the bank in August was for transactions from the end of July (93 of them). One adjustment added £2.35.

**Unmatched items:** there was only one. Order #33431 (£12.95) was cancelled, so it isn't counted as a sale. The card was still charged, and the refund for the same amount is in the refunds line. I kept both in the bridge instead of cancelling them out. No card order is missing its charge, and no charge differs from its order total.

**Money you won't find in the payout report:** £11,918.00. This comes from 180 August orders paid by PayPal or gift card, plus the gift-card part of 36 orders paid partly by gift card and partly by card. PayPal money goes to your PayPal account, and gift-card money was received when the gift card was sold. None of it is part of the gap.

## How this was counted
- Orders tagged "test" and orders paid through Shopify's test gateway are left out of sales. This is the answer in your `store_definitions.json`.
- The inputs were `orders_export.csv` (9,074 rows) and `payout_transactions.csv` (4,133 rows).
- I only checked these figures against the exports themselves. If you send a total from Shopify or the bank, I can check against that too.

## Question for you
The export's format hasn't been confirmed yet, and the figures above assume it's as expected. Are these the values you'd expect?
- **Payment methods:** Shopify Payments, PayPal Express Checkout, Gift card, Bogus Gateway (for testing)
- **Order statuses:** paid, partially_refunded, refunded, voided
- **Tags:** pre-order, test
- **Payout transaction types:** charge, refund, dispute, dispute_won, adjustment
- **Currency:** GBP only

If you confirm, I'll record this format so that anything new next month gets flagged. A different answer could change the figures.

The full write-up is in `files/reconciliation_2026-08.md`. It lists every order individually: the 87 transactions in transit with their payout dates, the 93 earlier transactions paid out in August, and all the PayPal, gift-card and split-payment orders.

<!-- the report this run saved next to the exports: reconciliation_2026-08.md -->

# Where August's card money went

**The gap: £5,186.28.** Card orders placed in August came to £99,582.82 (1,445 orders); Shopify Payments paid £94,396.54 to the bank in August. The bridge below closes to £0.00 unexplained: every pound of the gap is accounted for.

Before any figure: the exports cover all 31 of 31 days of August (orders) and 31 of 31 (payouts). Nothing is missing at either end. The figures use the export's shape as it stands; the one open question about it is below the bridge and is answered with the usual answer until you confirm it.

## The bridge

| | | GBP |
|---|---|---:|
| | Card orders placed in August (Shopify Payments, shipped yet or not) | 99,582.82 |
| plus | Card charge on an order not counted as a sale: #33431, cancelled (refunded in full below) | 12.95 |
| minus | Refunds processed in August | 2,762.41 |
| | of which on orders from earlier months | 1,093.51 |
| minus | Card fees | 2,019.03 |
| minus | Disputes: amount and fees | 268.95 |
| plus | Other payout transactions (adjustment) | 2.35 |
| minus | Still in transit at month end | 6,075.32 |
| **equals** | **Paid out for August's card transactions** | **88,472.41** |
| plus | Paid out in August for earlier months' transactions | 5,924.13 |
| **equals** | **Paid out to the bank in August** — check this against the bank statement | **94,396.54** |

Disputes: amount £223.95 plus fees £45.00.

## Where the money went, in words

- **Still in transit (£6,075.32).** The biggest single item. August's last sales were paid out in September; this is timing, not a loss.
- **Refunds (£2,762.41).** £1,093.51 of this was refunds on orders from earlier months, taken out of August's payouts.
- **Card fees (£2,019.03)** on August's charges. These are the fees in the export; this check confirms they add up, not that they match your contract rates.
- **Disputes (£268.95)**, three chargebacks, listed below.
- Working the other way: **£5,924.13** of what the bank got in August was for transactions from the end of July, paid out in early August, and one **adjustment** added £2.35.

## Disputes

| Order | Amount | Fee |
|---|---:|---:|
| #32603 | 41.95 | 15.00 |
| #32955 | 116.00 | 15.00 |
| #33706 | 66.00 | 15.00 |

## Unmatched items

- Card orders with no charge in payouts: none.
- Charges whose amount differs from the order: none.
- Charges with no counted order: #33431 (£12.95). The order was cancelled and refunded, so it is not counted as a sale, but the charge went through and the refund of the same amount is in the refunds line. It is shown as its own line in the bridge rather than netted away.

## Money that is not in Shopify Payments at all

180 August orders were paid by PayPal or gift card, and 36 more were paid partly by gift card. Together £11,918.00 was never going to appear in the payout report: PayPal money lands in your PayPal account, and gift-card money was received when the gift card was sold. None of it is part of the gap above.

## Lists

**Still in transit at 31 August, with payout dates (87 transactions):** #34375 (2026-09-01), #34376 (2026-09-01), #34377 (2026-09-01), #34378 (2026-09-01), #34380 (2026-09-01), #34381 (2026-09-01), #34382 (2026-09-01), #34383 (2026-09-01), #34384 (2026-09-01), #34385 (2026-09-01), #34387 (2026-09-01), #34388 (2026-09-01), #34389 (2026-09-01), #34390 (2026-09-01), #34391 (2026-09-01), #34392 (2026-09-01), #34393 (2026-09-01), #34394 (2026-09-01), #34395 (2026-09-01), #34396 (2026-09-01), #34397 (2026-09-01), #34398 (2026-09-01), #34399 (2026-09-01), #33031 (2026-09-01), #34401 (2026-09-01), #34402 (2026-09-01), #34403 (2026-09-01), #34404 (2026-09-01), #34407 (2026-09-01), #34408 (2026-09-01), #34409 (2026-09-01), #34410 (2026-09-01), #34411 (2026-09-01), #34412 (2026-09-01), #33385 (2026-09-01), #34413 (2026-09-01), #34414 (2026-09-01), #34415 (2026-09-01), #34416 (2026-09-01), #34417 (2026-09-01), #34418 (2026-09-01), #34419 (2026-09-01), #34420 (2026-09-01), #34421 (2026-09-01), #34422 (2026-09-02), #34423 (2026-09-02), #34424 (2026-09-02), #34425 (2026-09-02), #34426 (2026-09-02), #34427 (2026-09-02), #34428 (2026-09-02), #34429 (2026-09-02), #34430 (2026-09-02), #34432 (2026-09-02), #34433 (2026-09-02), #34434 (2026-09-02), #34435 (2026-09-02), #34436 (2026-09-02), #34438 (2026-09-02), #34439 (2026-09-02), #34440 (2026-09-02), #34441 (2026-09-02), #34442 (2026-09-02), #34443 (2026-09-02), #34444 (2026-09-02), #34445 (2026-09-02), #34446 (2026-09-02), #34447 (2026-09-02), #34448 (2026-09-02), #34449 (2026-09-02), #34450 (2026-09-02), #34451 (2026-09-02), #34453 (2026-09-02), #34454 (2026-09-02), #34455 (2026-09-02), #34457 (2026-09-02), #34458 (2026-09-02), #34459 (2026-09-02), #34461 (2026-09-02), #34462 (2026-09-02), #34463 (2026-09-02), #34464 (2026-09-02), #34465 (2026-09-02), #34467 (2026-09-02), #34468 (2026-09-02), #34469 (2026-09-02), #34470 (2026-09-02)

**Earlier months' transactions paid out in August (93):** #31800 (2026-08-03), #32737 (2026-08-03), #32738 (2026-08-03), #32739 (2026-08-03), #32740 (2026-08-03), #32741 (2026-08-03), #32742 (2026-08-03), #32743 (2026-08-03), #32744 (2026-08-03), #32745 (2026-08-03), #32746 (2026-08-03), #32747 (2026-08-03), #32748 (2026-08-03), #32700 (2026-08-03), #32749 (2026-08-03), #32750 (2026-08-03), #32751 (2026-08-03), #32752 (2026-08-03), #32753 (2026-08-03), #32754 (2026-08-03), #32755 (2026-08-03), #32757 (2026-08-03), #32758 (2026-08-03), #32759 (2026-08-03), #32760 (2026-08-03), #31818 (2026-08-03), #32109 (2026-08-03), #31692 (2026-08-03), #32227 (2026-08-03), #32764 (2026-08-03), #32765 (2026-08-03), #32766 (2026-08-03), #32767 (2026-08-03), #32768 (2026-08-03), #32770 (2026-08-03), #32771 (2026-08-03), #32772 (2026-08-03), #32773 (2026-08-03), #32774 (2026-08-03), #32775 (2026-08-03), #32776 (2026-08-03), #32777 (2026-08-03), #32778 (2026-08-03), #32779 (2026-08-03), #32780 (2026-08-03), #32782 (2026-08-03), #32783 (2026-08-03), #32784 (2026-08-03), #32785 (2026-08-03), #32086 (2026-08-03), #32786 (2026-08-03), #32787 (2026-08-03), #32788 (2026-08-03), #32789 (2026-08-03), #32790 (2026-08-03), #32791 (2026-08-03), #32792 (2026-08-03), #32793 (2026-08-03), #32794 (2026-08-03), #32795 (2026-08-03), #32796 (2026-08-03), #32797 (2026-08-03), #32798 (2026-08-03), #32800 (2026-08-03), #32801 (2026-08-03), #32802 (2026-08-03), #32803 (2026-08-03), #32804 (2026-08-03), #32805 (2026-08-03), #32806 (2026-08-03), #32807 (2026-08-03), #32808 (2026-08-03), #32809 (2026-08-03), #32810 (2026-08-03), #32811 (2026-08-03), #32813 (2026-08-03), #32814 (2026-08-03), #32816 (2026-08-03), #32817 (2026-08-03), #32818 (2026-08-03), #32819 (2026-08-03), #32820 (2026-08-03), #32821 (2026-08-03), #32822 (2026-08-03), #32823 (2026-08-03), #32824 (2026-08-03), #32825 (2026-08-03), #32536 (2026-08-03), #32826 (2026-08-03), #32827 (2026-08-03), #32828 (2026-08-03), #32829 (2026-08-03), #32830 (2026-08-03)

**Paid outside Shopify Payments (180):** #32832 (PayPal Express Checkout), #32838 (PayPal Express Checkout), #32848 (PayPal Express Checkout), #32866 (PayPal Express Checkout), #32876 (Gift card), #32888 (PayPal Express Checkout), #32893 (PayPal Express Checkout), #32895 (PayPal Express Checkout), #32923 (PayPal Express Checkout), #32936 (Gift card), #32947 (PayPal Express Checkout), #32986 (PayPal Express Checkout), #32991 (PayPal Express Checkout), #32999 (Gift card), #33013 (PayPal Express Checkout), #33014 (PayPal Express Checkout), #33020 (PayPal Express Checkout), #33029 (Gift card), #33044 (PayPal Express Checkout), #33048 (Gift card), #33064 (PayPal Express Checkout), #33068 (PayPal Express Checkout), #33077 (PayPal Express Checkout), #33083 (Gift card), #33088 (Gift card), #33116 (PayPal Express Checkout), #33122 (PayPal Express Checkout), #33123 (PayPal Express Checkout), #33134 (Gift card), #33139 (PayPal Express Checkout), #33144 (Gift card), #33149 (PayPal Express Checkout), #33186 (PayPal Express Checkout), #33206 (PayPal Express Checkout), #33207 (PayPal Express Checkout), #33209 (Gift card), #33213 (Gift card), #33228 (PayPal Express Checkout), #33231 (PayPal Express Checkout), #33238 (Gift card), #33249 (PayPal Express Checkout), #33252 (PayPal Express Checkout), #33277 (PayPal Express Checkout), #33295 (PayPal Express Checkout), #33296 (Gift card), #33314 (Gift card), #33316 (Gift card), #33320 (Gift card), #33340 (Gift card), #33368 (PayPal Express Checkout), #33373 (PayPal Express Checkout), #33391 (PayPal Express Checkout), #33394 (PayPal Express Checkout), #33413 (PayPal Express Checkout), #33421 (PayPal Express Checkout), #33423 (PayPal Express Checkout), #33425 (Gift card), #33439 (PayPal Express Checkout), #33444 (PayPal Express Checkout), #33461 (PayPal Express Checkout), #33468 (PayPal Express Checkout), #33482 (PayPal Express Checkout), #33484 (PayPal Express Checkout), #33497 (PayPal Express Checkout), #33506 (Gift card), #33507 (PayPal Express Checkout), #33522 (Gift card), #33523 (Gift card), #33540 (PayPal Express Checkout), #33545 (PayPal Express Checkout), #33564 (PayPal Express Checkout), #33567 (PayPal Express Checkout), #33568 (PayPal Express Checkout), #33582 (PayPal Express Checkout), #33585 (PayPal Express Checkout), #33595 (PayPal Express Checkout), #33610 (PayPal Express Checkout), #33622 (Gift card), #33641 (PayPal Express Checkout), #33660 (PayPal Express Checkout), #33663 (PayPal Express Checkout), #33675 (PayPal Express Checkout), #33683 (PayPal Express Checkout), #33687 (PayPal Express Checkout), #33694 (PayPal Express Checkout), #33701 (PayPal Express Checkout), #33705 (Gift card), #33711 (PayPal Express Checkout), #33713 (PayPal Express Checkout), #33723 (PayPal Express Checkout), #33725 (PayPal Express Checkout), #33728 (PayPal Express Checkout), #33733 (PayPal Express Checkout), #33738 (PayPal Express Checkout), #33739 (Gift card), #33762 (Gift card), #33766 (PayPal Express Checkout), #33804 (PayPal Express Checkout), #33810 (PayPal Express Checkout), #33820 (PayPal Express Checkout), #33824 (PayPal Express Checkout), #33828 (Gift card), #33831 (PayPal Express Checkout), #33832 (Gift card), #33838 (PayPal Express Checkout), #33853 (PayPal Express Checkout), #33854 (PayPal Express Checkout), #33859 (Gift card), #33867 (PayPal Express Checkout), #33884 (PayPal Express Checkout), #33901 (PayPal Express Checkout), #33914 (PayPal Express Checkout), #33928 (Gift card), #33931 (PayPal Express Checkout), #33933 (PayPal Express Checkout), #33940 (PayPal Express Checkout), #33942 (PayPal Express Checkout), #33944 (PayPal Express Checkout), #33958 (PayPal Express Checkout), #33977 (PayPal Express Checkout), #33986 (PayPal Express Checkout), #34006 (PayPal Express Checkout), #34008 (Gift card), #34012 (PayPal Express Checkout), #34017 (Gift card), #34027 (Gift card), #34040 (Gift card), #34046 (Gift card), #34050 (PayPal Express Checkout), #34057 (PayPal Express Checkout), #34077 (PayPal Express Checkout), #34080 (PayPal Express Checkout), #34082 (Gift card), #34121 (Gift card), #34125 (PayPal Express Checkout), #34126 (Gift card), #34129 (PayPal Express Checkout), #34134 (PayPal Express Checkout), #34142 (PayPal Express Checkout), #34163 (PayPal Express Checkout), #34173 (PayPal Express Checkout), #34178 (PayPal Express Checkout), #34207 (Gift card), #34217 (PayPal Express Checkout), #34219 (Gift card), #34234 (PayPal Express Checkout), #34238 (PayPal Express Checkout), #34239 (PayPal Express Checkout), #34244 (PayPal Express Checkout), #34245 (PayPal Express Checkout), #34247 (PayPal Express Checkout), #34251 (Gift card), #34256 (PayPal Express Checkout), #34259 (Gift card), #34267 (PayPal Express Checkout), #34271 (PayPal Express Checkout), #34282 (PayPal Express Checkout), #34299 (PayPal Express Checkout), #34301 (PayPal Express Checkout), #34310 (PayPal Express Checkout), #34313 (PayPal Express Checkout), #34317 (Gift card), #34326 (PayPal Express Checkout), #34330 (Gift card), #34334 (PayPal Express Checkout), #34348 (Gift card), #34351 (PayPal Express Checkout), #34354 (PayPal Express Checkout), #34361 (Gift card), #34366 (PayPal Express Checkout), #34379 (Gift card), #34386 (PayPal Express Checkout), #34400 (Gift card), #34405 (PayPal Express Checkout), #34431 (PayPal Express Checkout), #34437 (PayPal Express Checkout), #34452 (PayPal Express Checkout), #34456 (PayPal Express Checkout), #34460 (PayPal Express Checkout), #34466 (Gift card)

**Split payments, gift card part not in payouts (36):** #32938 (Gift card, Shopify Payments), #33006 (Gift card, Shopify Payments), #33043 (Gift card, Shopify Payments), #33056 (Gift card, Shopify Payments), #33074 (Gift card, Shopify Payments), #33099 (Gift card, Shopify Payments), #33135 (Gift card, Shopify Payments), #33162 (Gift card, Shopify Payments), #33182 (Gift card, Shopify Payments), #33197 (Gift card, Shopify Payments), #33217 (Gift card, Shopify Payments), #33262 (Gift card, Shopify Payments), #33326 (Gift card, Shopify Payments), #33392 (Gift card, Shopify Payments), #33437 (Gift card, Shopify Payments), #33441 (Gift card, Shopify Payments), #33465 (Gift card, Shopify Payments), #33478 (Gift card, Shopify Payments), #33538 (Gift card, Shopify Payments), #33539 (Gift card, Shopify Payments), #33633 (Gift card, Shopify Payments), #33647 (Gift card, Shopify Payments), #33669 (Gift card, Shopify Payments), #33670 (Gift card, Shopify Payments), #33674 (Gift card, Shopify Payments), #33719 (Gift card, Shopify Payments), #33760 (Gift card, Shopify Payments), #33905 (Gift card, Shopify Payments), #33993 (Gift card, Shopify Payments), #34010 (Gift card, Shopify Payments), #34024 (Gift card, Shopify Payments), #34048 (Gift card, Shopify Payments), #34053 (Gift card, Shopify Payments), #34084 (Gift card, Shopify Payments), #34213 (Gift card, Shopify Payments), #34220 (Gift card, Shopify Payments)

## How this was counted

- orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (your answer)

What it was computed from and checked against:

- the orders export has records on 31 of 31 days of August 2026
- the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: GBP; payment method: Bogus Gateway (for testing), Gift card, PayPal Express Checkout, Shopify Payments; tags: pre-order, test)
- the payout export has records on 31 of 31 days of August 2026
- the payout export's shape is not recorded yet (type: adjustment, charge, dispute, dispute_won, refund; payout status: in_transit, paid; currency: GBP)
- checked against nothing outside the export: give a figure from Shopify or the bank to check it

- orders_export.csv: 9,074 rows, SHA-256 3035dcb90b8edd7c
- payout_transactions.csv: 4,133 rows, SHA-256 2bf625390cc8ebe1
- store_definitions.json: 36 rows, SHA-256 c370f6ea8162b60d
- computed by shopify-month-end v0.5.2, scripts 05e46938ecfc

## Question for you

The figures above use the usual answer to this until you confirm it; a different answer can change them.

- The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.

