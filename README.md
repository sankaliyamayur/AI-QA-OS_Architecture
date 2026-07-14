# AI-QA-OS Documentation

This is the working documentation system for building AI-QA-OS step by step. It sits alongside [`00-Foundation/`](./00-Foundation/), which holds the platform's architecture and design blueprints — the [`docs/`](./docs/) tree below exists to track *build progress* against that architecture: prompts given to Claude Code, implementation notes, and verification results, one Step and Phase at a time.

Start here:

1. Read [`AI-QA-OS-Documentation-Standard.md`](./AI-QA-OS-Documentation-Standard.md) — the naming, formatting, and structure rules every file below follows.
2. Read [`docs/roadmap/00-Project-Roadmap.md`](./docs/roadmap/00-Project-Roadmap.md) — the full Phase/Step build sequence and current status.
3. Copy the relevant file from [`docs/templates/`](./docs/templates/) to begin the next Step.

---

## Folder Index

| # | Folder | Purpose |
|---|---|---|
| 01 | [`docs/architecture/`](./docs/architecture/README.md) | Architecture notes scoped to an individual step or subsystem (system diagrams, module dependencies) |
| 02 | [`docs/phases/`](./docs/phases/README.md) | The 18 high-level build Phases (`Phase-01-Foundation.md` … `Phase-18-End-to-End-Integration.md`) |
| 03 | [`docs/implementation/`](./docs/implementation/README.md) | The 12 functional development Steps (`01-Requirement-Management.md` … `12-End-to-End-Platform.md`) |
| 04 | [`docs/prompts/`](./docs/prompts/README.md) | Copy-paste-ready Claude Code prompts, one per Step |
| 05 | [`docs/verification/`](./docs/verification/README.md) | Post-implementation walkthroughs and pass/fail evidence, one per Step |
| 06 | [`docs/workflow/`](./docs/workflow/AI-QA-OS-Workflow.md) | How the platform executes, learns, and coordinates agents end to end |
| 07 | [`docs/api/`](./docs/api/README.md) | API reference documentation as endpoints are built |
| 08 | [`docs/guides/`](./docs/guides/README.md) | User-facing and developer-facing how-to guides |
| 09 | [`docs/templates/`](./docs/templates/) | Reusable Markdown templates for every document type above |
| 10 | [`docs/user-stories/`](./docs/user-stories/README.md) | Source user stories / acceptance criteria feeding the Requirement Agent |
| 11 | [`docs/knowledge/`](./docs/knowledge/README.md) | Curated reference knowledge and learnings behind documentation decisions |
| 12 | [`docs/examples/`](./docs/examples/README.md) | Worked examples — sample requirement → test case → automation walkthroughs |
| 13 | [`docs/integrations/`](./docs/integrations/README.md) | How-to docs for external system integrations (Jira, GitHub, MCP servers, CI/CD) |
| 14 | [`docs/release-notes/`](./docs/release-notes/README.md) | What shipped in each released version |
| 15 | [`docs/changelog/`](./docs/changelog/README.md) | Per-component changelogs |
| 16 | [`docs/testing/`](./docs/testing/README.md) | Test strategy and coverage for the platform itself |
| 17 | [`docs/decisions/`](./docs/decisions/README.md) | Architecture Decision Records (ADRs) |
| 18 | [`docs/assets/`](./docs/assets/README.md) | Images, diagrams, and other binary assets referenced from docs |
| — | [`docs/roadmap/`](./docs/roadmap/00-Project-Roadmap.md) | Overall project roadmap, release plan, future features, and doc version history |

---

## Naming Convention (short version)

Numbered files sort in build order automatically:

```
01-Requirement-Management.md
02-Semantic-Parser.md
03-Brain-Analysis.md
```

Full rules: [`AI-QA-OS-Documentation-Standard.md`](./AI-QA-OS-Documentation-Standard.md).

---

## Relationship to `00-Foundation/`

`00-Foundation/` = the architecture (what AI-QA-OS is and how it's designed).

`docs/` = the build log (how it's actually getting built, prompt by prompt, step by step).

Nothing in `00-Foundation/` is modified by work done here.

---

## Document Completion Status

Status: Framework Established — Step content not yet authored

Version: 1.1.0
