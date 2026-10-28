# Routine: Team Performance – Apply Approved Changes (daily 21:17)

Agent: Team Performance Agent. Read `CLAUDE.md` and `.claude/agents/team-performance-agent.md` first. Sends NO message. Silent when nothing is approved.

1. **Find approvals.** Query 🛠️ Team Improvements in VIEW mode (view://eca46cd8-4865-4b59-9753-3ba4fe5422f6) and keep only rows with Decision = **Approved**. If there are none, write a Run Log row (Result = Skipped, Items produced = "nothing approved") and stop.
2. **Check each row before acting.** Skip it (leave it Approved, write the reason in Change log, and add one Outbox item Priority Today: "Needs you: <proposal>") if:
   - Exact change starts with "Needs live session:" or falls in the agent file's live-session list, or
   - "Your notes" is unclear or conflicts with Exact change, or
   - the change would delete anything (retire = pause the scheduled task and move the routine file to `archive/`), or
   - the files have changed since the proposal so the change no longer fits.
3. **Make the change, exactly as written plus her notes.**
   - Repo: `git pull --ff-only` first so you work on the newest files. Edit only what the row names. Keep everything she added; list any text removed.
   - Scheduled tasks: load `list_triggers` and `update_trigger` with ToolSearch. Change only the fields named (name, schedule, model, prompt, enabled). Never delete one. Send a schedule or name change in a call without a prompt. If a prompt change returns `needs_device_approval`, nothing changed: record that and flag it as in step 2.
   - Keep `docs/schedule.md`, the handbook and agent files consistent with any time, model or roster change.
4. **Commit and push**, one commit per proposal: "Team improvement: <proposal>" with the handbook's attribution lines if the repo uses them. If the push fails, record the error, leave the row Approved, and add an Outbox item Priority Today: "Approved change ready but not saved: <proposal>". Do not retry more than once.
5. **Close the row.** Decision = Done, Done on = today, Change log = what changed (file or scheduled task, before → after in short), commit hash, anything removed, and how the weekly review will check it worked.
6. **Outbox.** If anything was applied, ONE item "TEAM CHANGES APPLIED — <date>" (Priority FYI) listing each change in one line, for the next brief.

Finish with one Agent Run Log row: Agent = Team Performance Agent, Routine = apply-approved, Result, Items produced = applied / skipped counts, Errors, Model = Opus.
