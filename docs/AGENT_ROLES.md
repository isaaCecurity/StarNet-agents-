# Agent Roles

## Role Design Principles

Each agent gets a narrow responsibility, explicit tools, explicit knowledge scope, a defined output format, and an escalation path.

## Initial Social-Media Workforce

### Social Media Strategist
**Purpose:** Turn business goals into content strategy.

**Can:** read organization brand rules, audience definitions, product positioning and approved analytics.

**Cannot:** publish directly; change brand rules; access secrets.

### Research / Trend Agent
**Purpose:** Find relevant topics, trends, competitors and supporting information.

**Can:** use approved web/research tools and public sources.

**Cannot:** treat unverified claims as facts or publish externally.

### Content Creation Agent
**Purpose:** Draft posts, threads, captions, hooks, scripts and content variants.

**Can:** read brand voice and approved product information.

**Cannot:** publish or invent product claims.

### Brand / Quality Reviewer
**Purpose:** Independently check drafts for accuracy, tone, clarity, brand consistency and risk.

**Can:** reject or request changes.

**Cannot:** silently rewrite core business facts.

### Publishing / Scheduling Agent
**Purpose:** Execute approved publishing/scheduling actions.

**Can:** access only approved social accounts/tools.

**Cannot:** publish unapproved content.

### Analytics Agent
**Purpose:** Analyze performance and recommend improvements.

**Can:** read approved metrics.

**Cannot:** alter historical metrics or publish conclusions as facts without evidence.

### Knowledge / Memory Agent
**Purpose:** Curate durable organizational knowledge.

**Can:** classify, link, summarize and propose updates.

**Cannot:** destructively delete important knowledge or invent facts.

## Future Roles

- Commander
- Orchestrator
- Strategy Agent
- Planning/Architect Agent
- Evaluation Agent
- Backend Agent
- Frontend Agent
- QA Agent
- Security Agent
- DevOps Agent
- Customer Support Agent
- Email/Outreach Agent
- Finance/Operations Agent
- System Architect Agent

## Permission Model

Default: **deny**. An agent receives access only to the tools, projects, folders and data required for its job.

Public posting, external messaging, production changes, destructive operations and credential-sensitive operations require explicit policy and normally human approval.
