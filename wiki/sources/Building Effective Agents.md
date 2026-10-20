---
type: source
title: "Building Effective Agents"
author: "Erik S. and Barry Zhang"
source_type: article
source_url: "https://www.anthropic.com/engineering/building-effective-agents"
address: c-000076
created: 2026-06-09
updated: 2026-06-09
tags:
  - source
  - article
  - agent
  - llm
  - anthropic
  - workflow
status: current
related:
  - "[[Anthropic]]"
  - "[[Augmented LLM]]"
  - "[[Prompt Chaining]]"
  - "[[Routing (LLM Agent)]]"
  - "[[Parallelization (LLM)]]"
  - "[[Orchestrator-Workers]]"
  - "[[Evaluator-Optimizer]]"
  - "[[Agent-Computer Interface (ACI)]]"
  - "[[智能体工作流]]"
---

# Building Effective Agents

Anthropic Engineering Blog article (January 2025) detailing patterns for building LLM-based agentic systems, distilled from experience with dozens of customer implementations.

## Summary

The article catalogs six common patterns for agentic systems — from simple augmented LLMs to autonomous agents — and provides guidance on when to use each. It emphasizes starting simple, measuring performance, and only adding complexity when it demonstrably improves outcomes.

## Key Framework

The central architectural distinction: **workflows** (predefined code paths) vs. **agents** (LLMs dynamically directing processes). Most successful implementations use simple, composable patterns rather than complex frameworks.

### The Six Patterns

1. [[Augmented LLM]] — LLM enhanced with retrieval, tools, and memory (the basic building block)
2. [[Prompt Chaining]] — sequential step decomposition with programmatic gates
3. [[Routing (LLM Agent)]] — classification-based dispatch to specialized handlers
4. [[Parallelization (LLM)]] — sectioning and voting for simultaneous LLM calls
5. [[Orchestrator-Workers]] — dynamic task breakdown and delegation
6. [[Evaluator-Optimizer]] — generation-evaluation feedback loop

Plus **[[Agent-Computer Interface (ACI)]]** — tool design principles parallel to HCI.

## Applications

- Customer support: chatbot + tool integration with usage-based pricing
- Coding agents: SWE-bench Verified, autonomous code generation

## Relationship to Existing Wiki

This article's engineering-oriented agent taxonomy complements the creative/写作-oriented [[智能体工作流]] concept. The Anthropic patterns describe *how* to structure LLM calls technically, while [[智能体工作流]] describes *role-based* agent decomposition for human-AI creative collaboration.
