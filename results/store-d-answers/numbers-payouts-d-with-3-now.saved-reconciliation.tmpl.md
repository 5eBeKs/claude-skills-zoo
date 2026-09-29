# Shopify Payments payout reconciliation: June 2026

**Warning, read first:**

{{warnings|bullets}}

## The gap

Card orders placed in June came to {{currency|symbol}}{{bridge.card_orders_total|money}}. Shopify paid {{currency|symbol}}{{bridge.paid_out_in_month|money}} to the bank in June. The gap is {{currency|symbol}}{{totals_owners_ask_about.gap_card_sales_to_paid_out|money}}. The bridge below closes: the unexplained difference is {{currency|symbol}}{{bridge.unexplained_difference|money}}.

## Bridge

| | {{currency}} |
|---|---:|
| Card orders placed in June (Shopify Payments, shipped yet or not) | {{bridge.card_orders_total|money}} |
| − Refunds processed in June | {{bridge.refunds|money}} |
| &nbsp;&nbsp;of which on orders from earlier months | {{bridge.refunds_on_earlier_orders|money}} |
| − Card fees | {{bridge.card_fees|money}} |
| − Disputes: amount and fees | {{bridge.disputes_amount|money}} + {{bridge.dispute_fees|money}} |
| Reserve held (-) or released (+) by Shopify | {{bridge.reserve_net|money}} (still held at month end: {{bridge.reserve_held|money}}) |
| Failed payout paid again | {{bridge.failed_payouts_paid_again|money}} |
| Shopify adjustments | {{bridge.adjustments|money}} |
| − Still in transit at month end | {{bridge.in_transit_at_month_end|money}} |
| **= Paid out for June's card transactions** | **{{bridge.paid_out_for_this_months_sales|money}}** |
| + Paid out in June for transactions before the transactions export starts | {{bridge.paid_out_before_transactions_export|money}} |
| **= Paid out to the bank in June** | **{{bridge.paid_out_in_month|money}}** |

The last line is the figure to check against the bank statement.

The disputes' net cost is {{currency|symbol}}{{totals_owners_ask_about.dispute_total_cost|money}}.

Payouts in early June that carry transactions from before the transactions export starts (June 1):

| Payout date | Payout total | In transactions export | Before it |
|---|---:|---:|---:|
| {{payouts_short_of_transactions.0.payout_date}} | {{payouts_short_of_transactions.0.payout_total|money}} | {{payouts_short_of_transactions.0.in_transactions_export|money}} | {{payouts_short_of_transactions.0.not_in_it|money}} |
| {{payouts_short_of_transactions.1.payout_date}} | {{payouts_short_of_transactions.1.payout_total|money}} | {{payouts_short_of_transactions.1.in_transactions_export|money}} | {{payouts_short_of_transactions.1.not_in_it|money}} |
| {{payouts_short_of_transactions.2.payout_date}} | {{payouts_short_of_transactions.2.payout_total|money}} | {{payouts_short_of_transactions.2.in_transactions_export|money}} | {{payouts_short_of_transactions.2.not_in_it|money}} |
| {{payouts_short_of_transactions.3.payout_date}} | {{payouts_short_of_transactions.3.payout_total|money}} | {{payouts_short_of_transactions.3.in_transactions_export|money}} | {{payouts_short_of_transactions.3.not_in_it|money}} |

## Disputes

| Order | Amount | Fee |
|---|---:|---:|
| {{disputes.0.order}} | {{disputes.0.amount|money}} | {{disputes.0.fee|money}} |
| {{disputes.1.order}} | {{disputes.1.amount|money}} | {{disputes.1.fee|money}} |
| {{disputes.2.order}} | {{disputes.2.amount|money}} | {{disputes.2.fee|money}} |
| {{disputes.3.order}} | {{disputes.3.amount|money}} | {{disputes.3.fee|money}} |
| {{disputes.4.order}} | {{disputes.4.amount|money}} | {{disputes.4.fee|money}} |
| {{disputes.5.order}} | {{disputes.5.amount|money}} | {{disputes.5.fee|money}} |
| {{disputes.6.order}} | {{disputes.6.amount|money}} | {{disputes.6.fee|money}} |
| {{disputes.7.order}} | {{disputes.7.amount|money}} | {{disputes.7.fee|money}} |
| {{disputes.8.order}} | {{disputes.8.amount|money}} | {{disputes.8.fee|money}} |
| {{disputes.9.order}} | {{disputes.9.amount|money}} | {{disputes.9.fee|money}} |
| {{disputes.10.order}} | {{disputes.10.amount|money}} | {{disputes.10.fee|money}} |
| {{disputes.11.order}} | {{disputes.11.amount|money}} | {{disputes.11.fee|money}} |
| {{disputes.12.order}} | {{disputes.12.amount|money}} | {{disputes.12.fee|money}} |
| {{disputes.13.order}} | {{disputes.13.amount|money}} | {{disputes.13.fee|money}} |
| {{disputes.14.order}} | {{disputes.14.amount|money}} | {{disputes.14.fee|money}} |
| {{disputes.15.order}} | {{disputes.15.amount|money}} | {{disputes.15.fee|money}} |

