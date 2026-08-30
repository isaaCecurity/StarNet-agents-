# StarNet Configuration Inventory

> This file records the **observed live configuration/capabilities from the StarNet screenshots supplied on 2026-08-30**. Unknown values remain explicitly unknown.

## Platform

- StarNet version/build: `UNKNOWN`
- Workspace/project name: current UI contains stale `Undeify` references; canonical organization name/context is not yet configured.
- Primary runtime/interface: StarNet local desktop application.
- Communication: Slack connected; other channel types are supported by the UI.
- Current provider used during setup: OpenRouter.
- Global Full Power: **OFF**.
- E-STOP: **ENGAGED**; scheduling, loops and Night Shift are stopped/halting.

## Existing Crew Observed

| Agent | Observed role | Model | Tools/MCPs | Permissions | Status/notes |
|---|---|---|---|---|---|
| JUNIOR | Overseer / general agent | UNKNOWN | Orchestration/tool access implied | **FULL POWER** | Level 2; 52 runs shown |
| TOBI WEB DESIGNER | Web Designer | UNKNOWN | Capability-gated | ASK for risky actions | Idle |
| ALICE PRODUCT MAN | Product Manager | UNKNOWN | Capability-gated | ASK for risky actions | Idle |
| KEN DEVOPS ENG | DevOps Engineer | MiniMax M2.7 (free), HIGH effort shown | Capability-gated | ASK for risky actions | Idle |
| JEFF ENGINEER | Engineer | UNKNOWN | Capability-gated | ASK for risky actions | Idle |
| BOB QA TESTER | QA Tester | UNKNOWN | Capability-gated | ASK for risky actions | Idle |
| Agent 7 | Not verified | UNKNOWN | UNKNOWN | UNKNOWN | Do not assume existence |
| Agent 8 | Not verified | UNKNOWN | UNKNOWN | UNKNOWN | Do not assume existence |

The previous project notes assumed approximately eight agents. Only six are clearly identified by the supplied screenshots. The remaining two must be verified in the live Crew view before documentation is finalized.

## Agent Configuration Model Observed

Each agent has a station and dossier. Config exposes structured prompt files:

- `identity.md`
- `purpose.md`
- `context.md`
- `operating-manual.md`

The UI also exposes Brief, Growth, Record and Memory views.

## Native Capabilities Verified

### Workstations / Execution
Observed execution profiles include:
- Safe Cell
- Remote SSH
- Station Gear
- Trusted Project
- This Computer

Trusted Project was shown as an option that limits access to approved project folders.

### Toolsets
Observed native groups include:
- Comms Relay
- File Cabinet
- Workbench
- Task Delegation

Visible examples include filesystem tools (`fs.read`, `fs.list`, `fs.search`, `fs.write`, `fs.append`, `fs.edit`, `fs.patch`), shell/workbench/browser tools, communication tools and team delegation tools.

### Task Delegation / Orchestration
Visible tools include:
- `team.dispatch`
- `team.spawn`
- `team.summon`
- `team.subagents`
- `team.steer`
- `team.interrupt`
- `team.resume`
- `routine.list`

The UI indicates these tools require an orchestrator on the station. Determine whether JUNIOR is intended to fill that role before changing agent permissions.

### Capabilities / Permissions
Observed capability controls include:
- Compute
- Web Search
- Web Fetch
- Call an API
- Read Files
- Write Files
- Memory
- Terminal

Capabilities can be enabled or configured to ask for approval. The station/workstation loadout forms part of the permission boundary.

## Memory / Knowledge

Native features observed:
- Reflection with proposed memories requiring user decision.
- Stored beliefs with provenance.
- Agent run records.
- Dead-run post-mortems.
- Insights.
- Restore points.
- Shared Commander Dossier.
- Seeded `second-brain/` workspace in Deliverables/Workshop.

No external knowledge stack has been selected.

## Skills / Recipes

- Skill Library: **73 skills** observed.
- Agent-created skills: **none observed**.
- Skill Exchange: supported, with package inspection/provenance/guarding.
- Recipes: **101 recipes** observed across Developer, Research, Creator, Work, Business, Money, Data and General categories.

## Automation

