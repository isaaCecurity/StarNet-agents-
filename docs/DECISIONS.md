# Architecture Decision Log

## ADR-001 — Repository as project control center
**Decision:** Use this repository as the durable implementation and handoff record for StarNet Agents.

**Reason:** Another AI agent should be able to resume work without relying on the original conversation.

## ADR-002 — Social media first
**Decision:** The first production-oriented agent workforce focuses on social media/marketing rather than coding.

**Reason:** The user currently handles coding directly and wants to use StarNet to reduce non-coding workload first.

## ADR-003 — Human approval for high-impact actions
**Decision:** Require explicit approval before public posting, sensitive outbound communication, production changes and destructive operations during early stages.

**Reason:** Automation must be reliable before autonomy is increased.

## ADR-004 — Knowledge separated from reasoning
**Decision:** Keep durable knowledge in a human-readable source and place indexing/retrieval between that knowledge and the agents.

**Reason:** Avoid repeatedly sending the entire knowledge base to models and preserve portability.

## ADR-005 — Least privilege
**Decision:** Agents receive only the tools/data/project scope required for their role.

**Reason:** Limits security impact and prevents accidental cross-project actions.

## ADR-006 — Model routing
**Decision:** Use different model strengths by task complexity rather than one model for every agent.

**Reason:** Strong reasoning is valuable for strategy/planning, while routine tasks can use cheaper models.

## ADR-007 — Event-driven workflows
**Decision:** Prefer event/schedule triggers over continuous polling.

**Reason:** Reduces unnecessary model calls and makes automation more predictable.

## ADR-008 — Gradual autonomy
**Decision:** Start with approval-based workflows and increase autonomy only after measuring reliability.

**Reason:** External actions create real-world consequences and need evidence of safety/reliability.
