# Routine: Money check (Mondays 06:11)

Agent: Finance Agent. Read `CLAUDE.md` and `.claude/agents/finance-agent.md` first. Sends NO message: writes ONE Agent Outbox (Notion collection://3454181f-d803-4574-885e-a0eb0275d89a) item "MONEY — <date>" (From = Finance Agent, Priority This week, or Today if something is urgent; Deliver by today 06:43) for the Morning Brief.

1. **"my-accountant" sheet:** read it (Google Sheets). Which of the last 7 days have no transactions logged? List them and ask her to fill them in. Never edit past entries.
2. **Unusual charges:** from email receipts and bank/card emails in the last 7 days (Gmail, read only): duplicate payments, price rises, refunds not yet received, unknown merchants. Each with the email it comes from.
3. **Renewals:** subscriptions and bills renewing in the next 14 days, with amounts where the email shows them; a keep-or-cancel prompt for anything she may not use.
4. **Ltd:** fold in the Ltd Company sub-agent's latest Friday item headline (invoices overdue, deadlines in 30 days).
5. Never move money, log in anywhere, cancel anything or give investment advice; questions go to Phil Mosedale (personal) or Red76 (company).

Finish with one Agent Run Log row (Notion collection://7f336152-e2b5-4d58-9c00-c798dccd0a4d): Agent = Finance Agent, Routine = money-check, Model = Sonnet.
