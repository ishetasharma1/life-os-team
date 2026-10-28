# Routine: Monthly close (2nd of the month 06:37)

Agent: Finance Agent. Read `CLAUDE.md` and `.claude/agents/finance-agent.md` first. Sends NO message: writes ONE Agent Outbox (Notion collection://3454181f-d803-4574-885e-a0eb0275d89a) item "MONTHLY CLOSE — <month>" (Priority This week) and a page in 📊 Reviews & Coaching only if she has asked for one.

1. **Spend by category** for last month from the "my-accountant" sheet against her monthly budget categories, with a traffic light (green on plan, amber within 10% over, red beyond). If no budget is set yet, ask her once to set categories and amounts and show actuals only.
2. **Net worth and FIRE:** net-worth figure for month-end if she has logged it; savings rate; FIRE % towards £1.5m and the trend vs last month. If not logged, say "not logged" and prompt her. Never estimate balances.
3. **Pet budget:** the Vet Agent's monthly pet spend, if available.
4. **Ltd summary:** the Ltd Company sub-agent's month-end pack headline (invoiced, paid, overdue, deadlines).
5. **Questions for advisers:** anything that needs Phil Mosedale or Red76, as a short list.
6. **Moving-abroad money pack:** if the Life Coach or she has flagged a move as concrete, request a refresh from the Research Agent (Outbox item "RESEARCH: moving-abroad money pack").

Finish with one Agent Run Log row (Notion collection://7f336152-e2b5-4d58-9c00-c798dccd0a4d): Agent = Finance Agent, Routine = monthly-close, Model = Sonnet.
