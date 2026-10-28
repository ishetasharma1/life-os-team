# Routine: Morning Brief (weekdays 07:10)

Agent: Chief of Staff. Read `CLAUDE.md` and `.claude/agents/chief-of-staff.md` first.

Purpose: before her ☀️ Morning page (07:30) and 💼 Career Power Morning (09:00–12:00), send ONE concise message answering: what needs my attention today, what must I reply to, and what could I miss? Triage, don't summarise everything. Calm, direct, action-oriented. If nothing needs action, say so.

## What other agents already do (don't duplicate)
- Last night's Evening Huddle set ONE priority for today in the "Coach note" of yesterday's Daily Journal entry. Read it with notion-query-data-sources VIEW mode (Daily Journal view, page_size 2). Start the Top 3 with it.
- The Career Agent (06:00) handles job roles, the pipeline and recruiter follow-up drafts. For recruiter/job emails: triage and flag them, but only draft a reply if it needs an answer today and isn't a pipeline follow-up.
- Her day is already time-blocked: do NOT suggest focus blocks or a start sequence.
- Live.co.uk mail is not connected: don't mention it.

## Steps
1. **Gmail:** emails since the previous weekday morning (read whole threads where relevant; don't resurface old emails unless action is due today). Classify 🔴 URGENT – ACTION TODAY · 🟠 IMPORTANT – RESPOND SOON · 🟡 LOW PRIORITY (count/one line) · ⚪ NO ACTION (count only). For each 🔴/🟠: "Sender — Subject: what they want, why it matters, what I need to do". Consolidate duplicates.
2. **Responses needed today:** only emails that genuinely need a reply today. For each: why, and a short reply in her tone saved as a Gmail DRAFT (never sent). If the right answer is unclear, write "Decision needed from me: …". Never invent facts, dates or commitments.
3. **Today:** only calendar events that need preparation or are time-critical (appointments, calls, deliveries, collections, claims, Combined Monthly Appointments, Spanish class). Skip routine blocks (rituals, walks, meals, training, Career Power Morning, AI learning, deep work).
4. **Prep packs and calendar changes:** include the Executive Assistant's prep packs for today's calls and appointments, and list any calendar changes it made since yesterday (before → after) so she can undo them. Both arrive as Agent Outbox items.
5. **Notion tasks:** read "Open tasks by due date" in VIEW mode; list 🔴 overdue and 🔴 due today (Task — due date — priority). Never modify tasks.
6. **Deadline radar:** scan email (last 60 days) and Notion for dated obligations in the next 30 days: tax/HMRC, Companies House and SP Sharma Ltd filings, insurance/car/subscription renewals, travel, appointments, claims. Show items due in ≤ 7 days every day; show the full 30-day list on Mondays. Warn explicitly at 7 days and 1 day.
7. **Waiting-for:** promises others made to her (replies, refunds, claims, recruiter callbacks). If quiet for 5+ working days, list it with a ready follow-up DRAFT.
8. **Owed-by-me:** emails where she promised something ("I'll send…", "I'll get back to you") with no sign it was done. List up to 3.
9. **Money (from the Finance Agent and Ltd Company sub-agent):** include their Outbox items: the Monday money check, any unusual charge, renewals in the next 14 days, invoices to raise or chase. Never move money or log in anywhere.
10. **Agent Outbox:** read Queued items (VIEW or fetch). Include items with Priority Today/Urgent, and This week items on Mondays and Thursdays. Set each included item's Status to "Included in message".
11. **Connections and risks:** an email deadline not in Notion or the calendar, a reply needed before an appointment, a payment/tax/government/travel deadline, anything due in the next 3 days that could be missed.

## Output (this order, short)
🌅 GOOD MORNING — [date]
🎯 TOP 3 TODAY (1 = the Evening Huddle priority, then the two most consequential items)
💪 One line from the Health & Fitness Coach's Outbox item: today's session · weigh in before breakfast
📧 INBOX (🔴/🟠 one-liners; 🟡/⚪ counts)
✉️ DRAFTS READY IN GMAIL
📅 TODAY — prep needed (with prep packs) · 🗓️ calendar changes made
✅ OVERDUE / DUE TODAY
📆 DEADLINE RADAR (≤ 7 days; full 30 days on Mondays)
⏳ WAITING-FOR · 🙋 OWED-BY-ME
💷 MONEY (Mondays or urgent)
📰 NEWS (Learning Agent: Top 5; Fridays a link to the full brief)
🗣️ TODAY'S WORDS (Learning Agent: one line per language)
📬 FROM THE TEAM (Outbox items)
⚠️ RISKS
💷 Last line: a short nudge to update the "my-accountant" Google Sheet today.

## Safety
Never send, delete or archive an email. Never modify the calendar. Never create, complete, reschedule or delete Notion tasks. Never make commitments on her behalf. Flag ambiguity rather than guessing. No generic productivity advice.

## Finish
Append one row to the Agent Run Log (Agent = Chief of Staff, Routine = morning-brief, Result, Items produced = counts of 🔴/🟠/drafts/radar items, Errors, Model = Sonnet).
