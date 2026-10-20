---
type: concept
title: "Evaluator-Optimizer"
address: c-000075
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
  - "[[写作优化Prompt]]"
  - "[[品味判断力]]"
---

# Evaluator-Optimizer

An agentic workflow pattern where one LLM call generates a response while another provides evaluation and feedback in a loop.

## When to Use

Particularly effective when:
1. There are clear evaluation criteria for outputs
2. LLM responses can be demonstrably improved through articulated feedback
3. The evaluating LLM can provide useful critiques

Analogous to the iterative writing process a human writer goes through when producing a polished document.

## Examples

- **Literary translation**: the translator LLM produces an initial translation; the evaluator LLM catches nuances and provides critique
- **Complex search**: iterative rounds of searching and analysis, with the evaluator deciding whether further searches are warranted

## Relationship to [[Prompt Chaining]]

Unlike [[Prompt Chaining]]'s linear progression, the Evaluator-Optimizer uses a loop. Both can be combined: a chain step might internally use an evaluator-optimizer loop for refinement.

## Relationship to [[写作优化Prompt]] and [[品味判断力]]

The Evaluator-Optimizer pattern provides the *technical loop structure* for the creative evaluation process described in [[写作优化Prompt]] (writing evaluation knowledge as executable AI prompts) and [[品味判断力]] (the creator's intuitive judgment toward their own work).
