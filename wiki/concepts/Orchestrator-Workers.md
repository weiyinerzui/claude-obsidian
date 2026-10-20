---
type: concept
title: "Orchestrator-Workers"
address: c-000074
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
  - "[[Parallelization (LLM)]]"
  - "[[智能体工作流]]"
---

# Orchestrator-Workers

An agentic workflow pattern where a central LLM dynamically breaks down tasks, delegates them to worker LLMs, and synthesizes their results. The orchestrator decides what subtasks are needed based on the specific input.

## Key Distinction

Topographically similar to [[Parallelization (LLM)]], but the critical difference is **flexibility**: subtasks aren't pre-defined but determined by the orchestrator based on the specific input. The orchestrator can also adapt subtasks dynamically as workers return results.

## When to Use

Best for complex tasks where you can't predict the subtasks needed in advance.

## Examples

- **Coding**: complex changes requiring edits to multiple files — the number and nature of file changes depend on the specific task
- **Search**: gathering and analyzing information from multiple sources, where the orchestrator decides what to search and how to combine findings

## Relationship to [[智能体工作流]]

[[智能体工作流]] describes a similar role-based decomposition (with specific roles like wanderer, explorer, interpreter, outline-organizer, writer, critic, reviser). The Orchestrator-Workers pattern provides the *technical architecture* for dynamic task delegation, while [[智能体工作流]] provides the *creative domain roles*.
