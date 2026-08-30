# StarNet Agents — Master Implementation Plan

## 0. End Goal

Configure and progressively extend the existing StarNet runtime into a personalized AI operating system/digital workforce for the user's organization.

The long-term workforce should support:
- Social media and marketing
- Research and intelligence
- Email/outreach
- Customer support
- Product/business analytics
- Engineering assistance and code review
- QA/security/DevOps
- Deployment monitoring and incident response
- Strategic planning and decision support
- Scheduling and productivity
- Multiple products and future business lines

The user remains the final authority for high-impact actions.

## 1. Phase 0 — Repository Foundation

- [x] Create repository.
- [x] Establish documentation/handoff structure.
- [x] Establish architecture/security/cost/workflow decisions.
- [x] Correctly define StarNet as the runtime and repository as project control layer.

## 2. Phase 1 — StarNet Native Audit

**Status: completed from supplied screenshots/settings.**

Verified native primitives include agents/dossiers, workstations, memory, records, skills, recipes, routines, loops, autonomy, quests, deliverables, MCP/connectors, toolsets, approvals, budgets, model tiers/fallbacks, runtime controls, extensions and E-STOP.

Exit result: the project will configure StarNet rather than rebuild equivalent infrastructure.

## 3. Phase 1B — Station Hardening and Configuration

**Current phase.**

### Objectives
Make the existing StarNet station accurate, safe, economical and ready for the first controlled workforce.

### Tasks
- [ ] Update Commander Dossier with canonical organization/product context.
- [ ] Verify complete Crew list.
- [ ] Document every existing agent's prompt structure, model, capabilities, workstation, permissions and memory.
- [ ] Review JUNIOR's Full Power authority and establish minimum orchestration permissions.
- [ ] Verify Composio, Slack, GitHub and Google Drive connection/authentication states.
- [ ] Set conservative budget/model/concurrency controls.
- [ ] Diagnose KEN/JEFF failed away-work routines.
- [ ] Keep E-STOP engaged until automation is deliberately configured.
- [ ] Test native memory and seeded second-brain behavior.
- [ ] Trace and reduce 34K–37K model input contexts.

### Exit criteria
The station has an accurate Commander context, documented agent permissions, verified integrations, safe cost controls and a measured understanding of native memory/context behavior.

## 4. Phase 2 — Knowledge Foundation

Do **not** automatically install Obsidian or an external vector database.

### First test
- Commander Dossier
- agent context files
- native memory/reflection/beliefs
- records
- seeded second-brain workspace

### Only if native capability is insufficient
Evaluate:
`Local Markdown/Obsidian → index/retrieval → MCP → StarNet`

### Exit criteria
Agents can receive focused, trusted project/organization context without unnecessary full-vault/history injection.

## 5. Phase 3 — Social Media Workforce (FIRST REAL USE CASE)

### Objective
Create the first useful, low-risk department using StarNet-native capabilities.

### Candidate responsibilities
- Strategy
- Research/trends
- Content
- Brand/quality
- Publishing/scheduling
- Analytics
- Knowledge curation

Before recruiting, evaluate StarNet's existing agent classes and determine whether each responsibility needs a distinct agent.

### Initial workflow
`Research → Strategy → Draft → Review → Human Approval → Publish/Schedule → Analytics → Lessons Learned`

Start in draft/approval mode. No automatic public posting initially.

### Exit criteria
A request can enter through StarNet/Slack, produce a researched and reviewed draft, stop for approval, and later capture performance/lessons.

## 6. Phase 4 — Workflow and Automation Expansion

Use StarNet Recipes, Routines, Active Loops and Night Shift before adding external workflow infrastructure.

Tasks:
- [ ] Define repeatable recipes.
- [ ] Define safe schedules.
- [ ] Add event-driven triggers where supported.
- [ ] Add retries/failure handling.
- [ ] Ensure external actions are idempotent where possible.
- [ ] Add approval checkpoints.
- [ ] Record workflow outcomes.

## 7. Phase 5 — Organization-Wide Workforce

Gradually add:
- Marketing
- Research
- Customer support
- Email/outreach
- Product strategy
- Analytics
- Operations
- Code review/QA
- Security
- DevOps

Do not create executive/orchestration agents unnecessarily when StarNet's native Overseer/task-delegation mechanisms can fulfill the role.

## 8. Phase 6 — Model and Cost Optimization

Use native StarNet DEEP/BALANCED/FAST tiers and fallback chains.

Tasks:
- [ ] Map roles to model tiers.
- [ ] Set budget caps.
- [ ] Measure tokens by task/agent/workflow.
- [ ] Reduce unnecessary context.
- [ ] Test caching/retrieval effects.
- [ ] Tune concurrency/iteration limits.

## 9. Phase 7 — Monitoring and Operations

Add monitoring of:
- agent activity
- workflow status
- model usage/cost
- application/deployment logs
- security events
- alerts

Use native StarNet observability first; add external systems only for demonstrated gaps.

## 10. Phase 8 — Multi-Product Organization

Isolate project context and permissions for:
- BigFlow
- Shift OS
- Lingora
- Mind Flow
- future products/businesses

Share organization-level principles/strategy where appropriate.

## 11. Phase 9 — Learning and Continuous Improvement

Capture:
- lessons
- repeated failures
- user corrections
- successful workflows
- important decisions
- architecture changes
- marketing outcomes

Use StarNet's native memory/reflection/records where sufficient. Critical policies must never silently change.

## 12. Phase 10 — Advanced Autonomy

Only after reliability evidence:
- routine autonomous research
- low-risk publishing
- bounded support responses
- safe operational remediation
- proactive recommendations
- executive briefings

High-impact actions retain human approval unless explicitly authorized.

## 13. Definition of Done — End State

The user can give a high-level objective through StarNet/Slack and the system can:
1. Understand the objective.
2. Retrieve relevant context.
3. Decide whether direct execution, planning or strategy is needed.
4. Plan and delegate through native StarNet mechanisms.
5. Execute using controlled tools.
6. Evaluate results.
7. Request approval when required.
8. Perform approved external actions.
9. Monitor outcomes.
10. Notify the user.
11. Record durable lessons.
12. Measure cost/performance.
13. Improve future workflows from evidence.

The target is a controlled digital workforce, not a collection of autonomous prompts.
