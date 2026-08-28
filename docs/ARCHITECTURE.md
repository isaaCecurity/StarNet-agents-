# StarNet Agents — Architecture

## Architectural Goal

Build a personalized AI workforce **on top of the existing StarNet desktop AI-agent harness**. StarNet is the runtime/application and already provides the primary visual interface, agent/workspace model, communications, provider connections and orchestration capabilities. This repository defines the configuration, knowledge, workflows, governance and long-term operating model we want to implement within that environment.

## Important Boundary

We are **not building a replacement StarNet web application**.

The architecture has two parts:

1. **StarNet runtime** — the installed executable/desktop application that provides the UI, agents, workspaces, orchestration, integrations and runtime state.
2. **StarNet Agents project layer** — this GitHub repository plus the knowledge system, workflow definitions, prompts/policies, configuration documentation and future supporting services that make the StarNet runtime into a personalized organizational AI workforce.

## Layers

### 1. User / Native StarNet Interface
- StarNet desktop application
- Crew/agent view
- Work/task view
- Build/configuration view
- System/settings view
- Agent communications
- Slack and other connected channels

### 2. Executive / Control
- Strategy Agent: what should happen?
- Planning/Architect Agent: how should it happen?
- Commander: coordinate a major objective.
- Orchestrator: route tasks and manage dependencies.
- Evaluation Agent: did it work and meet requirements?

Where StarNet already provides orchestration or task-management functionality, use the native capability rather than duplicating it externally.

### 3. Specialized Workforce
Social, research, content, outreach, analytics, support, operations, engineering, security, QA and future domain agents.

Initial priority is social media/marketing; coding automation is deliberately deferred.

### 4. Knowledge / Memory
Human-readable source of truth → index → retrieval → focused context.

Recommended conceptual split:
- Organization memory
- Product/project memory
- Task/working memory
- Long-term lessons

The exact implementation may use StarNet's native persistent memory plus an external/local knowledge vault and retrieval layer where that provides better control or search quality.

### 5. Workflow / Automation
Trigger → retrieve context → reason → execute → evaluate → approval if required → action → monitor → record outcome.

Prefer StarNet-native schedules, recipes, skills and event/automation capabilities where suitable. Add external workflow infrastructure only when StarNet cannot provide the required behavior reliably.

### 6. Model Layer
Model provider(s) selected by task complexity. Strong models for high-value reasoning; economical models for routine tasks.

OpenRouter is currently being used during setup. Provider configuration and rate-limit behavior must be measured before committing to a paid model strategy.

### 7. Execution / Integration Layer
StarNet connectors, MCP servers and controlled tools for:
- GitHub
- Social platforms
- Email
- Slack
- Browsers/APIs
- Cloud infrastructure
- Local files and applications
- Future business systems

Each agent receives only the tools and permissions required for its role.

### 8. Observability
- Agent activity
- Workflow execution
- Token/model usage
- Spend
- Errors
- Provider/rate-limit events
- Application/service logs
- Alerts
- Audit history

Use StarNet's native runtime/spend information where available, then add external observability only for gaps.

### 9. Governance
Least privilege, secret isolation, approvals, rate limits, budget limits, sandboxing and emergency stop controls.

## Target Data Flow

`User → StarNet Interface/Channel → Orchestrator → Strategy/Planning → Specialist Agent → Knowledge Retrieval → Tool/Workflow → Evaluation → Approval → External Action → Monitoring → Learning`

Not every request needs every layer. Simple tasks should take the shortest safe path.

## Context Efficiency

Agents should not receive the entire knowledge vault, repository or conversation history by default. Retrieval should select the smallest useful context. Deterministic search, metadata filtering and embeddings should happen before expensive LLM reasoning where practical.

## Native-vs-External Rule

Before adding another platform, ask:

1. Does StarNet already provide this capability?
2. Is the native implementation sufficient for our requirements?
3. If not, can an MCP/connector solve the gap?
4. If not, should we add a small supporting service?
5. Only then consider a separate orchestration/workflow platform.

This prevents unnecessary duplication and keeps the system understandable and cost-efficient.

## Failure Boundaries

Every external action should have:
- permission boundary
- timeout
- retry policy
- idempotency strategy where applicable
- audit record
- rollback or recovery plan where feasible

## Scaling Rule

Add agents only when there is a distinct responsibility that cannot be handled cleanly by an existing role. More agents are not automatically better; unnecessary delegation increases complexity and token cost.