## Failed payout

- Payout of {{failed_payouts.0.payout_date}}: {{currency|symbol}}{{failed_payouts.0.total|money}} failed and was not paid again in June (failed payout paid again: {{currency|symbol}}{{bridge.failed_payouts_paid_again|money}}).

The bank figure was checked against the payouts export (bank checked: {{bank_checked}}).

## Paid outside Shopify Payments (not in payouts at all)

These orders were paid through PayPal, manual, bank deposit, cash, gift card and similar methods, so this money never appears in the Shopify payouts. They total {{currency|symbol}}{{totals_owners_ask_about.paid_outside_shopify_payments|money}}:

{{orders_paid_outside_shopify_payments|list}}

## Split payments (gift card + card)

Only the card part reaches the payouts:

| Order | Order total | Card part | Other part |
|---|---:|---:|---:|
| {{split_payments.0.order}} | {{split_payments.0.order_total|money}} | {{split_payments.0.card_part|money}} | {{split_payments.0.other_part|money}} |
| {{split_payments.1.order}} | {{split_payments.1.order_total|money}} | {{split_payments.1.card_part|money}} | {{split_payments.1.other_part|money}} |
| {{split_payments.2.order}} | {{split_payments.2.order_total|money}} | {{split_payments.2.card_part|money}} | {{split_payments.2.other_part|money}} |
| {{split_payments.3.order}} | {{split_payments.3.order_total|money}} | {{split_payments.3.card_part|money}} | {{split_payments.3.other_part|money}} |
| {{split_payments.4.order}} | {{split_payments.4.order_total|money}} | {{split_payments.4.card_part|money}} | {{split_payments.4.other_part|money}} |
| {{split_payments.5.order}} | {{split_payments.5.order_total|money}} | {{split_payments.5.card_part|money}} | {{split_payments.5.other_part|money}} |
| {{split_payments.6.order}} | {{split_payments.6.order_total|money}} | {{split_payments.6.card_part|money}} | {{split_payments.6.other_part|money}} |
| {{split_payments.7.order}} | {{split_payments.7.order_total|money}} | {{split_payments.7.card_part|money}} | {{split_payments.7.other_part|money}} |
| {{split_payments.8.order}} | {{split_payments.8.order_total|money}} | {{split_payments.8.card_part|money}} | {{split_payments.8.other_part|money}} |
| {{split_payments.9.order}} | {{split_payments.9.order_total|money}} | {{split_payments.9.card_part|money}} | {{split_payments.9.other_part|money}} |
| {{split_payments.10.order}} | {{split_payments.10.order_total|money}} | {{split_payments.10.card_part|money}} | {{split_payments.10.other_part|money}} |
| {{split_payments.11.order}} | {{split_payments.11.order_total|money}} | {{split_payments.11.card_part|money}} | {{split_payments.11.other_part|money}} |
| {{split_payments.12.order}} | {{split_payments.12.order_total|money}} | {{split_payments.12.card_part|money}} | {{split_payments.12.other_part|money}} |
| {{split_payments.13.order}} | {{split_payments.13.order_total|money}} | {{split_payments.13.card_part|money}} | {{split_payments.13.other_part|money}} |
| {{split_payments.14.order}} | {{split_payments.14.order_total|money}} | {{split_payments.14.card_part|money}} | {{split_payments.14.other_part|money}} |
| {{split_payments.15.order}} | {{split_payments.15.order_total|money}} | {{split_payments.15.card_part|money}} | {{split_payments.15.other_part|money}} |
| {{split_payments.16.order}} | {{split_payments.16.order_total|money}} | {{split_payments.16.card_part|money}} | {{split_payments.16.other_part|money}} |
| {{split_payments.17.order}} | {{split_payments.17.order_total|money}} | {{split_payments.17.card_part|money}} | {{split_payments.17.other_part|money}} |
| {{split_payments.18.order}} | {{split_payments.18.order_total|money}} | {{split_payments.18.card_part|money}} | {{split_payments.18.other_part|money}} |
| {{split_payments.19.order}} | {{split_payments.19.order_total|money}} | {{split_payments.19.card_part|money}} | {{split_payments.19.other_part|money}} |
| {{split_payments.20.order}} | {{split_payments.20.order_total|money}} | {{split_payments.20.card_part|money}} | {{split_payments.20.other_part|money}} |
| {{split_payments.21.order}} | {{split_payments.21.order_total|money}} | {{split_payments.21.card_part|money}} | {{split_payments.21.other_part|money}} |
| {{split_payments.22.order}} | {{split_payments.22.order_total|money}} | {{split_payments.22.card_part|money}} | {{split_payments.22.other_part|money}} |
| {{split_payments.23.order}} | {{split_payments.23.order_total|money}} | {{split_payments.23.card_part|money}} | {{split_payments.23.other_part|money}} |
| {{split_payments.24.order}} | {{split_payments.24.order_total|money}} | {{split_payments.24.card_part|money}} | {{split_payments.24.other_part|money}} |
| {{split_payments.25.order}} | {{split_payments.25.order_total|money}} | {{split_payments.25.card_part|money}} | {{split_payments.25.other_part|money}} |
| {{split_payments.26.order}} | {{split_payments.26.order_total|money}} | {{split_payments.26.card_part|money}} | {{split_payments.26.other_part|money}} |
| {{split_payments.27.order}} | {{split_payments.27.order_total|money}} | {{split_payments.27.card_part|money}} | {{split_payments.27.other_part|money}} |
| {{split_payments.28.order}} | {{split_payments.28.order_total|money}} | {{split_payments.28.card_part|money}} | {{split_payments.28.other_part|money}} |
| {{split_payments.29.order}} | {{split_payments.29.order_total|money}} | {{split_payments.29.card_part|money}} | {{split_payments.29.other_part|money}} |
| {{split_payments.30.order}} | {{split_payments.30.order_total|money}} | {{split_payments.30.card_part|money}} | {{split_payments.30.other_part|money}} |
| {{split_payments.31.order}} | {{split_payments.31.order_total|money}} | {{split_payments.31.card_part|money}} | {{split_payments.31.other_part|money}} |
| {{split_payments.32.order}} | {{split_payments.32.order_total|money}} | {{split_payments.32.card_part|money}} | {{split_payments.32.other_part|money}} |
| {{split_payments.33.order}} | {{split_payments.33.order_total|money}} | {{split_payments.33.card_part|money}} | {{split_payments.33.other_part|money}} |
| {{split_payments.34.order}} | {{split_payments.34.order_total|money}} | {{split_payments.34.card_part|money}} | {{split_payments.34.other_part|money}} |
| {{split_payments.35.order}} | {{split_payments.35.order_total|money}} | {{split_payments.35.card_part|money}} | {{split_payments.35.other_part|money}} |
| {{split_payments.36.order}} | {{split_payments.36.order_total|money}} | {{split_payments.36.card_part|money}} | {{split_payments.36.other_part|money}} |
| {{split_payments.37.order}} | {{split_payments.37.order_total|money}} | {{split_payments.37.card_part|money}} | {{split_payments.37.other_part|money}} |
| {{split_payments.38.order}} | {{split_payments.38.order_total|money}} | {{split_payments.38.card_part|money}} | {{split_payments.38.other_part|money}} |
| {{split_payments.39.order}} | {{split_payments.39.order_total|money}} | {{split_payments.39.card_part|money}} | {{split_payments.39.other_part|money}} |
| {{split_payments.40.order}} | {{split_payments.40.order_total|money}} | {{split_payments.40.card_part|money}} | {{split_payments.40.other_part|money}} |
| {{split_payments.41.order}} | {{split_payments.41.order_total|money}} | {{split_payments.41.card_part|money}} | {{split_payments.41.other_part|money}} |
| {{split_payments.42.order}} | {{split_payments.42.order_total|money}} | {{split_payments.42.card_part|money}} | {{split_payments.42.other_part|money}} |
| {{split_payments.43.order}} | {{split_payments.43.order_total|money}} | {{split_payments.43.card_part|money}} | {{split_payments.43.other_part|money}} |
| {{split_payments.44.order}} | {{split_payments.44.order_total|money}} | {{split_payments.44.card_part|money}} | {{split_payments.44.other_part|money}} |
| {{split_payments.45.order}} | {{split_payments.45.order_total|money}} | {{split_payments.45.card_part|money}} | {{split_payments.45.other_part|money}} |
| {{split_payments.46.order}} | {{split_payments.46.order_total|money}} | {{split_payments.46.card_part|money}} | {{split_payments.46.other_part|money}} |
| {{split_payments.47.order}} | {{split_payments.47.order_total|money}} | {{split_payments.47.card_part|money}} | {{split_payments.47.other_part|money}} |
| {{split_payments.48.order}} | {{split_payments.48.order_total|money}} | {{split_payments.48.card_part|money}} | {{split_payments.48.other_part|money}} |
| {{split_payments.49.order}} | {{split_payments.49.order_total|money}} | {{split_payments.49.card_part|money}} | {{split_payments.49.other_part|money}} |
| {{split_payments.50.order}} | {{split_payments.50.order_total|money}} | {{split_payments.50.card_part|money}} | {{split_payments.50.other_part|money}} |
| {{split_payments.51.order}} | {{split_payments.51.order_total|money}} | {{split_payments.51.card_part|money}} | {{split_payments.51.other_part|money}} |
| {{split_payments.52.order}} | {{split_payments.52.order_total|money}} | {{split_payments.52.card_part|money}} | {{split_payments.52.other_part|money}} |
| {{split_payments.53.order}} | {{split_payments.53.order_total|money}} | {{split_payments.53.card_part|money}} | {{split_payments.53.other_part|money}} |
| {{split_payments.54.order}} | {{split_payments.54.order_total|money}} | {{split_payments.54.card_part|money}} | {{split_payments.54.other_part|money}} |
| {{split_payments.55.order}} | {{split_payments.55.order_total|money}} | {{split_payments.55.card_part|money}} | {{split_payments.55.other_part|money}} |
| {{split_payments.56.order}} | {{split_payments.56.order_total|money}} | {{split_payments.56.card_part|money}} | {{split_payments.56.other_part|money}} |
| {{split_payments.57.order}} | {{split_payments.57.order_total|money}} | {{split_payments.57.card_part|money}} | {{split_payments.57.other_part|money}} |
| {{split_payments.58.order}} | {{split_payments.58.order_total|money}} | {{split_payments.58.card_part|money}} | {{split_payments.58.other_part|money}} |
| {{split_payments.59.order}} | {{split_payments.59.order_total|money}} | {{split_payments.59.card_part|money}} | {{split_payments.59.other_part|money}} |
| {{split_payments.60.order}} | {{split_payments.60.order_total|money}} | {{split_payments.60.card_part|money}} | {{split_payments.60.other_part|money}} |
| {{split_payments.61.order}} | {{split_payments.61.order_total|money}} | {{split_payments.61.card_part|money}} | {{split_payments.61.other_part|money}} |
| {{split_payments.62.order}} | {{split_payments.62.order_total|money}} | {{split_payments.62.card_part|money}} | {{split_payments.62.other_part|money}} |
| {{split_payments.63.order}} | {{split_payments.63.order_total|money}} | {{split_payments.63.card_part|money}} | {{split_payments.63.other_part|money}} |
| {{split_payments.64.order}} | {{split_payments.64.order_total|money}} | {{split_payments.64.card_part|money}} | {{split_payments.64.other_part|money}} |
| {{split_payments.65.order}} | {{split_payments.65.order_total|money}} | {{split_payments.65.card_part|money}} | {{split_payments.65.other_part|money}} |
| {{split_payments.66.order}} | {{split_payments.66.order_total|money}} | {{split_payments.66.card_part|money}} | {{split_payments.66.other_part|money}} |
| {{split_payments.67.order}} | {{split_payments.67.order_total|money}} | {{split_payments.67.card_part|money}} | {{split_payments.67.other_part|money}} |
| {{split_payments.68.order}} | {{split_payments.68.order_total|money}} | {{split_payments.68.card_part|money}} | {{split_payments.68.other_part|money}} |
| {{split_payments.69.order}} | {{split_payments.69.order_total|money}} | {{split_payments.69.card_part|money}} | {{split_payments.69.other_part|money}} |
| {{split_payments.70.order}} | {{split_payments.70.order_total|money}} | {{split_payments.70.card_part|money}} | {{split_payments.70.other_part|money}} |
| {{split_payments.71.order}} | {{split_payments.71.order_total|money}} | {{split_payments.71.card_part|money}} | {{split_payments.71.other_part|money}} |
| {{split_payments.72.order}} | {{split_payments.72.order_total|money}} | {{split_payments.72.card_part|money}} | {{split_payments.72.other_part|money}} |
| {{split_payments.73.order}} | {{split_payments.73.order_total|money}} | {{split_payments.73.card_part|money}} | {{split_payments.73.other_part|money}} |
| {{split_payments.74.order}} | {{split_payments.74.order_total|money}} | {{split_payments.74.card_part|money}} | {{split_payments.74.other_part|money}} |
| {{split_payments.75.order}} | {{split_payments.75.order_total|money}} | {{split_payments.75.card_part|money}} | {{split_payments.75.other_part|money}} |
| {{split_payments.76.order}} | {{split_payments.76.order_total|money}} | {{split_payments.76.card_part|money}} | {{split_payments.76.other_part|money}} |
| {{split_payments.77.order}} | {{split_payments.77.order_total|money}} | {{split_payments.77.card_part|money}} | {{split_payments.77.other_part|money}} |
| {{split_payments.78.order}} | {{split_payments.78.order_total|money}} | {{split_payments.78.card_part|money}} | {{split_payments.78.other_part|money}} |
| {{split_payments.79.order}} | {{split_payments.79.order_total|money}} | {{split_payments.79.card_part|money}} | {{split_payments.79.other_part|money}} |
| {{split_payments.80.order}} | {{split_payments.80.order_total|money}} | {{split_payments.80.card_part|money}} | {{split_payments.80.other_part|money}} |
| {{split_payments.81.order}} | {{split_payments.81.order_total|money}} | {{split_payments.81.card_part|money}} | {{split_payments.81.other_part|money}} |
| {{split_payments.82.order}} | {{split_payments.82.order_total|money}} | {{split_payments.82.card_part|money}} | {{split_payments.82.other_part|money}} |
| {{split_payments.83.order}} | {{split_payments.83.order_total|money}} | {{split_payments.83.card_part|money}} | {{split_payments.83.other_part|money}} |
| {{split_payments.84.order}} | {{split_payments.84.order_total|money}} | {{split_payments.84.card_part|money}} | {{split_payments.84.other_part|money}} |
| {{split_payments.85.order}} | {{split_payments.85.order_total|money}} | {{split_payments.85.card_part|money}} | {{split_payments.85.other_part|money}} |
| {{split_payments.86.order}} | {{split_payments.86.order_total|money}} | {{split_payments.86.card_part|money}} | {{split_payments.86.other_part|money}} |

