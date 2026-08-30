# Current State

> Primary status document. Update this whenever meaningful project progress is made.

## Current Phase
**Phase 1 — StarNet Native Audit completed; Phase 1B — Station Hardening / Configuration is next.**

The project is **not yet building the Social Media workforce**. We first audited the installed StarNet runtime and found that it already provides most of the infrastructure we had planned to build externally.

## Critical Architecture Correction

StarNet is **already the runtime/application we are using**. It is a local desktop AI-agent harness with a graphical station interface. We are not building a separate web application or replacement dashboard.

The `StarNet-agents-` GitHub repository is the project control/documentation layer for configuring, governing, extending and operating the StarNet runtime as a personalized AI organization.

## Audit Result — Native StarNet Capabilities Verified

Based on the supplied StarNet screenshots/settings archive, the installed system already provides the following native primitives:

- Agent dossiers with structured `identity.md`, `purpose.md`, `context.md` and `operating-manual.md` files.
- Crew/agent classes and recruitment; the observed Recruitment Bay exposes 35 classes (7 Code, 13 Research, 15 Ops).
- Per-agent workstations/stations.
- Native memory, reflection, beliefs, records, post-mortems and restore points.
- Agent growth/performance tracking.
- Native toolsets and capability gating.
- Execution profiles including Safe Cell, Remote SSH, Station Gear, Trusted Project and This Computer.
- Approval controls and Full Power controls.
- Task delegation/orchestration tooling including `team.dispatch`, `team.spawn`, `team.summon`, `team.subagents`, `team.steer`, `team.interrupt`, `team.resume` and routine tools.
- Native skills and a Skill Library; the audit showed 73 skills.
- Native agent-created skills (currently none created).
- Skill Exchange with inspection/provenance/guarding.
- Native Recipes; the audit showed 101 recipes.
- Native scheduled Routines.
- Native Active Loops including Build/Test/Verify, Sweep & Fix and Research Loop.
- Night Shift autonomous operation.
- Autonomy controls for initiative, reach, pace, focus and off-limits.
- Native Quest/goal and milestone tracking.
- Commander Dossier shared into agent briefings.
- MCP/connectors; Composio was visibly connected with 7 tools.
- Model clearance/routing tiers: DEEP, BALANCED and FAST.
- Model fallback chains, up to 8 models.
- Multiple provider options including OpenRouter and other providers shown in the UI.
- Native budgets/spend controls including per-run, per-agent, per-day and global limits.
- Runtime concurrency/iteration controls.
- Deliverables/Workshop Library.
- Extensions with hooks and plugins.
- Connected communication channels including Slack and other channel types shown by the UI.
- Global E-STOP/emergency control.

These capabilities should be treated as the **current observed StarNet feature set**, while exact behavior should still be verified during configuration/testing before being relied upon in production workflows.

## Current Crew Observed

The supplied screenshots clearly show these six agents:

| Agent | Observed role | Observed state / notes |
|---|---|---|
| JUNIOR | Overseer / general agent | Level 2; 52 runs shown; currently Full Power |
| TOBI WEB DESIGNER | Web Designer | Idle; approval mode shown |
| ALICE PRODUCT MAN | Product Manager | Idle; approval mode shown |
| KEN DEVOPS ENG | DevOps Engineer | Idle; MiniMax M2.7 (free), HIGH effort shown |
| JEFF ENGINEER | Engineer | Idle; approval mode shown |
| BOB QA TESTER | QA Tester | Idle; approval mode shown |

The earlier working assumption was approximately eight agents. The supplied audit screenshots clearly identify six; the remaining two are **not documented until their existence/configuration is verified**. Do not invent them.

## Important Current Permission State

- Global **Full Power — Whole Station: OFF**.
- JUNIOR is currently configured with **FULL POWER**.
- The other five clearly observed agents are configured to **ASK** for risky actions.
- This is a temporary/exploratory configuration and must be reviewed before production use.
- Do not enable global Full Power.

## Automation State

- Scheduling is currently **STOPPED by E-STOP**.
- Active Loops are **STOPPED by E-STOP** and no active loops were observed.
- Night Shift is **HALTED by E-STOP**.
- Two existing six-hour away-work routines for KEN and JEFF were visible and both showed a failure state with **“missing terminal outcome”**; they should not be re-enabled until diagnosed.

## Current Knowledge / Memory State

StarNet already provides native memory and a seeded second-brain workspace. JUNIOR's screenshots showed:

- Reflection with proposed memories requiring user approval.
- Stored beliefs with provenance back to originating runs.
- 42 beliefs visible for JUNIOR in the supplied screenshot.
- Record/run history, dead-run post-mortems and restore points.
- A shared Commander Dossier that is currently incomplete/stale.
- A seeded `second-brain/` workspace in the Deliverables/Workshop area.

