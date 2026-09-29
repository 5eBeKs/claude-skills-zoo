My last reply shortened the checking sections and added figures in my own words, so it didn't match the checked text. Below is the answer exactly as the saved calculation produced it. The same text is saved as `files/amazon-month-end_2026-08.md`.

About the figures:
- **Not everything shows up at the bank in the same month.** One August payout failed and Amazon paid it again in a later settlement. That settlement closed on the last day of the month but reached the bank in September, so it's counted in what Amazon owes. The "What reached the bank" and "What Amazon still owes us" sections show the details.
- **Amazon now pays a different account.** Payouts went to one account until August and to another account after that. Please check that the change was yours.
- **Two of my own rules need your OK.** I made them when the calculation was first set up: how orders are counted, and which report each figure comes from. They're under "Open questions".
- **All amounts are in US dollars.** A minus sign means money going out.

---

# Amazon month-end, 2026-08

**What we sold.** Product sales were 104,709.12. With shipping credits of 4,270.66, gift wrap credits of 119.76, promotional rebates of -1,387.26 and refunds of -4,550.17, net product sales were 103,162.11. Orders placed in the month: 2,917; 41 fully cancelled orders are left out.

**What Amazon kept.** Amazon fees were -40,616.33: referral fees -15,616.88, FBA fulfilment fees -17,840.96, storage fees -774.85 and other fees -6,383.64. Advertising was -10,826.11. Reimbursements paid to us were 222.06.

Storage fees counted this month, as they posted: FBA storage fee -642.10 posted 2026-08-10 (Pacific), FBA Long-Term Storage Fee -132.75 posted 2026-08-17 (Pacific).

Marketplace facilitator tax collected from buyers was 7,540.11; Amazon withheld and paid it over, so it nets to 0.00 and is in none of the figures above.

**What reached the bank.** Deposited to the bank: 32,239.51 in 1 deposits: settlement 26900538638: 32,239.51 on 2026-08-06 to account x4417.

Amazon's transfers posted this month: To account ending in 4417 -32,239.51 (settlement 26900538638), To account ending in 4417 -21,849.95 (settlement 26944784040), Failed disbursement 21,849.95 (settlement 26985759971), To account ending in 8841 -46,421.19 (settlement 26985759971).

**What Amazon still owes us.** Owed by Amazon at month end: 69,067.66, made of settlement 26985759971: 46,421.19 (closed, deposited after month end), settlement 26988006297: -179.50 (negative balance carried), settlement 27027934433: 22,825.97 (open settlement). Of these, closed settlements not in the bank (in transit, failed or negative): settlement 26985759971 (closed, deposited after month end): 46,421.19, settlement 26988006297 (negative balance carried): -179.50. The reserve held at month end, apart from what is owed, was 4,069.25, from settlement 26988006297.

**Roll-forward.** Owed at the start of the month 49,054.47 plus the reserve at the start 4,380.22, plus everything posted to us in the month 51,941.73 (tax excluded, transfers and reserve lines excluded), less deposits 32,239.51, gives owed at month end 69,067.66 plus reserve at month end 4,069.25.

Left out or not placed:
- Cancelled orders left out: order 111-1112329-5723576, order 111-1869761-9785685, order 111-2532641-0159177, order 111-3441428-9728088, order 111-3677601-3880631, order 111-4238876-1693963, order 112-1212902-0235358, order 112-2683278-8326914, order 112-2810778-3697126, order 112-7137723-5416226, order 112-7439446-5043930, order 112-7610440-9176900, order 112-8314560-6441783, order 113-0356429-8915462, order 113-2156111-6967800, order 113-2602427-2727685, order 113-2753288-7159327, order 113-2798226-0813640, order 113-2890776-1672050, order 113-3567755-5890012, order 113-3595607-8238759, order 113-4093028-4807500, order 113-5793090-2189234, order 113-5840474-4903781, order 113-6229151-1534283, order 113-6281973-6195983, order 113-7224747-8140050, order 113-8010781-5154284, order 113-9967404-1167541, order 114-2610710-8425975, order 114-3515262-2657338, order 114-3736735-8478124, order 114-3866898-2005001, order 114-4186356-9595456, order 114-5329446-7839978, order 114-6253626-7499817, order 114-6970651-7503755, order 114-7473281-8393699, order 114-8152970-2738167, order 114-8442382-1090337, order 114-9527558-6591054
- Orders on another sales channel left out: none
- Date Range lines not placed: none
- Settlement lines not placed: none
- Settlements with lines this month but no settlement file (their lines counted in owed from the Date Range report): none

