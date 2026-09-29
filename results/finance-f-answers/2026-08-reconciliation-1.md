<!-- Cowork in claude.ai (September 2026), Anthropic's Finance plugin 1.3.0 installed (our plugin turned off), Opus 5.5 High, case F's five Stripe exports attached. The bench's question alone, sent with the plugin's /reconciliation command; the session used the Finance plugin's reconciliation skill. Copied from the page as text. -->

I'll work through the August 2026 Stripe exports and reconcile sales, fees, payouts and balance.

August 2026 reconciles cleanly. Every payout ties to the cent to the transactions behind it, and the Stripe balance rolls forward from August 1 to August 31 with no difference. Figures use the account's own clock (UTC−5), which is the day boundary Stripe itself uses for its daily fees and reserve entries. On a UTC cut, gross charges would be $139,409.16 instead.

What happened to the money

Amount
Stripe balance, 1 Aug 3,685.15
+ Net volume (sales after refunds and disputes) 136,069.40
− Stripe fees (7,302.22)
− Moved into the rolling reserve (1,671.14)
− Payouts sent to the bank (130,027.10)
+ Failed payout returned to balance 3,688.05
= Stripe balance, 31 Aug 4,442.14

Bank side: 3,552.26 was in transit on 31 July. Add 126,339.05 of payouts sent in August (net of the failed one), subtract 10,085.69 still in transit on 31 August (it landed 1 September), and you get 119,805.62 that actually reached the bank in August.

How the lines are built

Sales: 4,266 charges. Net volume is gross charges, less refunds and disputes, plus disputes won back.
Stripe fees are made up of:
$6,408.26 card processing
$420.20 Stripe Billing
$353.76 Stripe Tax
$120.00 dispute fees: ten disputes at $15, less $30 returned on the two disputes won.
Tax is converted to dollars at each charge's own rate. EUR, GBP and CAD tax added up as if it were dollars would understate it by about $400.
$2,282.71 of it is US sales tax.
$6,119.71 is UK, EU and Canadian VAT/GST.
About $192 of the tax was handed back through August refunds.

Worth a look before you close

Payout bank account changed twice in August.
A new account was used from 12 August. A $3,946.70 payout to it shows as paid on 13 August.
The next payout to that account ($3,688.05) failed as "invalid account number". Those funds went back to the balance and out again in the 19 August payout to a third account.
Please check that both changes were authorised, and that the $3,946.70 really arrived in your bank.
Stripe started a 5% rolling reserve on 24 August. The $1,671.14 held at month end isn't cash in the bank or in the Stripe balance. It's an amount due from Stripe, released 30 days later (releases started 23 September).
Stripe billed the 10 August Billing fee twice. The $11.51 duplicate is in the August fees and was credited back on 9 September.
A $42.22 refund failed. It was issued on 28 August (order GL-109608) and failed on 2 September, so the money came back to the balance and the customer didn't receive it.
Most August disputes are still open. Of the 10, 7 are still under review and 3 were lost. The $53.45 won back relates to July disputes.
Test-mode charges are left out. The payments export includes some test charges; the balance export already leaves them out.

I can turn this into a workpaper spreadsheet with the transaction detail behind each line if your bookkeeper wants it.

Gross charges: $139,509.28
Refunds: $3,204.12
Disputes withdrawn: $289.21
Disputes won back: $53.45
Net volume: $136,069.40
Sales tax collected: $8,402.42
Stripe fees: $7,302.22
Paid out to the bank: $119,805.62
Still in transit at month end: $10,085.69
Stripe balance at month end: $4,442.14
Held in reserve at month end: $1,671.14
