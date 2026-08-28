# Current State

> This file is the primary handoff/status document. Update it whenever meaningful project progress is made.

## Current Phase
**Phase 0 — Project Foundation**, moving into **Phase 1 — Knowledge System** and **Phase 2 — Social Media Workforce**.

## Critical Architecture Correction

StarNet is **already the runtime/application we are using**. It is not a backend that we need to build a separate web interface around.

The installed StarNet application is a local-first desktop AI-agent harness with a visual pixel-art station interface. The interface represents live runtime state: agents/crew, workspaces, communications, tasks, capabilities, model/provider state, budgets and other runtime information. The user runs StarNet locally as an executable/desktop application.

Our `StarNet-agents-` GitHub repository is therefore **not a replacement UI or a new StarNet implementation**. It is the project control plane/documentation layer for configuring, extending and operating the user's StarNet-based AI workforce.

Official StarNet capabilities that are relevant to this project include multi-agent workspaces with bounded permissions, OpenRouter/provider connections, Slack/Telegram/Discord/Signal/Matrix integrations, schedules/recipes/skills, MCP connectors, persistent local memory/transcripts/tasks/spend records, budgets, and consent checks. These capabilities should be verified against the user's installed version before relying on any specific feature.

## What the User's Current StarNet UI Shows

The user has provided a screenshot of the installed StarNet dashboard. It shows:
- A **Crew** area containing approximately eight created agents.
- A central **Agent Quarters / station** view representing the active workspace/runtime.
- A **Comms** panel where the user can communicate with the orchestrator/agent.
- Navigation for areas such as Crew, Work, Build and System.
- A visible token/spend indicator.
- Model/provider warnings in the communications area, confirming that provider configuration/rate limits are currently an important setup issue.

The exact names, roles, prompts, tools, MCPs, model assignments, permissions and workstation/loadout configuration of all eight agents still need to be documented from the live StarNet installation.

## What Has Been Decided

- Repository: `StarNet-agents-`.
- StarNet desktop harness is the primary runtime/orchestration environment.
- Initial real-world use case: social media and marketing automation.
- Coding automation is deferred for now; the user continues coding products directly.
- Long-term goal: a personalized AI workforce for the organization and its products.
- Planned products: BigFlow, Shift OS, Lingora and Mind Flow.
- Knowledge architecture: human-readable local knowledge source plus an indexing/retrieval layer so agents receive focused context.
- Obsidian remains a candidate/source-of-truth layer; the retrieval implementation is not yet finalized.
- Slack is intended as an important command, notification and approval interface and is already connected.
- Agents must use least privilege.
- High-impact external actions should require human approval initially.
- Model routing should use stronger reasoning for strategy/planning and cheaper models for routine work.
- Token usage must be monitored and constrained.

## Existing StarNet Setup

The user has already created approximately eight agents and configured some connectors/MCPs. OpenRouter was used as the current model provider during setup. Slack has also been connected through an app so the user can message StarNet and receive responses.

The current setup is still exploratory. The next job is **not** to rebuild StarNet. It is to audit the existing StarNet configuration and map it onto the target architecture.

## First Build Target: Social Media

Initial target workforce:
- Social Media Strategist
- Research/Trend Agent
- Content Creation Agent
- Brand/Quality Reviewer
- Publishing/Scheduling Agent
- Analytics Agent
- Knowledge/Memory Agent

Initial workflow:
`Research → Strategy → Draft → Review → User Approval → Publish/Schedule → Analytics → Lessons Learned`

## Completed in This Repository

- [x] Repository identified and initialized.
- [x] Project README established.
- [x] Master implementation plan created.
- [x] Current-state/handoff tracking established.
- [x] Architecture corrected to treat StarNet itself as the runtime/UI rather than a platform we need to recreate.

## Immediate Next Tasks

1. Audit the live StarNet UI and document all eight existing agents.
2. Document current model/provider configuration and investigate the visible rate-limit/provider warnings.
3. Document existing MCPs/connectors and their permissions.
4. Identify how StarNet's native workstations, skills, recipes, schedules and memory should map to our target architecture.
5. Decide the exact knowledge-base implementation after evaluating StarNet's native memory/MCP capabilities.
6. Create the local knowledge-vault structure.
7. Define social-media agent responsibilities and permissions.
8. Configure a first end-to-end social-media workflow in draft/approval mode.
9. Measure token usage before adding more automation.
10. Add monitoring and cost controls.

## Do Not Do Yet

- Do not build a separate dashboard to replace StarNet's native interface.
- Do not rebuild orchestration functionality that StarNet already provides unless a concrete gap is identified.
- Do not build the full autonomous organization immediately.
- Do not give every agent unrestricted access to every tool or project.
- Do not allow automatic public posting or sensitive outbound communication without an approval gate.
- Do not add coding agents as the primary focus yet.
- Do not optimize around the all-time token counter without measuring actual per-task cost.

## Last Updated
2026-08-28
