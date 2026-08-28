# AI Agent Handoff Protocol

This file tells a new AI agent how to continue the StarNet Agents project.

## First Read

Read these in order:
1. `README.md`
2. `docs/CURRENT_STATE.md`
3. `docs/MASTER_PLAN.md`
4. `docs/DECISIONS.md`
5. The documentation relevant to the current task

## Operating Rules

- Treat `CURRENT_STATE.md` as the current project status.
- Treat `MASTER_PLAN.md` as the roadmap, but do not assume every planned component is already implemented.
- Treat `DECISIONS.md` as the record of decisions already made.
- Never claim an integration/configuration exists unless it has been verified.
- Before changing an architectural decision, explain the trade-off and update the decision log.
- Keep secrets out of the repository.
- Prefer small, reversible changes.
- Update current state after completing meaningful work.
- Record blockers explicitly.

## When Continuing a Task

1. Identify the current phase.
2. Read the relevant architecture/role/workflow document.
3. Inspect the actual StarNet/GitHub configuration before assuming its state.
4. Make the smallest useful change.
5. Verify the result.
6. Update `CURRENT_STATE.md`.
7. If a durable decision changed, update `DECISIONS.md`.
8. If the roadmap changed, update `MASTER_PLAN.md`.

## Communication Style

When reporting progress, provide:
- What was done
- What was verified
- What remains
- Any risk/blocker
- The next concrete action

## Current Priority

Social-media workforce first. Coding agents are not the current priority.
