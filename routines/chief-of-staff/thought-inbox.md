# Routine: Thought Inbox (daily 18:40)

Agent: Chief of Staff. Read `CLAUDE.md` and `.claude/agents/chief-of-staff.md` first.

Review her Notion 🧠 Inbox and process new thoughts (mostly Wispr voice captures).

**Reading Notion:** VIEW mode only (fetch the 🧠 Inbox database once to get a view URL, then filter to Status = Inbox yourself). For duplicate checks use ONE notion-search per item (search the Tasks database by keywords). Existing open tasks are also in the view "Open tasks by due date" (read it once per run and reuse it).

Only process entries where Status = Inbox. For each:
1. Read and understand the original thought, including imperfect voice transcription. Do not overwrite the original Thought.
2. Classify: Task, Project, Knowledge, Idea, Decision, Reflection, Reference, Someday.
3. Genuine task: check for duplicates; if none, create a Task (Status = Not Started, appropriate Priority, Due Date only if explicitly stated or clearly required), linked to an existing Project where appropriate and back to the Inbox thought.
4. Multi-step outcome: reuse an existing Project if possible; only create a new Project when genuinely necessary; link the thought.
5. Useful information: add to the Knowledge database, linked to a relevant Project where appropriate.
6. Idea, Reflection, Decision, Reference, Someday: classify and preserve; don't create a Task.
7. Never invent deadlines. If genuinely unsure, set Status = Needs Review.
8. Decluttering: the 🏡 90-Day Move-Ready Home project already has one task per room. Never create new decluttering tasks; link to the existing room task.
9. **Promises and waiting-for:** if a thought records something someone owes her or she owes someone, also add it as an Agent Outbox item (Priority This week) so the morning brief tracks it.

After processing: Status = Processed; populate Type, Next Action, Project and Priority where appropriate; keep the original thought. Never delete Inbox entries, Tasks, Projects or Knowledge; never change completed tasks.

**Multiple thoughts in one entry:** process each independently; never combine unrelated thoughts into one Task.

**Human corrections:** if she has filled in Type, Project, Priority or Next Action, treat it as authoritative. If she moves Needs Review back to Inbox, process it using her corrections.

**Protect existing tasks:** never delete, rename, complete, reprioritise or reschedule an existing task because of a new thought. Link instead of duplicating.

**Messages:** if nothing was in the Inbox, finish silently. Otherwise do NOT message her; put one Agent Outbox item (Priority Today) listing anything set to Needs Review or any new task due within 7 days, for tomorrow's morning brief. Only message directly if something is due tomorrow before 07:10.

Finish with one Agent Run Log row (Routine = thought-inbox).
