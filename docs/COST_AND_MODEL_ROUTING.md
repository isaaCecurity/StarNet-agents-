# Cost and Model Routing

## Objective

Keep the AI workforce affordable and predictable while reserving strong reasoning for tasks where it materially improves outcomes.

## Routing Principles

### High reasoning
Use for:
- strategy
- architecture
- complex planning
- difficult debugging
- security decisions
- ambiguous/high-impact evaluations

### Medium reasoning
Use for:
- content creation
- research synthesis
- normal implementation assistance
- code review
- test analysis

### Low cost / fast
Use for:
- classification
- tagging
- formatting
- simple summaries
- routine metadata operations
- deterministic tool selection

## Context Budget

Before calling an expensive model:
1. retrieve relevant context
2. remove irrelevant material
3. deduplicate
4. limit history to what is needed
5. use deterministic tools where possible

## Measurement

Track:
- tokens by agent
- tokens by workflow
- cost by model
- cost per successful task
- average latency
- retries
- context size

The all-time token counter is useful for trend monitoring but is not sufficient for understanding why usage occurred. Investigate per-task/per-agent usage.

## Budget Controls

The implementation should support:
- provider spending limits
- per-agent limits
- per-workflow limits
- rate limits
- maximum retries
- maximum context size
- fallback models

## Model Portability

Agent definitions should describe capabilities rather than hard-code business logic around a single model vendor. Model assignments can change as quality and pricing change.
