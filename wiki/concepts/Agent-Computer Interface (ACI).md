---
type: concept
title: "Agent-Computer Interface (ACI)"
address: c-000077
created: 2026-06-09
updated: 2026-06-09
tags:
  - concept
  - agent
  - tool-design
  - pattern
status: developing
related:
  - "[[Building Effective Agents]]"
  - "[[Augmented LLM]]"
  - "[[Model Context Protocol]]"
---

# Agent-Computer Interface (ACI)

The design principles for creating tools that LLM agents use effectively. Analogous to Human-Computer Interface (HCI) design, but adapted for the model's cognitive patterns and constraints.

## Core Principle

Invest as much effort in designing the agent's tools as we do in designing user interfaces. A well-designed tool is obvious in its use, clear in its parameters, and hard to misuse.

## Design Guidelines

1. **Put yourself in the model's shoes**: Is it obvious how to use this tool from the description and parameters? If a human would need to think carefully, the model probably does too.

2. **Great docstrings**: Write tool documentation as if for a junior developer on your team. Include example usage, edge cases, input format requirements, and clear boundaries from similar tools.

3. **Test how the model uses tools**: Run many example inputs to see what mistakes the model makes. Iterate.

4. **Poka-yoke your tools**: Change arguments to make it harder to make mistakes. Example from Anthropic's SWE-bench agent: switching from relative to absolute filepaths eliminated an entire class of errors.

## Format Considerations

Different formats for the same action can have dramatically different LLM performance:
- Writing a diff requires knowing line counts in chunk headers
- Writing code inside JSON requires escaping newlines and quotes (harder than markdown)
- Prefer formats the model has seen naturally occurring in text on the internet
- Avoid formatting overhead that requires the model to maintain accurate counts

## Relationship to [[Model Context Protocol]]

MCP provides the *infrastructure* for connecting tools; ACI provides the *design principles* for how those tools should be specified and documented.
