# Cost and Model Routing

## Objective

Keep the AI workforce affordable and predictable while reserving stronger reasoning for tasks where it materially improves outcomes.

## Native StarNet Strategy

The audit confirmed that StarNet already provides:
- DEEP / BALANCED / FAST model clearance tiers.
- Per-agent model pinning versus station default.
- A fallback chain supporting up to 8 models.
- Provider selection.
- Hard USD budget controls for per-run, per-agent, per-day and global limits.
- Runtime controls for concurrency and iterations.

Therefore **do not build a separate model router or budget system unless a concrete native gap is demonstrated.**

## Routing Policy

### DEEP
Use for:
- strategy
- architecture
- difficult planning
- high-impact decisions
- complex evaluation
- security-sensitive reasoning

### BALANCED
Use for:
- research synthesis
- content creation
- normal specialist work
- planning
- code review/test analysis

### FAST
Use for:
- classification
- tagging
- formatting
- simple summaries
- routine metadata operations
- deterministic tool selection

These are policy targets; exact model assignments will be selected after cost/quality testing.

## Current Evidence

The supplied OpenRouter screenshots showed approximately:
- 5.44M tokens in the displayed past-month period.
- 211 requests.
- $0.01 spend.
- ~50% cache hit rate.
- ~3.33M tokens attributed to the Agents API key.

A separate StarNet budget screen showed:
- $0.00 spent today.
- $0.00 lifetime spend.
- 60 runs.

These counters have different scopes and must not be treated as equivalent.

## Critical Context-Efficiency Finding

Several OpenRouter log entries showed approximately **34K–37K input tokens** with very small outputs.

This is the current priority because large prompts can become expensive when a paid model is used. Before scaling the workforce:

1. Identify what StarNet injects into each request.
2. Determine whether full histories, prompts, memories, skills or workspace context are being included.
3. Reduce irrelevant context.
4. Prefer focused retrieval and deterministic filtering.
5. Measure tokens before/after each change.

## Budget Policy

Before paid-model experimentation, configure conservative values for:
- per-run cap
- per-agent cap
- per-day cap
- global cap

Never rely on the model/provider price alone as a safety mechanism.

## Runtime Policy

The audited runtime showed:
- max iterations = 0 (unlimited/default)
- max concurrent agents = 0 (unlimited/default)

Review these before enabling autonomous workflows to avoid accidental concurrency/token spikes.

## Measurement

Track where StarNet/provider telemetry allows:
- input tokens
- output tokens
- cache hits
- cost by model
- cost by agent
- cost by workflow
- retries
- latency
- successful task cost
- context size

## Model Portability

Agent definitions should describe capabilities and responsibilities rather than hard-code business logic to one vendor. Use StarNet's provider/fallback mechanisms and change models as quality/pricing changes.
