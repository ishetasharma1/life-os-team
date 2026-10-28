# Life OS Team

A team of six AI agents that runs Isheta Sharma's personal operating system: career, health, home, learning, relationships and admin. It is built on Claude scheduled tasks, Notion as the system of record, and Gmail, Calendar, Drive and Indeed connectors, with humans approving every irreversible step.

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
| Chief of Staff | Run the day: triage, deadlines, admin, money, the morning brief | Mid |
| Career Agent | Land the right role by 30 Nov and build an AI-era profile | Top |
| Body Coach | Health is goal #1: food, training, recovery, weekly plan | Mid |
| Life Coach | Keep the 11 goals moving: reviews, people, meaning | Top |
| Home Agent | Move-ready home, selling, pets, home projects | Mid |
| Learning Agent | Languages, signal-only news, continuous AI learning | Mid |

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
- `docs/10-day-plan.md`: the build plan
- `evals/`: golden tasks and scores (added on day 9)

*Private repository: contains personal details.*
