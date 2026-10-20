---
type: concept
title: "Augmented LLM"
address: c-000070
created: 2026-06-09
updated: 2026-06-09
tags:
  - concept
  - agent
  - llm
  - architecture
status: developing
related:
  - "[[Building Effective Agents]]"
  - "[[Prompt Chaining]]"
  - "[[Routing (LLM Agent)]]"
  - "[[Model Context Protocol]]"
  - "[[智能体工作流]]"
---

# Augmented LLM

The basic building block of agentic systems: an LLM enhanced with augmentations such as retrieval, tools, and memory. Current models can actively use these capabilities — generating their own search queries, selecting appropriate tools, and determining what information to retain.

## Key Aspects

- **Tailor capabilities** to your specific use case
- **Well-documented interface** for how the LLM interacts with tools and data
- **MCP integration**: [[Model Context Protocol]] allows connecting to a growing ecosystem of third-party tools

## Connection to Other Patterns

The augmented LLM is the foundation for all other agentic patterns. Each workflow pattern ([[Prompt Chaining]], [[Routing (LLM Agent)]], [[Parallelization (LLM)]], etc.) composes multiple augmented LLM calls into structured systems.

## Relationship to [[智能体工作流]]

The Augmented LLM pattern provides the *technical* layer — how a single LLM call interacts with tools and memory. The [[智能体工作流]] pattern provides the *role-based* layer — how multiple agents with distinct personas collaborate on creative work. They operate at different abstraction levels and can be combined.
