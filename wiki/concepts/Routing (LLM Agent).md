---
type: concept
title: "Routing (LLM Agent)"
address: c-000072
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
  - "[[Prompt Chaining]]"
  - "[[Augmented LLM]]"
  - "[[Intelligent Agent]]"
---

# Routing (LLM Agent)

An agentic workflow pattern that classifies an input and directs it to a specialized followup task. This allows separation of concerns and building more specialized prompts — optimizing for one kind of input won't hurt performance on other inputs.

## When to Use

Best when there are distinct categories that require different handling, and classification can be done accurately (by an LLM or a traditional classifier).

## Examples

- Customer service: directing general questions, refund requests, and technical support into different downstream processes
- Model routing: sending easy/common questions to cost-efficient models like Claude Haiku, hard/unusual questions to more capable models like Claude Sonnet

## Relationship to [[Prompt Chaining]]

Routing can be used *within* a chain step: a router classifies input and dispatches to different sub-chains. This makes routing more of a flow-control pattern than a standalone workflow.