## How this was counted
- Month: the Pacific calendar month (America/Los_Angeles) of each line's posted date and time; a deposit in the month the bank posted it; an order in the month of its purchase date, Pacific time.
- Money in US dollars from our side: money to us positive; fees, refunds and advertising negative.
- Product sales: the product principal of the month's order lines, without tax.
- Refunds: everything given back to buyers on Refund, A-to-z Guarantee and Chargeback lines except tax: principal, shipping, gift wrap, and the promotion amounts that come back on the refund.
- Net product sales: product sales plus shipping credits, gift wrap credits and promotional rebates, plus refunds (all without tax).
- Amazon fees: referral fees (commission, commission returned on refunds, the refund administration fee), FBA fulfilment fees, storage fees (monthly and aged-inventory, in the month they post), and other fees (shipping and gift wrap chargebacks and their reversals, the subscription fee, removal and disposal, inbound placement, coupon fees, Buy Shipping labels).
- Advertising: the Sponsored Products invoices charged to the account, by posted date.
- Reimbursements: FBA inventory reimbursements, including customer-return reimbursements and their reversals.
- Marketplace facilitator tax is collected and paid over by Amazon: not our money, shown apart, and it nets to zero.
- Deposited to the bank: the deposits the bank posted in the month; a deposit that failed is not deposited.
- Owed by Amazon at month end: all money Amazon had posted to us by the month end that had not reached the bank, less the reserve: the open settlement, deferred orders, closed settlements whose deposit was in transit or failed, negative balances carried.
- Reserve held at month end: the Current Reserve Amount of the last settlement closed before the month end.
- Reserve lines, Payable to Amazon, Failed disbursement and Transfer lines move money inside Amazon or to the bank: never sales, fees or refunds.
- Orders (Claude's reading): distinct Amazon order ids placed in the month, Pacific time, on an Amazon sales channel; an order whose every line is cancelled is left out, a partly cancelled order counts once.
- Sources (Claude's reading): sales, refunds, fees, advertising and reimbursements from the Date Range report; what is owed and the reserve from the settlement files; deposits from the bank list; orders from the All Orders report. The settlements check the Date Range report figure by figure.
- Which date puts a sale, fee or refund in a period? The date the line posted in the settlement or transaction report (your answer)
- In which time zone does a day end? The seller's own time zone, as the books are kept (your answer)
- What is in "sales"? The item price only (your answer)
- How is the tax the marketplace collects and pays over to the state counted? Not the seller's money: left out of sales, shown apart, netting to zero (your answer)
- Which period does a refund belong to? The period the refund posted (your answer)
- Which parts of a refund count as refunds? Everything given back to the buyer except tax, promotion amounts that come back included (your answer)
- How do buyer-protection claims and card chargebacks count? As refunds, in the period they post (your answer)
- How does the referral fee returned on a refund, and the refund administration fee, count? Both in referral fees (your answer)
- Which period does a storage fee belong to? The period it posted (your answer)
- How is advertising taken from the settlement counted? Advertising invoices, by the date they posted (your answer)
- How do shipping labels bought through the marketplace count? As marketplace fees (your answer)
- How do reimbursements for lost, damaged or returned stock count? A line of their own, reversals included (your answer)
- How do fees to remove or dispose of stock count? In the marketplace's other fees (your answer)
- Which date puts a deposit in a period? The date the bank posted it (your answer)
- How does a deposit that failed count? Not deposited; it stays owed until it is paid again (your answer)
- What does "the marketplace still owes us" include at the end of a period? Everything posted to the seller and not yet in the bank, less the reserve; the reserve shown apart (your answer)
- How do the reserve lines of a settlement count? As movements inside the marketplace: never sales, fees or refunds (your answer)
- How do amounts the marketplace holds until delivery count? Activity when they post; owed until paid out (your answer)
- What counts as an order in a period? Orders placed in the period, fully cancelled ones left out (Claude's reading, not yet confirmed by you)
- What happens when two reports cover the same lines? Each figure from one report; the others only check it (Claude's reading, not yet confirmed by you)

## Open questions
- What counts as an order in a period? Claude counted it this way: Orders placed in the period, fully cancelled ones left out Is that how you count?
- What happens when two reports cover the same lines? Claude counted it this way: Each figure from one report; the others only check it Is that how you count?

## Checks
- a settlement that crosses a month end is split by its lines' dates, not counted in the month it closed: checked by 'cross-check with settlements: product sales', passed
- lines posted on the last evening of a month in local time stay in that month: checked by 'roll-forward', passed
- tax the marketplace collects and remits is not in sales and nets to zero: checked by 'facilitator tax nets to zero', passed
- promotions reduce sales and the part returned on a refund reduces the refund: checked by 'promotions reduce sales', passed
- a refund's shipping, gift wrap and returned promotion are refund parts, and its tax is not: checked by 'cross-check with settlements: refunds', passed
- buyer-protection claims and chargebacks are counted, not dropped as unknown line types: checked by 'every line placed', passed
- the referral fee returned on a refund and the refund administration fee are fees, not refunds: checked by 'cross-check with settlements: referral fees', passed
- a storage fee posted this month is for an earlier month, and the answer says which period it is counted in: checked by 'cross-check with settlements: storage fees', passed
- an advertising invoice posted just after midnight on the 1st is placed by the chosen time zone: checked by 'cross-check with settlements: advertising', passed
- a reimbursement reversed later is netted in the period of the reversal: checked by 'cross-check with settlements: reimbursements', passed
- a failed deposit is not in the bank and is paid again later; it is counted once: checked by 'each settlement reaches the bank once', passed
- a negative settlement carried into the next one is not a deposit and not a cost: checked by 'carried balances matched', passed
- reserve release and reserve hold lines net inside the marketplace and are not activity: checked by 'reserve chain', passed
- each deposit equals the total of its settlement, and a difference is named: checked by 'each deposit equals its settlement total', passed
- owed at the start plus the period's activity less deposits equals owed at the end: checked by 'roll-forward', passed
- the order count says whether it counts placed orders or orders with a sale posted: checked by 'posted orders are in the orders report', passed
- a line present in two reports is counted once: checked by 'no row repeated', passed
- a report in another encoding or with lines before its header is read, not guessed: checked by 'recount: rows', passed

What pin.py counted again from the files:
- 2026AugMonthlyTransaction.csv: all 3,882 rows are in exactly one of the calculation's 2 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- 2026AugMonthlyTransaction.csv: the groups' 'Regulatory Fee' add up to the file's own 'Regulatory Fee' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'Tax On Regulatory Fee' add up to the file's own 'Tax On Regulatory Fee' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'fba fees' add up to the file's own 'fba fees' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'gift wrap credits' add up to the file's own 'gift wrap credits' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'giftwrap credits tax' add up to the file's own 'giftwrap credits tax' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'marketplace withheld tax' add up to the file's own 'marketplace withheld tax' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'other' add up to the file's own 'other' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'other transaction fees' add up to the file's own 'other transaction fees' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'product sales' add up to the file's own 'product sales' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'product sales tax' add up to the file's own 'product sales tax' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'promotional rebates' add up to the file's own 'promotional rebates' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'promotional rebates tax' add up to the file's own 'promotional rebates tax' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'selling fees' add up to the file's own 'selling fees' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'shipping credits' add up to the file's own 'shipping credits' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'shipping credits tax' add up to the file's own 'shipping credits tax' total (added up again)
- 2026AugMonthlyTransaction.csv: the groups' 'total' add up to the file's own 'total' total (added up again)
- 2026JulMonthlyTransaction.csv: all 4,277 rows are in exactly one of the calculation's 2 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- 2026JulMonthlyTransaction.csv: the groups' 'Regulatory Fee' add up to the file's own 'Regulatory Fee' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'Tax On Regulatory Fee' add up to the file's own 'Tax On Regulatory Fee' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'fba fees' add up to the file's own 'fba fees' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'gift wrap credits' add up to the file's own 'gift wrap credits' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'giftwrap credits tax' add up to the file's own 'giftwrap credits tax' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'marketplace withheld tax' add up to the file's own 'marketplace withheld tax' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'other' add up to the file's own 'other' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'other transaction fees' add up to the file's own 'other transaction fees' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'product sales' add up to the file's own 'product sales' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'product sales tax' add up to the file's own 'product sales tax' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'promotional rebates' add up to the file's own 'promotional rebates' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'promotional rebates tax' add up to the file's own 'promotional rebates tax' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'selling fees' add up to the file's own 'selling fees' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'shipping credits' add up to the file's own 'shipping credits' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'shipping credits tax' add up to the file's own 'shipping credits tax' total (added up again)
- 2026JulMonthlyTransaction.csv: the groups' 'total' add up to the file's own 'total' total (added up again)
- 2026SepMonthlyTransaction.csv: all 4,073 rows are in exactly one of the calculation's 2 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- 2026SepMonthlyTransaction.csv: the groups' 'Regulatory Fee' add up to the file's own 'Regulatory Fee' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'Tax On Regulatory Fee' add up to the file's own 'Tax On Regulatory Fee' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'fba fees' add up to the file's own 'fba fees' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'gift wrap credits' add up to the file's own 'gift wrap credits' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'giftwrap credits tax' add up to the file's own 'giftwrap credits tax' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'marketplace withheld tax' add up to the file's own 'marketplace withheld tax' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'other' add up to the file's own 'other' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'other transaction fees' add up to the file's own 'other transaction fees' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'product sales' add up to the file's own 'product sales' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'product sales tax' add up to the file's own 'product sales tax' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'promotional rebates' add up to the file's own 'promotional rebates' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'promotional rebates tax' add up to the file's own 'promotional rebates tax' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'selling fees' add up to the file's own 'selling fees' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'shipping credits' add up to the file's own 'shipping credits' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'shipping credits tax' add up to the file's own 'shipping credits tax' total (added up again)
- 2026SepMonthlyTransaction.csv: the groups' 'total' add up to the file's own 'total' total (added up again)
- settlement_26821949902.txt: all 8,077 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- settlement_26821949902.txt: the groups' 'amount' add up to the file's own 'amount' total (added up again)
- settlement_26860307225.txt: all 7,729 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- settlement_26860307225.txt: the groups' 'amount' add up to the file's own 'amount' total (added up again)
- settlement_26900538638.txt: all 11,884 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- settlement_26900538638.txt: the groups' 'amount' add up to the file's own 'amount' total (added up again)
- settlement_26944784040.txt: all 8,303 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- settlement_26944784040.txt: the groups' 'amount' add up to the file's own 'amount' total (added up again)
- settlement_26985759971.txt: all 9,017 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- settlement_26985759971.txt: the groups' 'amount' add up to the file's own 'amount' total (added up again)
- settlement_26988006297.txt: all 12 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- settlement_26988006297.txt: the groups' 'amount' add up to the file's own 'amount' total (added up again)
- settlement_27027934433.txt: all 8,851 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- settlement_27027934433.txt: the groups' 'amount' add up to the file's own 'amount' total (added up again)
- settlement_27066464770.txt: all 10,120 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- settlement_27066464770.txt: the groups' 'amount' add up to the file's own 'amount' total (added up again)
- disbursements.csv: all 6 rows are in exactly one of the calculation's 2 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- disbursements.csv: the groups' 'amount' add up to the file's own 'amount' total (added up again)
- all_orders_2026-07-01_2026-09-30.txt: all 10,740 rows are in exactly one of the calculation's 3 groups (pin.py counted the rows again from the file; it checks the groups, not each figure)
- all_orders_2026-07-01_2026-09-30.txt: the groups' 'item-price' add up to the file's own 'item-price' total (added up again)

What each break of a copy of the files did:
- rows exported twice (every 50th) in 2026JulMonthlyTransaction.csv: caught (warned: Control failed: no row repeated: 86 Date Range row(s) appear more than once)
- amounts in cents (x100) in 2026JulMonthlyTransaction.csv: caught (warned: Control failed: cross-check with settlements: product sales: Date Range 11,281,817.00 against settlements 112,818.17; differ in 26860307225, 26900538638, 269447)
- amounts with a decimal comma in 2026JulMonthlyTransaction.csv: caught (the answer stops: calc.py stopped (exit 2):)
- a kind of row the calculation never saw (every 50th row) in 2026JulMonthlyTransaction.csv: caught (warned: New in 2026JulMonthlyTransaction.csv, column 'type': 'zz_new_kind' on 86 row(s). The calculation was pinned without it; check how it counts before using these f)
- amounts a cent off (every 50th row) in 2026JulMonthlyTransaction.csv: caught (warned: Control failed: every line placed: 172 line(s) not placed or not adding up)
- rows exported twice (every 50th) in all_orders_2026-07-01_2026-09-30.txt: caught (warned: Control failed: no order line repeated: 215 orders report line(s) appear twice)
- the last three days of every month missing in all_orders_2026-07-01_2026-09-30.txt: caught (warned: Control failed: posted orders are in the orders report: 1057 order(s) posted in the Date Range reports are missing from the orders report)
- amounts in cents (x100) in all_orders_2026-07-01_2026-09-30.txt: no effect (the figures stay the same)
- amounts with a decimal comma in all_orders_2026-07-01_2026-09-30.txt: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in all_orders_2026-07-01_2026-09-30.txt: caught (warned: Control failed: orders post after they are placed: 1487 order(s) posted before their purchase time)
- a kind of row the calculation never saw (every 50th row) in all_orders_2026-07-01_2026-09-30.txt: caught (warned: New in all_orders_2026-07-01_2026-09-30.txt, column 'order-status': 'zz_new_kind' on 215 row(s). The calculation was pinned without it; check how it counts befo)
- amounts a cent off (every 50th row) in all_orders_2026-07-01_2026-09-30.txt: no effect (the figures stay the same)
- rows exported twice (every 50th) in disbursements.csv: caught (warned: Control failed: each settlement reaches the bank once: deposited more than once: 26821949902)
- amounts in cents (x100) in disbursements.csv: caught (warned: Control failed: each deposit equals its settlement total: 26821949902: bank 2,287,957.00, settlement 22,879.57; 26860307225: bank 1,448,220.00, settlement 14,48)
- amounts with a decimal comma in disbursements.csv: caught (the answer stops: calc.py stopped (exit 2):)
- amounts a cent off (every 50th row) in disbursements.csv: caught (warned: Control failed: each deposit equals its settlement total: 26821949902: bank 22,879.58, settlement 22,879.57)
- rows exported twice (every 50th) in settlement_26900538638.txt: caught (the answer stops: calc.py stopped (exit 2):)
- the last three days of every month missing in settlement_26900538638.txt: caught (warned: Control failed: each settlement's lines add up to its total: 26900538638: lines 33,993.39, total 32,239.51)
- amounts in cents (x100) in settlement_26900538638.txt: caught (warned: Control failed: each settlement's lines add up to its total: 26900538638: lines 3,223,951.00, total 32,239.51)
- amounts with a decimal comma in settlement_26900538638.txt: caught (the answer stops: calc.py stopped (exit 2):)
- times written eight hours later (another time zone) in settlement_26900538638.txt: caught (warned: Control failed: reserve chain: a gap or overlap between settlement 26860307225 (ends 2026-07-21 03:15) and 26900538638; a gap or overlap between settlement 2690)
- a kind of row the calculation never saw (every 50th row) in settlement_26900538638.txt: caught (warned: New in settlement_26900538638.txt, column 'transaction-type': 'zz_new_kind' on 238 row(s). The calculation was pinned without it; check how it counts before usi)
- amounts a cent off (every 50th row) in settlement_26900538638.txt: caught (warned: Control failed: each settlement's lines add up to its total: 26900538638: lines 32,241.88, total 32,239.51)

For the bookkeeper:
Product sales: 104,709.12
Refunds: -4,550.17
Net product sales: 103,162.11
Amazon fees: -40,616.33
Advertising: -10,826.11
Reimbursements: 222.06
Deposited to the bank: 32,239.51
Owed by Amazon at month end: 69,067.66
Reserve held at month end: 4,069.25
Orders: 2,917

Counted by the pinned calculation 935eb0dd68d9 ('amazon-month-end', pin 1); the same code, definitions and answer as when the owner pinned it.

Checked by pinned-calculation v0.11.6 · seal e976aad0ec24
