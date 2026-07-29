# Decisions

Architecture Decision Records (ADRs) — a short record for each significant, hard-to-reverse decision, so the reasoning survives even after the decision itself is old news.

## Canonical ADR log

The platform's ADRs are maintained as a **single canonical log** in the workspace architecture doc set (adjacent to this repo):

**`AI-QA-OS-Architecture-Decisions.md`**

It currently records forty-nine ADRs:

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
| ADR-021 | Vector store standardization: Qdrant + In-Memory | Accepted |
| ADR-022 | Semantic & prompt cache for AI invocations | Accepted |
| ADR-023 | Sharded cross-browser execution matrix (fan-out over virtual threads) | Accepted |
| ADR-024 | Single migration owner + per-service connection pools (shared schema by design) | Accepted |
| ADR-025 | LLM cost-quota enforcement at the provider choke point (soft cap) | Accepted |
| ADR-026 | Unified AI audit trail by aggregation over run-keyed sources | Accepted |
| ADR-027 | Deterministic weighted prompt A/B routing + leaderboard over PE-1 scores | Accepted |
| ADR-028 | Durable version registry with pin/rollback behind a store seam (prompt now, generic for model) | Accepted |
| ADR-029 | Responsible-AI policy as a config-driven guardrail at the SEC-3 boundary (OPA deferred) | Accepted |
| ADR-030 | Real PII masking in `ai-qa-os-testdata`: classification-driven, pluggable strategies, format-preserving default | Accepted |
| ADR-031 | Close the continuous-learning loop via recorded improvement proposals; adoption gated on LRN-4 | Accepted |
| ADR-032 | Safe-adoption gate: core contract + Brain impl reusing the confidence gate + an eval threshold | Accepted |
| ADR-033 | Autonomous locator healing: deterministic heuristic healer behind a seam + confidence-gated auto-apply | Accepted |
| ADR-034 | Learning metrics computed in-module over a supplied observation series | Accepted |
| ADR-035 | Healing approval: strict confidence tier for script edits + in-module approval lifecycle | Accepted |
| ADR-036 | Plugin architecture: in-process contract + lifecycle registry with semver + permission governance | Accepted |
| ADR-037 | Integration plugins normalised on the PLG-1 contract via delegating adapters + governed registrar | Accepted |
| ADR-038 | Learning loop closed end-to-end: LRN-1 proposals gated through the LRN-4 safe-adoption gate | Accepted |
| ADR-039 | Self-healing loop closed end-to-end: HEAL-1 locator proposal governed by the HEAL-2 approval workflow | Accepted |
| ADR-040 | Governance loop closed: version promotion policy-gated by the Responsible-AI policy | Accepted |
| ADR-041 | Multi-tenancy foundation: tenant-context contract in `core` with thread-local + MDC propagation | Accepted |
| ADR-042 | `ai-qa-os-tenant` module: tenant registry seam + active-only resolver over the `core` context | Accepted |
| ADR-043 | Gateway tenant-resolution filter: request-scoped tenant binding (ENT-1 FI-ENT1-B) | Accepted |
| ADR-044 | `ai-qa-os-notification` module: single governed egress point via a channel-sender SPI | Accepted |
| ADR-045 | First-class agent roster catalog (AGT-1 increment) | Accepted |
| ADR-046 | Tenant-scoped cross-run healing memory over `MemoryStore` | Accepted |
| ADR-047 | Healing analytics read-model via a pure assembler (HEAL-3 backend increment) | Accepted |
| ADR-048 | Extension SDK: uniform `Extension` SPI in `core` + governed registry in `integration` | Accepted |
| ADR-049 | Centralised event→notification routing + templating over MOD-2 | Accepted |

## Convention

New ADRs are appended to the canonical log. Each records **Status** (Proposed / Accepted / Accepted — Planned / Superseded), **Context**, **Decision**, and **Consequences**, per the Documentation Standard (`../../AI-QA-OS-Documentation-Standard.md`, Section 1a). ADRs are **immutable once Accepted** — a changed decision is a new *superseding* ADR, never an edit to history (see ADR-009).

> A single source of truth is used deliberately to minimise drift (MNT-5 decision, Option A). Per-file ADRs (`NNN-Descriptive-Title.md`) may be split out into this folder later if the log grows.

---

Established by **MNT-5** (2026-07-22). Previously this folder was an empty scaffold ("No files yet").
