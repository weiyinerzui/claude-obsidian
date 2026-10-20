---
type: concept
title: "Prompt Chaining"
address: c-000071
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
  - "[[Augmented LLM]]"
  - "[[Routing (LLM Agent)]]"
  - "[[Evaluator-Optimizer]]"
---

# Prompt Chaining

An agentic workflow pattern that decomposes a task into a sequence of steps, where each LLM call processes the output of the previous one. Programmatic checks ("gates") can be added on any intermediate step to ensure the process is still on track.

## When to Use

Best when the task can be cleanly decomposed into fixed subtasks. The main tradeoff: higher latency for higher accuracy, by making each LLM call a simpler task.

## Examples

- Generating marketing copy, then translating it into a different language
- Writing an outline, checking it meets criteria, then writing the full document

## Notable Properties

- **Gates** — programmatic checks between steps, enabling early termination if criteria aren't met
- **Predictable** — fixed flow makes behavior consistent and debuggable

## Related Patterns

- [[Routing (LLM Agent)]] can be used *within* a chain step to dispatch to specialized sub-handlers
- [[Evaluator-Optimizer]] uses a loop instead of a linear sequence, more suited for refinement than decomposition
