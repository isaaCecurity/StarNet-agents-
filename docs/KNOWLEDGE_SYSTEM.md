# Knowledge and Memory System

## Current Decision

Do **not** select or install Obsidian, a vector database, or an external retrieval service yet.

The StarNet audit established that the installed runtime already provides native memory/reflection, beliefs with provenance, records/post-mortems, agent context files, a shared Commander Dossier and a seeded `second-brain/` workspace.

We will test these native mechanisms first. An external knowledge layer remains a candidate only if a concrete capability gap is demonstrated.

## Objective

Provide durable organizational/project knowledge while giving agents the smallest relevant context required for a task.

## Current Native-First Architecture

`Commander Dossier + agent context + StarNet memory/records + seeded second brain → StarNet retrieval/context → agent`

Potential future extension, only if required:

`Local Markdown/Obsidian → indexing/retrieval → MCP/tool → StarNet agents`

## Knowledge Domains

Conceptually retain separation between:

```text
Organization/
Products/
Marketing/
Research/
Decisions/
Lessons-Learned/
Archive/
```

The exact filesystem/vault structure will be created only after native capability testing.

## Native Components to Evaluate

### Commander Dossier
Shared station-level context that folds into agent briefings.

### Agent Context
`context.md` provides project/domain context for an individual agent.

### Memory / Reflection
StarNet can propose memories after work; the user can keep, edit or discard them.

### Beliefs
Stored beliefs retain provenance to the run that produced them.

### Records
Run history, insights, post-mortems and restore points provide operational history.

### Seeded Second Brain
A `second-brain/` workspace already exists in the audited station. Its structure and retrieval behavior must be tested before adding another knowledge product.

## Retrieval Rules

1. Identify task/project first.
2. Apply permissions and scope.
3. Retrieve only relevant context.
4. Prefer deterministic/local filtering before expensive semantic reasoning.
5. Preserve provenance/source references.
6. Do not inject the entire knowledge base by default.
7. Measure token usage before and after retrieval/context changes.

## Memory Types

- Working/task context
- Project/product knowledge
- Organization-wide context
- Durable decisions and lessons
- Agent-specific memories/beliefs

## Knowledge Integrity

Authoritative business facts must not be silently rewritten. Important changes should preserve provenance/history. Critical policies require human review before modification.

## Security

Never place API keys, passwords, OAuth tokens, cookies, private keys or other secrets in the knowledge system, prompts, memory notes or GitHub repository.

## Evaluation Plan

Before adopting external retrieval, test:
- context relevance
- missing-context rate
- irrelevant-context rate
- retrieval latency
- tokens injected per task
- task success rate
- repeatability

The key question is not "which note-taking app is best?" It is:

> **Can StarNet reliably retrieve the smallest trusted context needed for the job?**
