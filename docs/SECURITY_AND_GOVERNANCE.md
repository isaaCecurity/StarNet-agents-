# Security and Governance

## Core Rule

Agents are software principals, not trusted administrators. Access is granted by role and minimized by default.

## Least Privilege

Each agent should have explicit access to:
- allowed tools
- allowed projects
- allowed knowledge paths
- allowed communication channels
- allowed external actions

Everything else is denied.

## Secrets

- Never commit secrets to GitHub.
- Use environment variables or a dedicated secret manager.
- Do not put credentials in prompts, memory notes or logs.
- Separate production credentials from development credentials.

## Human Approval

Human approval is required initially for:
- public social posts
- sensitive emails/messages
- production deployments
- destructive file/data operations
- financial actions
- security-sensitive configuration changes
- changes to critical policies

## Sandboxing

Untrusted code and risky automation should run in isolated environments. Production systems should not be the default workspace for agents.

## Auditability

Record:
- who/what initiated a task
- workflow ID
- agent actions
- tools called
- relevant outputs
- approvals
- final external actions
- failures

## Emergency Controls

The system should eventually provide:
- global pause
- per-agent disable
- per-workflow disable
- credential revocation
- spending limit enforcement

## Knowledge Integrity

Agents must not silently rewrite authoritative business facts. Major decisions should have provenance and version history.
