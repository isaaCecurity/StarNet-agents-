# StarNet Agents

A personal, organization-wide AI workforce designed to reduce repetitive work, coordinate projects, manage knowledge, automate workflows, and provide decision support.

## Vision

Build a modular AI operating system that can grow from a small social-media assistant into a broader digital workforce supporting products, engineering, research, marketing, operations, customer support, monitoring, and strategic work.

The system should be **goal-driven, context-aware, cost-controlled, permissioned, auditable, and human-supervised for high-impact actions**.

## Current Starting Point

The first implementation focus is **social media**, not coding. Coding automation is intentionally deferred because the user currently prefers to handle product coding directly.

Current product context:
- BigFlow — SaaS product, already substantially developed.
- Shift OS — SaaS product, already substantially developed.
- Lingora — planned/in-progress product.
- Mind Flow — planned/in-progress product.

## Core Architecture

1. User / communication channels
2. Executive and orchestration layer
3. Specialized agent workforce
4. Knowledge and memory layer
5. Workflow and automation engine
6. Model/provider layer
7. Tool and execution layer
8. Monitoring and observability
9. Evaluation and feedback
10. Learning and adaptation
11. Security, governance, cost controls, and human approval

## Repository Documentation

- [`docs/MASTER_PLAN.md`](docs/MASTER_PLAN.md) — complete implementation roadmap from setup to end state.
- [`docs/CURRENT_STATE.md`](docs/CURRENT_STATE.md) — authoritative current progress and next action.
- [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) — system architecture and boundaries.
- [`docs/AGENT_ROLES.md`](docs/AGENT_ROLES.md) — agent responsibilities and permissions.
- [`docs/KNOWLEDGE_SYSTEM.md`](docs/KNOWLEDGE_SYSTEM.md) — second-brain and retrieval design.
- [`docs/WORKFLOWS.md`](docs/WORKFLOWS.md) — workflow patterns and automation rules.
- [`docs/SECURITY_AND_GOVERNANCE.md`](docs/SECURITY_AND_GOVERNANCE.md) — security and human-approval policy.
- [`docs/COST_AND_MODEL_ROUTING.md`](docs/COST_AND_MODEL_ROUTING.md) — token/cost strategy.
- [`docs/DECISIONS.md`](docs/DECISIONS.md) — architectural decisions and rationale.
- [`docs/HANDOFF.md`](docs/HANDOFF.md) — instructions for another AI agent taking over the project.
- [`CHANGELOG.md`](CHANGELOG.md) — major project changes.

## Source of Truth Rule

This repository is the **implementation-control center** for the StarNet Agents project. When a major decision is made, update the relevant documentation so another AI can resume work without reconstructing the entire conversation.

Never commit API keys, OAuth secrets, access tokens, private credentials, or other sensitive information.
