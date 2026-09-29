<!-- Cowork in claude.ai (September 2026), the plugin 0.11.7 uploaded as a ZIP, Opus 5.5 High, store A's orders_export.csv and payout_transactions.csv attached. Question: "We sold way more in August than landed in our bank. The Shopify orders export and the Shopify Payments payout transactions export are attached. Where did the money go?" The skill fired on its own; the session shows "Created a file, shared a file, ran 3 commands". A first attempt, before the account's older copies of the three Shopify skills (uploaded one by one the day before, v0.10.1) were turned off, loaded the old payout-reconciliation instead of the plugin's: with two copies of a skill, Cowork does not always take the newer one. Copied from the page as text, so Markdown formatting is lost. -->

Where August's money went

Gap: €371.08 between card orders placed in August and what Shopify Payments paid out to your bank in August. Nothing is missing: the bridge below closes to €0.00 unexplained.

Before the figures:

The bank figure is not checked: the transactions export starts on 2026-08-01 and the payouts export was not given.
The bridge
EUR
Card orders placed in August (Shopify Payments, shipped yet or not) 2,819.82
− Refunds processed in August 70.50
− Card fees 56.59
− Disputes: amount and fees 19.30 + 15.00
− Still in transit at month end 209.69
= Paid out for August's card transactions 2,448.74
= Paid out to the bank in August 2,448.74

That last line is the figure to find on your bank statement.

What each piece is

Refunds. Two refunds went back to customers during the month, both on August orders.

Card fees. Shopify Payments takes its processing fee from every charge before paying out. This is the single biggest steady cost in the gap.

The dispute. A customer disputed order #1060 with their bank: the €19.30 sale was pulled back and Shopify charged a €15.00 dispute fee on top, so it cost you €34.30 in all. If you have proof of delivery, it may be worth answering it in Shopify (Orders > the order > Dispute): a won dispute returns the amount.

Still in transit. Orders from the last days of August were paid out in the first days of September, so they belong to September's bank statement, not August's:

#1050 (2026-09-01), #1059 (2026-09-01), #1009 (2026-09-02), #1058 (2026-09-02)

Not in the payouts at all

This order was paid through PayPal, so its money went to your PayPal account, not through Shopify Payments; don't look for it on the payout report:

#1055 (PayPal Express Checkout)

Also left out of the card sales: the order that was voided (never charged) and an order tagged "test". Every other counted card order (57 in all) matched a charge of the same amount; nothing is unmatched.

How this was counted
orders tagged 'test' and orders paid through Shopify's test gateway are left out of sales (the usual answer; please confirm)
the orders export has records on 25 of 31 days of August 2026
the orders export's shape is not recorded yet (financial status: paid, partially_refunded, refunded, voided; fulfillment status: fulfilled, unfulfilled; currency: EUR; payment method: PayPal Express Checkout, Shopify Payments; tags: test)
the payout export has records on 26 of 31 days of August 2026
the payout export's shape is not recorded yet (type: charge, dispute, refund; payout status: in_transit, paid; currency: EUR)
the transactions export starts on 2026-08-01: payouts early in August 2026 may carry earlier transactions it does not have, so the bank figure is not checked; add the payouts export (Finances > Payouts > Export)
checked against nothing outside the export: give a figure from Shopify or the bank to check it
orders_export.csv: 103 rows, SHA-256 b3f1fd5c8f24954c
payout_transactions.csv: 60 rows, SHA-256 695fdc5736fef3b7
computed by shopify-month-end v0.11.7, scripts 6e9e71a410d0
Questions for you

The figures above use the usual answer to each of these until you confirm it; a different answer changes them.

Test orders (tagged 'test', or paid through Shopify's test gateway): leave them out of sales (usual), or count them?
The export's shape is not recorded yet: are the payment methods, statuses, tags and currencies listed under "How this was counted" all as expected? If so, they are kept as store_shape.json, and a new one next month is flagged.
The transactions export starts on 2026-08-01, so the payouts of the first days of August 2026 may be short of what the bank received. Can you add the payouts export (Finances > Payouts > Export) to check the bank figure?

Checked by payout-reconciliation v0.11.7 · seal accdf6b2634b
