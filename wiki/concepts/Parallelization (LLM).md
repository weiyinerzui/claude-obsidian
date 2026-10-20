---
type: concept
title: "Parallelization (LLM)"
address: c-000073
created: 2026-06-09
updated: 2026-06-09
tags:
  - concept
  - agent
  - workflow
  - pattern
status: developing
related:
  - "[[Building Effective Agents]]"
  - "[[Orchestrator-Workers]]"
  - "[[Augmented LLM]]"
  - "[[Evaluator-Optimizer]]"
---

# Parallelization (LLM)

An agentic workflow pattern where LLMs work simultaneously on a task and their outputs are aggregated programmatically. Manifests in two key variations.

## Variations

### Sectioning
Breaking a task into independent subtasks run in parallel. Each subtask gets focused attention from a dedicated LLM call.

- **Example**: Implementing guardrails — one model instance processes user queries while another screens for inappropriate content. Performs better than having the same LLM handle both.
- **Example**: Automated evals — each LLM call evaluates a different aspect of the model's performance on a given prompt.

### Voting
Running the same task multiple times to get diverse outputs, then aggregating results.

- **Example**: Code vulnerability review — several different prompts review and flag code if they find a problem.
- **Example**: Content moderation — multiple prompts evaluate different aspects or require different vote thresholds.

## When to Use

Effective when subtasks can be parallelized for speed, or when multiple perspectives are needed for higher confidence. LLMs generally perform better when each consideration is handled by a separate focused call.

## Related Patterns

- [[Orchestrator-Workers]] looks similar but subtasks are dynamically determined, not pre-defined
- [[Evaluator-Optimizer]] uses sequential iteration, not parallel decomposition
