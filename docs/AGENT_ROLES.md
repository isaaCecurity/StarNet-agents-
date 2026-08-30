# Agent Roles

## Role Design Principles

Each agent should have a distinct responsibility, explicit tools/capabilities, explicit knowledge scope, a defined output expectation and an escalation path.

**Do not create an agent simply because a role appears on the long-term architecture.** First check whether an existing agent or StarNet's native agent classes can perform the responsibility cleanly.

## Existing Crew Observed

The supplied screenshots clearly identify:

- **JUNIOR** — Overseer/general agent; currently has FULL POWER and must be reviewed before production.
- **TOBI WEB DESIGNER** — Web Designer.
- **ALICE PRODUCT MAN** — Product Manager.
- **KEN DEVOPS ENG** — DevOps Engineer.
- **JEFF ENGINEER** — Engineer.
- **BOB QA TESTER** — QA Tester.

Two additional agents were previously assumed but are not clearly identified in the supplied screenshots. Their existence and configuration must be verified before documenting them.

## Native Role/Recruitment System

The audited StarNet Recruitment Bay exposes approximately **35 agent classes**:
- 7 Code
- 13 Research
- 15 Ops

The available native classes include specialized strategic/research/operational roles. Evaluate these classes before creating custom agents.

StarNet also has a native Overseer/task-delegation concept. Task Delegation tools include `team.dispatch`, `team.spawn`, `team.summon`, `team.subagents`, `team.steer`, `team.interrupt` and `team.resume`. Determine whether JUNIOR is the intended orchestrator before creating a separate Commander/Orchestrator agent.

## Initial Social-Media Workforce — Candidate Roles

These are **candidate responsibilities**, not yet-created agents:

### Social Media Strategist
**Purpose:** Turn business goals into content strategy.

**Can:** read approved organization, audience, product positioning and analytics context.

**Cannot:** publish directly or change canonical brand rules.

### Research / Trend Agent
**Purpose:** Find relevant topics, trends, competitors and supporting information.

**Can:** use approved research/web tools and public sources.

**Cannot:** treat unverified claims as facts or publish externally.

### Content Creation Agent
**Purpose:** Draft posts, threads, captions, hooks, scripts and variants.

**Can:** read approved brand voice and product information.

**Cannot:** publish or invent product claims.

### Brand / Quality Reviewer
**Purpose:** Independently check accuracy, tone, clarity, brand consistency and risk.

**Can:** reject or request changes.

**Cannot:** silently change core business facts.

### Publishing / Scheduling Agent
**Purpose:** Execute approved publishing/scheduling actions.

**Can:** access only approved social accounts/tools.

**Cannot:** publish unapproved content.

### Analytics Agent
**Purpose:** Analyze approved performance metrics and recommend improvements.

**Cannot:** alter historical metrics or present unsupported conclusions as facts.

### Knowledge / Memory Agent
**Purpose:** Curate durable organizational knowledge and lessons.

**Can:** classify, link, summarize and propose updates.

**Cannot:** silently delete authoritative knowledge or invent facts.

## Long-Term Roles

Potential roles include:
- Strategy
- Planning/Architect
- Evaluation
- Marketing
- Research
- Customer Support
- Email/Outreach
- Analytics
- Operations
- Code Review
- QA
- Security
- DevOps
- System Architecture

These remain subject to the native-agent-first rule.

## Permission Model

Default: **deny/minimize**. An agent receives only the tools, projects, folders, data and external actions required for its job.

Public posting, sensitive external messaging, production changes, destructive operations and credential-sensitive actions require explicit policy and normally human approval.
