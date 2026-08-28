# Knowledge and Memory System

## Objective

Create a durable second brain that humans can understand and maintain while agents can retrieve precise context without scanning the entire knowledge base.

## Proposed Architecture

`Local Markdown knowledge → indexing/search → retrieval layer → MCP/tool → StarNet agents`

Obsidian is the preferred human-facing/local knowledge layer for the initial implementation because Markdown keeps the knowledge portable. The retrieval layer is intentionally separate so the project can replace the UI or indexing technology later.

## Knowledge Domains

```text
Knowledge Vault/
├── Organization/
│   ├── Vision.md
│   ├── Principles.md
│   ├── Brand/
│   ├── Strategy/
│   └── Operations/
├── Products/
│   ├── BigFlow/
│   ├── Shift-OS/
│   ├── Lingora/
│   └── Mind-Flow/
├── Marketing/
├── Research/
├── Decisions/
├── Lessons-Learned/
└── Archive/
```

## Retrieval Rules

1. Identify the task/project first.
2. Filter by metadata and permissions.
3. Search locally/lexically where possible.
4. Use semantic/vector retrieval where it improves recall.
5. Return only relevant documents/chunks.
6. Preserve source references.
7. Give the reasoning model only the context it needs.

## Memory Types

- Working memory: current task and temporary context.
- Project memory: architecture, requirements, current state and product facts.
- Organizational memory: principles, strategy, brand and operating rules.
- Long-term memory: durable lessons, decisions and patterns.

## Memory Agent

The memory agent acts as a librarian/curator. It can turn rough notes into structured records, suggest tags/links, detect duplication and propose canonical updates.

It should **not** silently delete information or invent facts. Important changes should preserve source and history.

## Canonical Source Rule

For each important subject, maintain one authoritative document. Other notes should link to it rather than creating competing “final” versions.

## Security

Do not place API keys, passwords, OAuth tokens, private credentials or sensitive secrets in the knowledge vault. Apply agent-level path and topic permissions.

## Token-Efficiency Objective

The knowledge system exists partly to reduce context waste. A successful retrieval should answer: “What is the smallest set of trusted information required for this task?”

## Evaluation

Measure retrieval quality using:
- relevance of returned context
- missing-context rate
- irrelevant-context rate
- latency
- token usage before/after retrieval
- agent task success rate
