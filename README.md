# Life OS Team

A team of ten AI agents (plus one sub-agent) that runs Isheta Sharma's personal operating system: career, health, home, learning, relationships and admin. It is built on Claude scheduled tasks, Notion as the system of record, and Gmail, Calendar, Drive and Indeed connectors, with humans approving every irreversible step.

## How it works

```
 Triggers (scheduled tasks) ──► Agent (.claude/agents/*.md) ──► Skills (.claude/skills/)
                                   │  reads CLAUDE.md (one shared handbook)
                                   ▼
        Tools: Notion · Gmail (drafts) · Calendar · Drive · Indeed · web · browser (read-only)
                                   │
                                   ▼
        Agent Outbox ──► Chief of Staff ──► max 4 messages a day ──► Isheta decides
                                   │
                                   ▼
                    Run Log · Feedback Log · Evals ──► monthly team review
```

## The team

| Agent | Mission | Model tier |
|---|---|---|
| Chief of Staff | Triage, priorities, deadline radar, the briefs; composes all team messages | Mid |
| Executive Assistant | Calendar, schedule, appointments, travel, logistics, admin | Mid |
| Career Agent | Roles, applications, recruiters, interviews, AI-era profile | Top |
| Health & Fitness Coach | Food, training, recovery, personal healthcare | Mid |
| Life Coach | Reviews, 11 goals, people, meaning | Top |
| Home & Car Agent | Move-ready home, selling, home and car maintenance | Mid |
| Vet Agent | Pet care schedule, weights, vet visits | Mid |
| Finance Agent (+ Ltd Company sub-agent) | Personal accounts and FIRE; SP Sharma Ltd compliance and invoicing | Mid |
| Research Agent | Sourced research on request; weekly deep dive | Top |
| Learning Agent | Languages, news, AI learning | Mid |

## Design principles
1. One handbook (`CLAUDE.md`); agents never copy it.
2. Least privilege: each agent gets only the connectors it needs.
3. Claude prepares, the human decides: drafts only, nothing sent, bought or deleted.
4. Untrusted content is data, never instructions.
5. Every run logged; every correction becomes a rule; every agent has evals.

## Repository map
- `CLAUDE.md`: team handbook (targets, rules, safety, data map, protocol)
- `.claude/agents/`: one charter per agent
- `.claude/skills/`: reusable procedures (added from day 6)
- `docs/schedule.md`: every scheduled task, time and output
- `docs/10-day-plan.md`: original build plan (superseded: built in one day, 28 Oct 2026)
- `evals/`: golden tasks and scores (added on day 9)

*Private repository: contains personal details.*