Therefore **Obsidian/external retrieval is not yet selected**. Native StarNet memory, Commander Dossier, context files and the seeded second brain must be evaluated first.

## Current MCP / Integration State

- **Composio:** visibly connected; 7 tools shown.
- **Slack:** connected and intended for command/notification/approval flows.
- GitHub/Google Drive were referenced by the existing Quest, but their exact authenticated connection state must be verified rather than assumed.
- No API keys or secrets belong in this repository.

## Model / Cost Findings

OpenRouter activity screenshots showed approximately:

- **5.44M token volume** for the displayed past-month period.
- **211 requests**.
- **$0.01 total spend** for the displayed period.
- Approximately **50% cache hit rate**.
- Agents API key activity around **3.33M tokens** was visible.

Individual logs showed several requests with roughly **34K–37K input tokens** and very small outputs. This is the primary current cost-efficiency concern.

A separate StarNet budget screenshot showed:

- **$0.00 spent today**
- **$0.00 lifetime spend**
- **60 runs**

These counters do not appear to represent the same accounting scope as the OpenRouter activity screen. Therefore the previous ~2.5M StarNet token figure must **not** be interpreted as equivalent to paid spend.

## Current Product Context

The organization is currently focused on SaaS products:

- **BigFlow** — nearly finished; backend more than halfway complete, frontend partly complete, tests already done.
- **Shift OS** — friend is nearly finished.
- **Lingora** — planned/in progress.
- **Mind Flow** — planned/in progress.

Long term, the organization may expand beyond SaaS into other businesses/services.

## Current Strategic Priority

The first real StarNet workforce will be **Social Media / Marketing**, not coding.

The user intends to continue coding BigFlow personally for now.

## Revised Target Architecture

```text
YOU
  │
  ├── StarNet UI / Slack / channels
  │
  ▼
STARNet STATION / COMMANDER
  │
  ├── Commander Dossier / shared context
  ├── Crew / Agents
  ├── Native Memory / Records / Growth
  ├── Toolsets / Permissions / Approvals
  ├── Models / Fallback / Budgets
  ├── Recipes / Routines / Loops / Night Shift
  ├── Quest / Deliverables / Skills
  └── MCP / Connectors
           │
           ▼
     SPECIALIZED WORKFORCE
           │
           ▼
      EXTERNAL ACTIONS
           │
           ▼
    EVALUATION / MONITORING
           │
           ▼
    MEMORY / LESSONS LEARNED
```

External infrastructure is added only where StarNet has a demonstrated capability gap.

## Decisions Confirmed by the Audit

- Do **not** build a replacement web dashboard.
- Do **not** build a custom orchestration engine while StarNet's native delegation exists.
- Do **not** build a custom scheduler/workflow engine before testing StarNet Recipes, Routines and Loops.
- Do **not** build a custom approval/budget/model-fallback system before testing StarNet's native controls.
- Do **not** choose Obsidian yet; evaluate native StarNet memory/second-brain capabilities first.
- Do **not** recruit more agents yet.
- Do **not** make coding automation the primary use case.
- Keep global Full Power OFF.
- Keep E-STOP engaged until automation is deliberately configured.
- High-impact external actions require human approval during the initial deployment.
- Treat context reduction/retrieval as a priority because observed requests can carry 34K–37K input tokens.

## Immediate Next Tasks

1. Update and verify the Commander Dossier with the real organization/product context.
2. Complete configuration records for the six observed agents and verify whether two more agents actually exist.
3. Review JUNIOR's Full Power authority and determine the minimum authority needed for orchestration.
4. Verify Composio, Slack, GitHub and Google Drive connection states.
5. Map existing agent capabilities/toolsets/workstations/permissions into a least-privilege matrix.
6. Set conservative StarNet budget/model/concurrency controls before paid-model experimentation.
7. Diagnose the failed KEN/JEFF away-work routines before enabling scheduling.
8. Test native memory, Commander Dossier and seeded second-brain retrieval before selecting an external knowledge stack.
9. Investigate the 34K–37K input-token pattern and identify what context is being injected.
10. Only after the above: design/configure the first Social Media workforce and draft-only workflow.

## Do Not Do Yet

- Do not build a separate web dashboard.
- Do not add another orchestration layer without a demonstrated StarNet gap.
- Do not add more agents simply to increase headcount.
- Do not enable global Full Power.
- Do not enable Night Shift, Loops or unattended schedules until deliberately configured.
- Do not allow automatic public posting or sensitive outbound communication without approval.
- Do not select/install Obsidian or an external vector database yet.
- Do not spend the limited paid-model budget until token/context behavior is understood.
- Do not treat StarNet's all-time token counter as a billing figure.

## Last Updated
2026-08-30
