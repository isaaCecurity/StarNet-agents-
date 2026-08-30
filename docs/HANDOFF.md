# AI Agent Handoff Protocol

This file tells a new AI agent how to continue the StarNet Agents project.

## First Read

Read these in order:
1. `README.md`
2. `docs/CURRENT_STATE.md`
3. `docs/MASTER_PLAN.md`
4. `docs/DECISIONS.md`
5. `docs/STARNET_CONFIGURATION.md`
6. Documentation relevant to the current task

## Operating Rules

- Treat `CURRENT_STATE.md` as authoritative current status.
- Treat `MASTER_PLAN.md` as the roadmap, not proof of implementation.
- Treat `DECISIONS.md` as durable decisions.
- Treat `STARNET_CONFIGURATION.md` as the observed StarNet configuration inventory; unknowns must remain unknown until verified.
- Never claim a StarNet feature, integration or authentication state exists unless it has been verified.
- Prefer StarNet-native capabilities before proposing external infrastructure.
- Before adding a platform, ask whether StarNet already provides the capability, then whether MCP/Composio can fill the gap.
- Never commit secrets.
- Prefer small, reversible changes.
- Update `CURRENT_STATE.md` after meaningful work.
- Update `DECISIONS.md` when a durable architectural decision changes.
- Update `MASTER_PLAN.md` when the roadmap changes.

## Current Verified Direction

StarNet is the existing local desktop runtime. Do not design a replacement web dashboard.

The audited station already provides native agents, workstations, memory, records, skills, recipes, routines, loops, autonomy, MCP/connectors, toolsets, approvals, budgets, model routing/fallback, quests, deliverables and E-STOP.

Therefore the project is currently a **configuration/hardening and workflow-design effort**, not a platform-rebuild effort.

## Current Priority

**Station hardening first, Social Media/Marketing second.** Coding automation is deliberately deferred because the user is currently handling product coding directly.

## Immediate Next Work

1. Update the Commander Dossier with canonical organization/product context.
2. Verify the full Crew list and document every existing agent.
3. Review JUNIOR's current FULL POWER authority and determine minimum orchestration permissions.
4. Verify Composio, Slack, GitHub and Google Drive connection states.
5. Build the least-privilege agent/tool/workstation matrix.
6. Set conservative budgets/model/concurrency controls.
7. Diagnose failed KEN/JEFF away-work routines.
8. Keep E-STOP engaged during hardening.
9. Test native memory and seeded second-brain behavior before selecting Obsidian/external retrieval.
10. Investigate 34K–37K input-token requests before paid-model scaling.
11. Only then configure the first draft-only Social Media workflow.

## Important Current Risks

- JUNIOR currently has FULL POWER while other observed agents use approval-based risky actions.
- Global Full Power is OFF and must remain OFF.
- E-STOP is engaged; do not enable autonomous schedules/loops/Night Shift yet.
- Two six-hour away-work routines show `missing terminal outcome` failures.
- Commander Dossier/Quest text contains stale setup information.
- Large model input contexts are a likely source of avoidable cost/latency.

## Communication Style

When reporting progress, provide:
- What was done
- What was verified
- What remains
- Risks/blockers
- Next concrete action
