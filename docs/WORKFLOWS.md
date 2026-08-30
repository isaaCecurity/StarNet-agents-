# Workflow Architecture

## Native-First Decision

StarNet already provides Recipes, scheduled Routines, Active Loops, Night Shift, task delegation and approval controls. Use these native mechanisms first. Do not build an external workflow engine unless testing identifies a concrete capability gap.

## Standard Logical Pattern

`Trigger → Relevant Context → Plan → Execute → Evaluate → Approval if required → External Action → Monitor → Record/Learn`

A workflow may skip stages when unnecessary. Simple tasks should take the shortest safe path.

## Initial Social Media Workflow

Target pattern:

`Research → Strategy → Draft → Brand/Quality Review → User Approval → Publish/Schedule → Analytics → Lessons Learned`

The first implementation should be **draft/approval only**. No automatic public posting until reliability and permission controls are proven.

## Native Mapping

| Requirement | StarNet-native mechanism to test first |
|---|---|
| Reusable workflow | Recipe |
| Scheduled work | Routine |
| Iterative objective | Active Loop |
| Unattended work | Night Shift / away-work controls |
| Agent delegation | Task Delegation / crew orchestration |
| Approval | Native approval prompts / channel approval |
| Context | Commander Dossier / agent context / memory |
| External integration | MCP / Composio / connectors |
| Result history | Records / Deliverables |
| Long-term goal | Quest |

## Approval Classes

### Low risk
- Internal summaries
- Draft generation
- Classification
- Tagging
- Organization
- Non-destructive analysis

### Medium risk
- Routine workflow changes
- Selected support actions
- Scheduling actions that have already been approved by policy

### High risk
- Public social posts
- Sensitive external communication
- Production deployment
- Destructive changes
- Financial actions
- Credential-sensitive operations
- Critical policy changes

High-risk actions require explicit human approval during the initial deployment.

## Automation State During Hardening

The audited station currently has E-STOP engaged. Scheduling, Active Loops and Night Shift are therefore stopped/halting. Keep this state until automation has been deliberately configured.

Two existing six-hour away-work routines for KEN and JEFF showed `missing terminal outcome` failures. Diagnose before re-enabling.

## Event-Driven Preference

Prefer event/schedule triggers over continuous polling. Candidate triggers include:
- new Slack request
- scheduled time
- new GitHub issue/PR
- deployment failure
- monitoring alert
- new analytics data

## Reliability Requirements

Any workflow with an external side effect should consider:
- idempotency
- duplicate prevention
- timeout
- retry policy
- failure notification
- audit record
- rollback/recovery where possible

## Workflow Outputs

Every completed workflow should provide:
- status
- actions taken
- important evidence
- unresolved issues
- approvals received
- cost/usage when available
- next recommended action
