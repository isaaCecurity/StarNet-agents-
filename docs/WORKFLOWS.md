# Workflow Architecture

## Standard Pattern

`Trigger → Context → Plan → Execute → Evaluate → Approval → External Action → Monitor → Record`

A workflow may skip stages when they are unnecessary, but high-impact actions must retain the appropriate controls.

## Social Media: First Workflow

### Request
User sends a request through Slack.

### Flow
1. Strategy agent interprets objective.
2. Research agent gathers supporting information.
3. Content agent drafts variants.
4. Brand/Quality agent reviews.
5. Slack approval is requested.
6. Publishing agent schedules/posts only after approval.
7. Analytics agent measures results later.
8. Memory agent records useful lessons.

## Approval Classes

### Low risk
Internal summaries, draft generation, tagging and organization.

### Medium risk
Scheduling non-sensitive content, routine workflow changes and selected customer-support actions.

### High risk
Public posting, sensitive external communication, production deployment, destructive changes, financial actions and credential-sensitive operations.

High-risk actions require explicit human approval initially.

## Event-Driven Automation

Prefer triggers such as:
- new Slack request
- scheduled time
- new GitHub issue/PR
- deployment failure
- monitoring alert
- new analytics data

Avoid continuous agent polling when an event trigger can perform the same job.

## Reliability Requirements

Every workflow that can cause an external side effect should consider:
- idempotency
- duplicate prevention
- timeout
- retry policy
- failure notification
- audit record
- rollback/recovery where possible

## Workflow Outputs

Every completed workflow should provide a concise result containing:
- status
- actions taken
- important evidence
- unresolved issues
- approvals received
- cost/usage when available
- next recommended action
