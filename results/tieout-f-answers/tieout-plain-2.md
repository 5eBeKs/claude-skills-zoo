Mostly not. Gross, refunds, disputes won back and net volume are right, but six other figures are wrong. I got these numbers from the balance-transaction export and cross-checked them against the payouts, payments and invoices exports.

**Wrong figures:**
- **Disputes withdrawn:** 10 chargebacks were withdrawn in August, totalling $289.21 before the $15 fees. The report says $265.14. Its net figure of $135,969.28 only works out with $289.21, so the table contradicts itself.
- **Stripe fees:** these should be $7,297.25: $6,407.25 processing, plus $150 dispute fees withdrawn, less $30 returned, plus $770.00 of Billing ($422.48) and Tax ($347.52) usage fees. The report's $6,527.25 leaves out the Billing/Tax fees even though its label says it includes them. The $11.51 credit for a duplicate Billing fee is dated 9 September, and credits aren't netted anyway.
- **Refund share:** $3,204.12 ÷ $139,409.16 is 2.30%, not 2.36%.
- **Euro payments:** $17,641.65 is the euro payments before fees. After $1,117.64 of processing fees they come to $16,524.01.
- **Paid out:** the $130,027.10 includes the $3,688.05 payout that failed on 14 August. Leaving it out gives $126,339.05. The $3,688.05 was then sent again inside the $31,351.45 payout on 18 August, which is already counted.
- **Month-end balance:** $5,224.32 includes the $1,473.01 rolling reserve Stripe withheld from 25 to 31 August. Without the reserve the balance is $3,751.31. I got that figure two independent ways (details under "Checked and right").
- **Renewals paid:** 2,364 renewal invoices were paid in August, not 2,221. Two of them had no card charge, so 2,362 went through Stripe as payments.
- **Unpaid renewals:** 41 renewal invoices were issued by month end and still unpaid (24 were later voided and 17 paid in September). The report says 58. Counting the four invoices created just before midnight on 31 August but only issued after it gives 45, which is still not 58.

**Checked and right:** gross $139,409.16 (all live, no test payments in the balance data), refunds $3,204.12 (the $42.22 failed refund came back on 2 September, so it belongs to September), disputes won back $53.45, net $135,969.28, processing fees at 4.6% of gross, and the $3,688.05 returned payout. The "about $10.1k" in transit is the $10,085.69 payout created 31 August that arrived 1 September. July gross was $125,344.26, so "up on July at about $139k" holds.

The two ways I got the $3,751.31 balance:
- the 1 July opening balance ($4,013.24, taken from the first July payout) plus all net movements since;
- adding up the transactions made by 31 August that were only paid out in September.

**Can't check from these files:**
- The open dispute count and how many need a response. The exports only show each dispute's status as of October, and disputes on June payments aren't in the payments export.
- MRR and its growth. The subscriptions export only shows each subscription as of October 4, so I can't rebuild 31 August.
- The Google Ads invoice and the hours spent.

The report doesn't give a figure for sales tax collected or for the reserve on its own line; the reserve at month end was $1,473.01.

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
58 | wrong, should be 41
$4,180.00 | cannot check from these files
