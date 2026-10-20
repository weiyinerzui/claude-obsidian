---
type: entity
title: "Anthropic"
address: c-000069
created: 2026-06-09
updated: 2026-06-09
tags:
  - entity
  - organization
  - ai-company
status: developing
related:
  - "[[Building Effective Agents]]"
  - "[[Augmented LLM]]"
  - "[[Agent-Computer Interface (ACI)]]"
  - "[[Claude]]"
---

# Anthropic

An AI safety and research company, creator of the Claude family of large language models. Anthropic publishes research and engineering guidance on building effective LLM-based systems.

## Key Publications

- [[Building Effective Agents]] — engineering guide on agentic system patterns (workflows vs. agents, prompt chaining, routing, parallelization, orchestrator-workers, evaluator-optimizer)
- Claude Agent SDK — framework for building agentic systems

## Tools & Protocols

- [[Model Context Protocol]] (MCP) — open protocol for connecting LLMs with external tools and data sources
- Claude API — primary interface for building agentic systems with Claude models

## Approach to Agents

Anthropic distinguishes between **workflows** (predefined code paths orchestrating LLMs and tools) and **agents** (LLMs dynamically directing their processes and tool usage). Their guidance emphasizes simplicity: start with single LLM calls, add complexity only when it demonstrably improves outcomes.
