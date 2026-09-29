<!-- Cowork in claude.ai (September 2026), Anthropic's Finance plugin 1.3.0 installed (our plugin turned off), Opus 5.5 High, case F's five Stripe exports and the owner's definitions (definitions.md) attached, sent with the plugin's /reconciliation command; the session used the Finance plugin's reconciliation skill. The bookkeeper lines were asked in one sentence ("each on its own line as 'Label: amount'"), not as a list: the chat box did not keep the line breaks. Copied from the page as text. -->

I'll work through the August 2026 Stripe exports against your definitions and give you the month-end figures.

August 2026 closes cleanly: the balance rolls forward from 1 August to 1 September to the cent.

What you sold. Gross charges were $139,409.16 across 4,264 live payments. That includes $8,404.78 of sales tax. After $3,204.12 of refunds (104 of them, 20 for payments made in June or July) and $289.21 of disputes withdrawn (10 of them), less $53.45 of disputes won back (2 of them), net volume is $135,969.28.

What Stripe kept. Total fees were $7,297.25:

$6,407.25 in processing fees on the month's charges.
$120.00 in net dispute fees: 10 × $15 charged, less 2 × $15 returned.
$770.00 in Billing and Tax usage fees.

What reached the bank and what's still on its way. Eighteen payouts totalling $126,339.05 left Stripe in August. Of that, $10,085.69 (created 31 Aug 21:49 UTC) was still in transit at month end and arrived on 1 September. On 1 September, $3,751.31 was still sitting in the Stripe balance, and $1,473.01 was held separately in reserve.

Roll-forward

USD
Balance 1 Aug 00:00 UTC 2,891.34
+ Gross charges 139,409.16
− Processing fees (6,407.25)
− Refunds (3,204.12)
− Disputes withdrawn, net of won back (235.76)
− Dispute fees, net (120.00)
− Billing/Tax fee rows (770.00)
− Moved into reserve (1,473.01)
− Payouts (failed one excluded) (126,339.05)
Balance 1 Sep 00:00 UTC 3,751.31

Every payout from July through October also matches the sum of the transactions Stripe assigned to it, except the first two in early July, which include June activity not in the export.

Items your bookkeeper should know about

Failed payout. The $3,688.05 payout of 13 Aug failed because the bank account number was invalid. The money came back on 14 Aug and went out in the $31,351.45 payout on 18 Aug. The payout bank account changed twice in August, and all payouts since 18 Aug have gone to the newest one. It's worth checking that this is the right account.
Rolling reserve. Stripe started holding back 5% of each day's volume on 25 Aug. The first release came on 24 Sep. None of the reserve is included in the balance figure above.
Refund that later failed. A $42.22 refund dated 28 Aug is counted in August refunds. It failed on 2 Sep, so the money returns in September.
Duplicate usage fee. The Billing usage fee for 10 Aug was charged twice ($11.51), and both charges are in August fees. Stripe credited one back on 9 Sep; under your rules that credit doesn't reduce fees.
Excluded items. Seventeen test-mode payments from 12 Aug are excluded; they never touched the balance. The usage fee for 31 Aug was posted on 1 Sep, so it falls in September.
Sales tax. For subscriptions I took tax from the invoices; for one-off orders, from the payments' tax metadata. Tax on CAD, EUR and GBP charges was converted at each charge's own rate and rounded per charge. Converting without per-charge rounding gives 6 cents less.
Dates. Everything is based on the UTC timestamps. The balance export's plain "created" column is in UTC−5, and using it would move items between months.
Export date. The files run to 3 October, but my calendar shows today as [run date]. This doesn't affect any August figure.

Gross charges: $139,409.16
Refunds: $3,204.12
Disputes withdrawn: $289.21
Disputes won back: $53.45
Net volume: $135,969.28
Sales tax collected: $8,404.78
Stripe fees: $7,297.25
Paid out to the bank: $126,339.05
Still in transit at month end: $10,085.69
Stripe balance at month end: $3,751.31
Held in reserve at month end: $1,473.01