## Still in transit at month end

These were paid out in July, with the payout dates shown:

{{in_transit|list}}

## Unmatched items

Charged after the month ended (charged in July):

| Order | Order total | Charged in June | Charged after month end | Date |
|---|---:|---:|---:|---|
| {{charged_after_month_end.0.order}} | {{charged_after_month_end.0.order_total|money}} | {{charged_after_month_end.0.charged_in_month|money}} | {{charged_after_month_end.0.charged_after_month_end|money}} | {{charged_after_month_end.0.date}} |
| {{charged_after_month_end.1.order}} | {{charged_after_month_end.1.order_total|money}} | {{charged_after_month_end.1.charged_in_month|money}} | {{charged_after_month_end.1.charged_after_month_end|money}} | {{charged_after_month_end.1.date}} |
| {{charged_after_month_end.2.order}} | {{charged_after_month_end.2.order_total|money}} | {{charged_after_month_end.2.charged_in_month|money}} | {{charged_after_month_end.2.charged_after_month_end|money}} | {{charged_after_month_end.2.date}} |
| {{charged_after_month_end.3.order}} | {{charged_after_month_end.3.order_total|money}} | {{charged_after_month_end.3.charged_in_month|money}} | {{charged_after_month_end.3.charged_after_month_end|money}} | {{charged_after_month_end.3.date}} |
| {{charged_after_month_end.4.order}} | {{charged_after_month_end.4.order_total|money}} | {{charged_after_month_end.4.charged_in_month|money}} | {{charged_after_month_end.4.charged_after_month_end|money}} | {{charged_after_month_end.4.date}} |

Charges with no counted June order:

{{charges_without_counted_order|list}}

Charge amount differs from order total:

{{charge_amount_mismatch|list}}

## How this was counted

{{definitions_in_words|bullets}}

{{export_in_words|bullets}}

{{fingerprints_in_words|bullets}}

## Open questions for you

The figures above use the usual answer until you confirm it. A different answer changes them.

{{open_questions|bullets}}
