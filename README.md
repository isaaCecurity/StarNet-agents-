# StarNet Agents

A personalized AI-agent organization built **inside the existing StarNet desktop runtime**. The long-term goal is to turn StarNet into a controlled digital workforce for the organization: reducing repetitive work, coordinating projects, managing knowledge, automating workflows, monitoring systems and supporting decisions.

## Core Principle

**Configure and extend StarNet; do not rebuild StarNet.**

StarNet is already the local executable/desktop application and graphical station interface. The GitHub repository is the project's durable control/documentation layer, not a replacement web dashboard.

## Vision

Grow from a small Social Media/Marketing workforce into a broader AI operating system supporting:

- Social media and marketing
- Research and market intelligence
- Customer support
- Email/outreach
- Product strategy and analytics
- Project/operations management
- QA and code review
- Security and DevOps
- Deployment monitoring and log analysis
- Scheduling and task management
- Strategic decision support

The user remains in control of high-impact actions.

## Current Products

- **BigFlow** — nearly finished; user continues coding it directly for now.
- **Shift OS** — friend is nearly finished.
- **Lingora** — planned/in progress.
- **Mind Flow** — planned/in progress.

The organization may later expand beyond SaaS.

## Current Phase

**StarNet Native Audit completed → Station Hardening / Configuration.**

The supplied StarNet screenshots established that the runtime already provides native primitives for:

- agents and agent dossiers
- workstations/execution profiles
- memory, reflection, beliefs and records
- skills and a large skill library
- recipes, routines and active loops
- Night Shift/autonomy
- task delegation/orchestration
- MCP/connectors
- toolsets/capabilities
- approvals and Full Power controls
- DEEP/BALANCED/FAST model routing and fallbacks
- budgets and runtime limits
- quests and deliverables
- extensions/hooks/plugins
- E-STOP

Therefore the current project is primarily **configuration, governance, knowledge design, workflow design and optimization**.

## Immediate Priorities

1. Correct the Commander Dossier with canonical organization context.
2. Verify and document the complete existing Crew.
3. Review JUNIOR's current Full Power authority.
4. Verify Composio/Slack/GitHub/Google Drive connection states.
5. Establish least-privilege tool/workstation permissions.
6. Configure conservative model, budget and runtime controls.
7. Diagnose failed away-work routines.
8. Test StarNet's native memory and seeded second brain before selecting Obsidian/external retrieval.
9. Investigate large 34K–37K input-token requests.
10. Only then configure the first Social Media workflow.

## Native-vs-External Rule

Before adding infrastructure:

1. Check whether StarNet already provides it.
2. If not, check MCP/Composio/connectors.
3. If still missing, consider a small supporting service.
4. Only then consider a separate platform.

This avoids duplicated functionality, unnecessary token usage and unnecessary operational complexity.

## Repository Documentation

- `docs/MASTER_PLAN.md` — roadmap.
- `docs/CURRENT_STATE.md` — authoritative current status.
- `docs/ARCHITECTURE.md` — architecture and native/external boundaries.
- `docs/AGENT_ROLES.md` — role definitions and permissions.
- `docs/KNOWLEDGE_SYSTEM.md` — knowledge/memory strategy.
- `docs/WORKFLOWS.md` — workflow and automation rules.
- `docs/SECURITY_AND_GOVERNANCE.md` — security and approval policy.
- `docs/COST_AND_MODEL_ROUTING.md` — cost and model strategy.
- `docs/DECISIONS.md` — durable architecture decisions.
- `docs/STARNET_CONFIGURATION.md` — observed live StarNet configuration inventory.
- `docs/HANDOFF.md` — continuation protocol for another AI agent.
- `TASKS.md` — active work.
- `CHANGELOG.md` — historical project changes.

## Source of Truth Rule

This repository is the implementation-control center for StarNet Agents. Major decisions, verified configuration changes and project-state changes must be documented so another AI can resume the work without reconstructing the original conversation.

Never commit API keys, OAuth secrets, access tokens, private credentials or other sensitive information.
