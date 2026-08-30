# StarNet Agents — Architecture

## Architectural Goal

Build a personalized AI workforce **inside and on top of the existing StarNet desktop AI-agent harness**. StarNet is the runtime/application and already provides the primary UI, agents, workstations, orchestration primitives, memory, tools, permissions, approvals, models, budgets and automation mechanisms.

This repository is the project control plane: it defines the organizational configuration, policies, knowledge strategy, workflow designs, governance rules, decisions and implementation roadmap.

## Important Boundary

We are **not building a replacement StarNet web application**.

The architecture has two layers:

1. **StarNet runtime** — installed local executable/desktop application providing the operational environment.
2. **StarNet Agents project layer** — this repository plus only those supporting knowledge/integration components that StarNet cannot provide natively.

## Native StarNet Substrate Observed

The audit of the supplied StarNet screenshots/settings established native support for:

- Crew and agent recruitment/classes.
- Agent dossiers and structured prompt files: `identity.md`, `purpose.md`, `context.md`, `operating-manual.md`.
- Per-agent stations/workspaces.
- Memory, reflection, beliefs, records, post-mortems and restore points.
- Agent growth/performance tracking.
- Toolsets and capability gating.
- Execution profiles and workstation isolation.
- Approval prompts and Full Power controls.
- Task delegation/orchestration tools.
- Skills and a 73-skill library in the audited station.
- Recipes; 101 were visible in the audited station.
- Scheduled Routines.
- Active Loops such as Build/Test/Verify, Sweep & Fix and Research Loop.
- Night Shift and configurable autonomy controls.
- Quest/goal/milestone tracking.
- Shared Commander Dossier/context.
- MCP/connectors; Composio was visibly connected with 7 tools.
- Model clearance tiers (DEEP/BALANCED/FAST) and fallback chains.
- Multiple model providers.
- Per-run, per-agent, per-day and global budget controls.
- Runtime concurrency/iteration controls.
- Deliverables/Workshop Library.
- Extensions with hooks/plugins.
- Communication channels including Slack.
- Global E-STOP.

These are **observed capabilities**, not assumptions about undocumented behavior. Production use still requires targeted verification.

## Architecture Layers

### 1. User / Native Interface
- StarNet desktop UI
- Crew / Agent Dossier
- Work / Build / System views
- Comms
- Slack and other connected channels

### 2. Native Control and Orchestration
Use StarNet's native mechanisms first:
- Commander/Overseer behavior
- Task delegation
- Crew management
- Quest/goals
- Recipes
- Routines
- Loops
- Native approvals
- E-STOP

Do not create a second orchestration layer unless a concrete StarNet gap is demonstrated.

### 3. Specialized Workforce
Initial priority:
- Social media strategy
- Research/trends
- Content
- Brand/quality review
- Publishing/scheduling
- Analytics
- Knowledge curation

Later:
- Marketing
- Customer support
- Outreach
- Product strategy
- Engineering/code review
- QA
- Security
- DevOps
- Operations

### 4. Knowledge / Memory
Start with StarNet's native:
- Commander Dossier
- Agent context files
- Memory/reflection/beliefs
- Records
- seeded second-brain workspace

Only add an external knowledge vault/index/retrieval layer if testing demonstrates that native capabilities are insufficient. Obsidian remains a candidate, not a decision.

### 5. Tool / Integration Layer
Use:
- Native StarNet toolsets
- Native filesystem/workbench capabilities
- MCP
- Composio
- Slack
- Approved external APIs/services

Each agent receives only the capabilities required for its responsibility.

### 6. Model Layer
Use StarNet's native clearance/routing model:

- **DEEP** — strategy, architecture, difficult decisions and high-value evaluation.
- **BALANCED** — planning, research synthesis, normal specialist work and review.
- **FAST** — classification, tagging, formatting, simple summaries and routine tasks.

Use fallback chains where appropriate. Avoid vendor-specific business logic.

### 7. Automation
Prefer StarNet-native:
- Recipes
- Routines
- Active Loops
- Night Shift
- Event/channel triggers where available

Do not introduce an external workflow platform until native mechanisms are shown to be insufficient.

### 8. Observability and Cost
Use StarNet and provider telemetry for:
- agent activity
- runs
- errors
- tokens
- model usage
- spend
- retries
- workflow state

The audited OpenRouter logs showed several ~34K–37K input-token requests with tiny outputs. Context efficiency is therefore an immediate optimization target.

### 9. Governance
Cross-cutting controls:
- least privilege
- approval gates
- execution profiles
- budget caps
- model limits
- E-STOP
- secret isolation
- auditability
- controlled autonomy

Global Full Power remains OFF.

## Target Data Flow

`User → StarNet/Slack → Native Orchestration → Specialist → Relevant Knowledge/Memory → Tool/MCP → Evaluation → Approval if required → External Action → Monitoring → Record/Learning`

Not every request requires every stage. Simple tasks should take the shortest safe path.

## Native-vs-External Rule

Before adding another platform:

1. Does StarNet already provide the capability?
2. Is the native implementation sufficient?
3. Can MCP/Composio provide the missing integration?
4. Can a small supporting service solve the remaining gap?
5. Only then consider a separate platform.

## Scaling Rule

Add an agent only when it has a genuinely distinct responsibility. More agents increase coordination overhead, context usage and failure surface.
