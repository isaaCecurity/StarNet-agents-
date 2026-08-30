# Security and Governance

## Core Rule

Agents are software principals, not trusted administrators. Access is granted by role and minimized by default.

## Native StarNet Controls

The audit confirmed that StarNet already provides important governance primitives:
- capability/toolset gating
- workstation/execution profiles
- approval prompts
- Full Power controls
- budget limits
- runtime controls
- global E-STOP
- autonomy/reach controls
- task/delegation boundaries

Use these native controls before creating custom governance infrastructure.

## Current Safety State

- **Global Full Power: OFF.** Keep it OFF.
- **E-STOP: ENGAGED.** Keep it engaged during configuration/hardening.
- **JUNIOR: FULL POWER.** Treat this as temporary and review before production.
- Other clearly observed crew members use approval-based risky-action settings.

## Least Privilege

Each agent should have explicit access to:
- allowed tools
- allowed projects
- allowed knowledge paths
- allowed communication channels
- allowed external actions

Everything else should be denied or approval-gated.

## Approval Policy

Human approval is required initially for:
- public social posts
- sensitive emails/messages
- production deployments
- destructive file/data operations
- financial actions
- security-sensitive configuration changes
- changes to critical policies
- other irreversible/high-impact external actions

## Autonomy Policy

Begin with WAIT/SUGGEST or draft-oriented operation. Do not enable unrestricted FREE autonomy until reliability has been demonstrated.

For unattended work, prefer sandbox/draft reach over send/publish reach.

## Execution Isolation

Prefer StarNet's bounded execution profiles such as Safe Cell, Station Gear or Trusted Project for ordinary work. Do not use unrestricted host access as the default.

## Secrets

- Never commit secrets to GitHub.
- Use environment variables or a dedicated secret manager.
- Do not place credentials in prompts, memory notes or logs.
- Separate production credentials from development credentials.
- Never place secrets in the knowledge vault.

## Auditability

Record where StarNet/provider tooling permits:
- initiating user/request
- workflow/task identifier
- agent actions
- tools called
- relevant outputs
- approvals
- external actions
- failures
- cost/usage

## Emergency Controls

StarNet's global E-STOP is the first emergency control. Additional per-agent/per-workflow controls should use native mechanisms where available before custom implementation.

## Knowledge Integrity

Agents must not silently rewrite authoritative business facts. Important organizational decisions and critical policies require provenance and human review.

## Security Principle

Do not expand permissions because an agent is inconvenient to configure. First determine the exact capability needed, then grant the narrowest safe access.