### Routines
Native scheduled routines exist. Two visible away-work routines:
- KEN DevOps/deployer — every 6 hours — failed with `missing terminal outcome`.
- JEFF Engineer/engineer — every 6 hours — failed with `missing terminal outcome`.

Both are currently prevented from running by E-STOP.

### Active Loops
Native loops observed:
- Build / Test / Verify
- Sweep & Fix
- Research Loop

No active loops were observed.

### Night Shift
Native unattended/night operation exists. Currently halted by E-STOP.

### Autonomy
Controls observed include:
- Initiative: WAIT / SUGGEST / AUTO / FREE
- Reach: OBSERVE / SANDBOX / SEND & PUBLISH
- Pace
- Focus
- Off-limits
- While-away modes including WAIT / SUGGEST / BUILD (DRAFTS) / FREE

Do not enable unrestricted autonomy yet.

## Goals / Deliverables

### Quest
Native goal + milestone tracking exists. Current quest content is stale because it still references connecting Composio/GitHub/Google Drive as a future step.

### Deliverables / Workshop
Native output/workshop library exists. A seeded second-brain workspace was visible.

## MCP / Connectors

| Connector | Observed state | Notes |
|---|---|---|
| Composio | **CONNECTED** | 7 tools visible |
| Slack | **CONNECTED** | Intended for command/notification/approval |
| GitHub | Requires verification | Existing Quest references it; do not assume authentication |
| Google Drive | Requires verification | Existing Quest references it; do not assume authentication |

## Models / Providers

Native model controls observed:
- Clearance tiers: **DEEP / BALANCED / FAST**.
- Per-agent model pinning versus station default.
- Fallback chain supporting up to 8 models.
- Provider choices visible include OpenRouter, StarNet Managed, ChatGPT/Codex, Grok, MiniMax, OpenAI API and Anthropic.

KEN was visibly configured with **MiniMax M2.7 (free)** and HIGH effort.

OpenRouter was shown as **key saved / not verified** in the provider configuration screenshots. Verify before paid operation.

## Budget / Cost

Native hard USD budget controls exist for:
- Per Run
- Per Agent
- Per Day
- Global

Budget screenshot showed:
- Spent today: **$0.00**
- Lifetime: **$0.00**
- 60 runs

OpenRouter activity screenshots separately showed approximately:
- 5.44M tokens in the displayed past-month period
- 211 requests
- $0.01 spend
- ~50% cache hit rate
- ~3.33M tokens attributed to the Agents API key

These are different accounting scopes. Do not equate StarNet's token counter with billing.

## Token Efficiency Finding

Multiple OpenRouter log entries showed approximately **34K–37K input tokens** for very small outputs. This is currently the highest-priority cost/context investigation.

Before paid-model scaling, identify what StarNet is injecting into these requests and test whether context/retrieval/history can be reduced.

## Runtime

Runtime controls observed:
- Max iterations: `0` = unlimited/default.
- Max concurrent agents: `0` = unlimited/default.
- Keep computer awake.
- Launch at login.
- Start minimized to tray.
- Close to tray/background operation.

Consider conservative concurrency/iteration limits before enabling autonomous workflows.

## Extensions

Native Extensions support:
- Hooks that can run before/after actions and can block actions.
- Plugins that can listen to events and retain state.

No custom plugins were observed.

## Global Safety State

- Global Full Power: **OFF**.
- E-STOP: **ENGAGED**.
- JUNIOR: **FULL POWER** — review before production.
- Other clearly observed crew: ASK for risky operations.

## Configuration To Verify Next

- [ ] Exact StarNet version/build.
- [ ] Exact full Crew list (including possible 7th/8th agents).
- [ ] JUNIOR's intended orchestrator role and minimum required permissions.
- [ ] Full per-agent model/tool/workstation configuration.
- [ ] Composio authentication and available integrations.
- [ ] GitHub authentication.
- [ ] Google Drive authentication.
- [ ] Exact contents/behavior of seeded second brain.
- [ ] Actual source of 34K–37K token contexts.
- [ ] Safe model fallback chain.
- [ ] Conservative budget values.
- [ ] Runtime concurrency/iteration limits.
- [ ] Failure cause of KEN/JEFF routines.

## Security Rule

Never store API keys, OAuth tokens, cookies, private keys or other secrets in this file or anywhere in the repository.
