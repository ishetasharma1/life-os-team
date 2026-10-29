# Routine: Company check (Fridays 06:13; month-end pack on the first Friday of the month)

Agent: Ltd Company sub-agent (SP Sharma Ltd). Read `CLAUDE.md`, `.claude/agents/finance-agent.md` and `.claude/agents/ltd-company-agent.md` first. Accountant: Red76. VAT registered. Sends NO message: writes ONE Agent Outbox (Notion collection://3454181f-d803-4574-885e-a0eb0275d89a) item "LTD — <date>" (Priority This week; Today if something is overdue or due within 7 days).

1. **Invoices:** from Gmail and Drive, invoices issued, due and paid. Overdue 7 or 14 days past due → a polite chase draft (Gmail draft, never sent). If contract days for the month are confirmed by her but no invoice exists, prepare a draft invoice in EUR to her template and numbering, with the VAT treatment Red76 has confirmed for that client; if unconfirmed, flag it.
2. **EUR→GBP:** for invoices paid since last week: EUR invoiced, GBP received, implied rate vs the market rate that day (web source); flag more than 2% worse with the £ cost.
3. **Deadlines:** Corporation Tax, quarterly VAT returns, Companies House accounts and confirmation statement, PAYE/payroll, self-assessment: anything within 30 days, with 30/7/1-day warnings (dates from her emails or Companies House/HMRC pages; never guessed).
4. **Expenses:** business receipts in Gmail this week into the monthly expenses log (Drive sheet "SP Sharma Ltd Expenses <YYYY-MM>": date, supplier, amount, category, link); flag missing receipts.
5. **Pay, dividends and pension:** if a salary, dividend or pension decision is coming up, a short list of questions for Red76 (and Phil for pension). Never advise.
6. **First Friday of the month:** the month-end pack for Red76 as a Gmail draft (invoices, payments, expenses log link, open questions). Never sent.

Never send, file, pay or contact HMRC/Companies House. Finish with one Agent Run Log row (Notion collection://7f336152-e2b5-4d58-9c00-c798dccd0a4d): Agent = Ltd Company sub-agent, Routine = company-check, Model = Sonnet.
