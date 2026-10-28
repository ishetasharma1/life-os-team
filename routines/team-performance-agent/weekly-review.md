# Routine: Team Performance – Weekly Review (Fridays 16:22; monthly scorecard on the first Friday)

Agent: Team Performance Agent. Read `CLAUDE.md` and `.claude/agents/team-performance-agent.md` first. Sends NO message: writes ONE Agent Outbox item for Saturday's Weekend Brief. Read Notion in VIEW mode only (handbook section 5); get a view URL by fetching the database first.

Sources:
- Agent Run Log collection://7f336152-e2b5-4d58-9c00-c798dccd0a4d · Feedback Log collection://3cd97634-a291-426a-b90e-6854b1c60230 · Agent Outbox collection://3454181f-d803-4574-885e-a0eb0275d89a
- 🛠️ Team Improvements collection://7c499485-3aab-4dbd-835c-2ca0731c40d6 (view://eca46cd8-4865-4b59-9753-3ba4fe5422f6)
- The scheduled task list (`list_triggers`, load with ToolSearch "list_triggers"; page through every result)
- `docs/schedule.md`, every file in `.claude/agents/` and `routines/` (not `archive/`)
- Result records named in the handbook data map (Job Pipeline, Daily Coach Log, Move-Ready rooms, Life Maintenance) as each agent's success metrics need.

Review window: the last 7 days (Saturday to Friday). Old agent names in the logs map to new ones: Body Coach → Health & Fitness Coach, Home Agent → Home & Car Agent, "Health & Fitness Coach + Life Coach" → Evening Huddle.

1. **Reliability per scheduled task.** Expected runs from its schedule vs Run Log rows and `last_run`. Count Success / Partial / Failed / Skipped / no row. Flag: any failure repeated twice, any task that did not run, any run with no Run Log row, any task whose cron or model differs from `docs/schedule.md` and the handbook tiers.
2. **Usefulness.** Run Log "Useful" marks; Outbox items Queued for more than 48 hours (by agent); messages sent per day vs the budget of four.
3. **Results vs targets.** For each agent, its success metrics (agent file) against the handbook targets, from the records only. Missing data = "not logged". Recount totals across every source and say what each number is based on.
4. **Feedback.** New Feedback Log rows this week; any kind seen twice for the same agent (or "Times seen" ≥ 2) with Status New → a "Rule from feedback" proposal.
5. **Design check.** Contradictions between files and the handbook, stale times or links, overlapping duties, a cheaper model that would do the same job, or a gap no agent covers.
6. **Follow-up on past changes.** For each row Done 14–21 days ago, compare the before/after evidence. If it did not help, propose a revert or an adjustment.
7. **Proposals.** Rank everything found by impact on her goals (health first, then career, then the rest) and add **at most 5** rows to 🛠️ Team Improvements:
   - Proposal (one line), Agent, Type, Risk, Decision = Proposed, Proposed on = today.
   - Why (evidence): numbers, dates, error text, links.
   - Exact change: the files and lines or scheduled task fields to change, with the new wording; precise enough that the apply run needs no judgement.
   - Expected benefit: what will improve and how it will be measured.
   - Mark Risk High and start Exact change with "Needs live session:" for anything in the agent file's "live session" list.
   - Before adding, check existing rows: do not repeat a Proposed row (update its evidence instead); do not re-raise a Rejected row unless the evidence has materially changed (say what changed); Parked rows may return after 4 weeks.
   - If nothing is worth changing, add nothing and say so.
8. **Monthly scorecard (first Friday of the month only).** Create a page "Team scorecard — <Month YYYY>" under the Agent Team page (https://app.notion.com/p/4071ca99553d810186a9ebb9fb92c0bf): one table row per agent (runs, success %, useful %, corrections, key result vs target, keep / change / retire), the month's Done changes and whether they helped, and this agent's own approval rate. Recommendations to change or retire become proposals in step 7.
9. **Outbox.** ONE item "TEAM REVIEW — <date>" (From = Team Performance Agent, Priority This week, Deliver by Saturday 08:51, Link = the Team Improvements database https://app.notion.com/p/ffcc7cfa4045477481f007b80da86571):
   - Line 1: team health in one line (e.g. "41/43 runs succeeded; 1 repeated failure").
   - Up to 5 lines: each new proposal in plain words with its risk.
   - Last line: "N proposals waiting for your decision (Approve / Reject / Park in Team Improvements)".
   - Priority Today instead if a scheduled task failed twice in a row, did not run at all, or a safety rule may have been broken.

Finish with one Agent Run Log row: Agent = Team Performance Agent, Routine = weekly-review, Items produced = runs reviewed, proposals added, scorecard yes/no, Model = Opus.
