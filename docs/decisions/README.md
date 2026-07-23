# Decisions

Architecture Decision Records (ADRs) — a short record for each significant, hard-to-reverse decision, so the reasoning survives even after the decision itself is old news.

## Canonical ADR log

The platform's ADRs are maintained as a **single canonical log** in the workspace architecture doc set (adjacent to this repo):

**`AI-QA-OS-Architecture-Decisions.md`**

It currently records twenty ADRs:

| ADR | Title | Status |
|---|---|---|
| ADR-001 | QA Brain as central decision authority | Accepted |
| ADR-002 | Workflow Engine as pipeline orchestrator | Accepted |
| ADR-003 | Memory Engine as a tiered experience store | Accepted |
| ADR-004 | Gateway as the single public entry point | Accepted |
| ADR-005 | Agent Manager as mandatory mediator | Accepted |
| ADR-006 | Self-Healing as a first-class autonomous capability | Accepted — Planned |
| ADR-007 | AI Governance as a cross-cutting control plane | Accepted — Planned |
| ADR-008 | Multi-Tenancy as a core context dimension | Accepted — Planned |
| ADR-009 | Decision & roadmap-honesty discipline | Accepted |
| ADR-010 | Confidence gate: contract in core, impl in the Brain | Accepted |
| ADR-011 | Human review: in-memory resume (gateway) + durable queue (DB) | Accepted |
| ADR-012 | A dedicated evaluation & guardrails module with contract seams | Accepted |
| ADR-013 | Prompt regression baseline as a committed file | Accepted |
| ADR-014 | Two-tier prompt-eval CI gate: deterministic always-on + live key-gated | Accepted |
| ADR-015 | Guardrail contract promoted to core; the AI-boundary control point | Accepted |
| ADR-016 | Centralised hardened security headers + download-only HTML artifacts | Accepted |
| ADR-017 | Execution decoupled behind a job-queue + artifact-store seam | Accepted — Partial |
| ADR-018 | Artifact object storage via a client seam + opt-in age retention | Accepted — Partial |
| ADR-019 | Module↔package naming convention + MDC correlation-id propagation | Accepted |
| ADR-020 | Raw-OTel tracing: config-gated export + span instrumentation | Accepted |

## Convention

New ADRs are appended to the canonical log. Each records **Status** (Proposed / Accepted / Accepted — Planned / Superseded), **Context**, **Decision**, and **Consequences**, per the Documentation Standard (`../../AI-QA-OS-Documentation-Standard.md`, Section 1a). ADRs are **immutable once Accepted** — a changed decision is a new *superseding* ADR, never an edit to history (see ADR-009).

> A single source of truth is used deliberately to minimise drift (MNT-5 decision, Option A). Per-file ADRs (`NNN-Descriptive-Title.md`) may be split out into this folder later if the log grows.

---

Established by **MNT-5** (2026-07-22). Previously this folder was an empty scaffold ("No files yet").
