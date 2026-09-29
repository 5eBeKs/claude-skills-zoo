The report has **eight figures wrong**. The core sales figures (gross, refunds, disputes won back and net) are right. The mistakes are in disputes withdrawn, fees, payouts, the balance, the euro total, the refund rate and two subscription counts. All amounts come from `balance_transactions_itemized.csv` cut by `created_utc`, checked against the other exports.

**What's wrong and why**
- **Disputes withdrawn:** there are 10 chargeback withdrawals in August, totalling $289.21 without the $15 fees. Ledgerline's own net sales figure ($135,969.28) only works with $289.21, so the $265.14 in the table doesn't match their own maths.
- **Stripe fees:** $6,527.25 is processing fees ($6,407.25) plus net dispute fees ($150 − $30). It leaves out the $770.00 of Billing and Tax usage fees, even though the report's own label says they're included. The correct total is **$7,297.25**. That $770 includes an $11.51 Billing fee charged twice on Aug 11. Stripe credited it back on Sep 9, and under your rules that credit isn't netted.
- **Refund rate:** $3,204.12 ÷ $139,409.16 is **2.30%**, not 2.36%. July's rate was 2.42%, so "much the same" still holds. One refund failed ($42.22), but it came back on Sep 2, so it doesn't change August.
- **Euro payments:** $17,641.65 is the euro payments *before* Stripe's fees. After fees the figure is **$16,524.01**, from 562 live charges. Test-mode payments are excluded.
- **Paid out:** $130,027.10 still includes the $3,688.05 payout that failed on Aug 14. Without it the total is **$126,339.05**. The $10,085.69 payout created on Aug 31 arrived on Sep 1, so "about $10.1k in transit" is right.
- **Month-end balance:** $5,224.32 includes the rolling reserve. The balance without the reserve is **$3,751.31**. The reserve held at month end, which the report should show on its own line, is **$1,473.01** (withheld daily from Aug 25).
- **Renewals:** 2,364 renewal invoices were paid in August (2,344 monthly and 20 yearly), not 2,221.
- **Unpaid renewals:** 41 renewal invoices had been issued but were still unpaid and not voided at 00:00 on Sep 1, not 58.

**What I couldn't check**
- **Disputes open at month end:** the export only shows each dispute's status as of Oct 4. It also leaves out payments from before July, and some disputes are on May and June payments.
- **MRR and its growth:** subscription amounts are in four currencies, the export is a snapshot from Oct 4, and it doesn't say how long coupons last. My rough rebuild gives about $51.2k for August and about $48.8k for July. That suggests $48,759.34 may really be July's MRR, but this is only an estimate.
- **Google Ads invoice and hours:** these aren't in Stripe.

The report doesn't give a sales tax figure.

about $139k | right
6.5 hours | cannot check from these files
$139,409.16 | right
$3,204.12 | right
$265.14 | wrong, should be $289.21
$53.45 | right
$135,969.28 | right
$6,527.25 | wrong, should be $7,297.25
2.36% | wrong, should be 2.30%
4.6% | right
$17,641.65 | wrong, should be $16,524.01
$130,027.10 | wrong, should be $126,339.05
about $10.1k | right
$3,688.05 | right
$5,224.32 | wrong, should be $3,751.31
14 cases | cannot check from these files
two of them need a response | cannot check from these files
$48,759.34 | cannot check from these files
4.9% | cannot check from these files
2,221 renewals | wrong, should be 2,364
58 renewal invoices | wrong, should be 41
$4,180.00 | cannot check from these files
