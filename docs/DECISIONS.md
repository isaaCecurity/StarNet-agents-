# Architecture Decision Log

## ADR-001 — Repository as project control center
**Decision:** Use this repository as the durable implementation and handoff record for StarNet Agents.

**Reason:** Another AI agent should be able to resume work without relying on the original conversation.

## ADR-002 — Social media first
**Decision:** The first production-oriented agent workforce focuses on social media/marketing rather than coding.

**Reason:** The user currently handles coding directly and wants to use StarNet to reduce non-coding workload first.

## ADR-003 — Human approval for high-impact actions
**Decision:** Require explicit approval before public posting, sensitive outbound communication, production changes and destructive operations during early stages.

**Reason:** Automation must be reliable before autonomy is increased.

## ADR-004 — Knowledge separated from reasoning
**Decision:** Durable knowledge must be retrievable as focused context rather than dumped into every model request.

**Updated after audit:** Do not commit to Obsidian/external retrieval yet. Test StarNet's native Commander Dossier, context files, memory, beliefs, records and seeded second brain first.

**Reason:** StarNet already provides substantial native knowledge/memory primitives; external infrastructure should be justified by a demonstrated gap.

## ADR-005 — Least privilege
**Decision:** Agents receive only the tools/data/project scope required for their role.

**Reason:** Limits security impact and prevents accidental cross-project actions.

## ADR-006 — Native StarNet primitives first
**Decision:** Use StarNet's native agents, workstations, orchestration, toolsets, approvals, budgets, model routing, skills, recipes, routines, loops, quests and memory before building equivalent external infrastructure.

**Reason:** The audit demonstrated that StarNet already supplies most of the required operating substrate. Duplicating it would add complexity, cost and failure points.

## ADR-007 — Native model routing
**Decision:** Use StarNet's DEEP/BALANCED/FAST clearance tiers and native fallback mechanisms before implementing a custom model router.

**Reason:** The installed runtime already supports task-appropriate model strength and fallback chains.

## ADR-008 — Native automation first
**Decision:** Prefer StarNet Recipes, Routines, Active Loops and Night Shift over an external workflow engine until a concrete capability gap is demonstrated.

**Reason:** The audit showed native automation primitives already exist.

## ADR-009 — Gradual autonomy
**Decision:** Keep E-STOP engaged during configuration and begin with approval-based/draft workflows. Increase autonomy only after reliability evidence.

**Reason:** StarNet exposes initiative, reach, pace, away-work and Night Shift controls; these should be deliberately configured rather than activated by default.

## ADR-010 — No new agents during audit/hardening
**Decision:** Do not recruit additional agents until the current Crew is fully understood and native agent classes are evaluated against the required responsibilities.

**Reason:** More agents increase token usage and coordination overhead. Distinct responsibility, not headcount, justifies an agent.

## ADR-011 — JUNIOR Full Power requires review
**Decision:** Treat JUNIOR's current FULL POWER configuration as temporary and review it before production use. Global Full Power remains OFF.

**Reason:** JUNIOR has significantly greater host authority than the other observed agents. We must determine the minimum authority needed for orchestration before reducing or expanding it.

## ADR-012 — Context efficiency is an immediate priority
**Decision:** Investigate and reduce unnecessarily large model contexts before paid-model scaling.

**Reason:** Supplied OpenRouter logs showed multiple requests around 34K–37K input tokens with very small outputs. Large prompts can create unnecessary cost and latency even when current spend is low.

## ADR-013 — Token counters are not billing equivalents
**Decision:** Do not interpret StarNet's all-time token counter as paid API spend.

**Evidence:** The supplied OpenRouter activity showed approximately 5.44M tokens and $0.01 for the displayed period, while a StarNet budget screen showed $0.00 today and $0.00 lifetime across 60 runs. These are different accounting scopes.
