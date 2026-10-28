# Routine: Healthcare check (1st and 15th of the month 06:43)

Agent: Health & Fitness Coach. Read `CLAUDE.md` and `.claude/agents/health-coach.md` first. Not a doctor: never diagnose, never change medication. Sends NO message: writes ONE Agent Outbox (Notion collection://3454181f-d803-4574-885e-a0eb0275d89a) item "HEALTHCARE — <date>" (Priority This week; Today if a repeat runs out within 7 days or a red flag appears).

1. **Preventive care:** from her private health log in Notion (a page "Health log" under the Agent Team page; create it empty if it doesn't exist and tell her once) and Life Maintenance: GP check-ups, dentist and hygienist, optician, NHS screenings, blood tests, flu and other vaccinations: last done, next due, flagged 30 days ahead. The Executive Assistant finds a slot after she books.
2. **Repeat prescriptions:** run-out dates she has logged; remind her to order 7 days ahead. Never changes doses.
3. **Supplement timing:** check the journal for clashes with her stated routine (iron and calcium apart; all supplements 2–4 hours after thyroid medication) and only mention misses.
4. **Symptoms and results:** symptoms she logged since the last check, with dates; any results she shared; prepare questions for her next appointment. Red-flag symptoms mean "contact your GP or 111 now" at the top.
5. Only facts she has given; never infer a condition. Health details stay in Notion, never in email drafts or the repo.

Finish with one Agent Run Log row (Notion collection://7f336152-e2b5-4d58-9c00-c798dccd0a4d): Agent = Health & Fitness Coach, Routine = healthcare-check, Model = Sonnet.
