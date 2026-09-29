I checked the report against the exports. The totals in the summary table are mostly right, but several figures elsewhere are wrong. Gross sales, refunds and disputes won back all match to the cent. Net sales is also right, but it doesn't follow from the report's own disputes figure.

**What's wrong:**
- **Disputes withdrawn:** 12 chargebacks took money out of the balance in August, totalling **$289.21**, not $265.14. Using the correct figure, $139,409.16 − $3,204.12 − $289.21 + $53.45 = $135,969.28, which is the net figure the report shows. Its own $265.14 would give $135,993.35.
- **Stripe fees:** the report's $6,527.25 is processing ($6,407.25) plus dispute fees ($180 withdrawn − $30 returned = $120). It leaves out the $770.00 of Billing and Tax usage fees created in August. The total should be **$7,297.25**. A September credit of $11.51 for a duplicate August Billing fee stays out, because a credit isn't netted against fees.
- **Refund rate:** $3,204.12 ÷ $139,409.16 = **2.30%**. The 2.36% comes from dividing by net sales instead of gross.
- **Euro payments:** $17,641.65 is the euro charges *before* fees. After $1,117.64 in processing fees they come to **$16,524.01**.
- **Paid out:** $130,027.10 still includes the $3,688.05 payout that bounced (created Aug 13, failed Aug 14). Without it the figure is **$126,339.05**. The money came back to the balance and went out in the Aug 18 payout, which is already in that total.
- **Month-end balance:** available plus pending at 00:00 UTC on Sep 1 was **$3,751.31**. That's the August transactions paid out in the Sep 1 payout. The report's $5,224.32 is exactly that plus the $1,473.01 rolling reserve held back from Aug 25 to Aug 31. The reserve should be shown on its own line: **$1,473.01 held in reserve at month end**. None of it was released until Sep 24.
- **Renewals:** **2,364** renewal invoices were paid in August, not 2,221. That count includes 20 July invoices that were paid on a retry in August, and 2 invoices for $0.
- **Unpaid renewals:** **45** August renewal invoices were still open at month end, not 58.

**What's right:** there were no test-mode payments among the August balance transactions. No refund failed and came back in August; the one refund failure is dated Sep 2, so it belongs to September. Processing fees were 4.6% of gross. The payout still in transit was $10,085.69, and it landed Sep 1.

**What I couldn't check:**
- **Open disputes:** the payments export only shows each dispute's status as of October 4. It doesn't show when lost cases closed, and some cases involve charges from before July. So I can't count what was open or needed a response on Aug 31.
- **MRR:** this would need subscription history and a rule for converting EUR, GBP and CAD plans to dollars. The exports have neither.
- **Hours and Google Ads:** the 6.5 hours and the Google Ads invoice aren't in the Stripe data.

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
two of them | cannot check from these files
$48,759.34 | cannot check from these files
4.9% | cannot check from these files
2,221 | wrong, should be 2,364
58 | wrong, should be 45
$4,180.00 | cannot check from these files
