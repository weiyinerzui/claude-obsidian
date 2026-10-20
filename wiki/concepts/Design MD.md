---
type: concept
title: "Design MD"
created: 2026-07-02
updated: 2026-07-02
tags:
  - concept
  - design
  - ai-coding
  - frontend
  - design-tokens
status: developing
address: c-000081
related:
  - "[[ljg-learn]]"
  - "[[Code as a Medium for Storytelling]]"
  - "[[Vibe Coding]]"
  - "[[Playgrounds (LLM Design)]]"
sources:
  - "[[Code as a Medium for Storytelling]]"
complexity: intermediate
domain: "ai-coding"
aliases:
  - "design.md"
  - "design tokens as markdown"
---

# Design MD

A pattern for guiding AI-generated front-end design using declarative markdown files that describe a **design system** (color combinations, typography, spacing, visual mood) rather than imperative HTML templates. The insight: LLMs do better work when given a design language to interpret creatively than when forced to fill content into pre-structured layout skeletons.

## The Problem with HTML Templates

When AI models are given HTML template files as design guides, they **overfit** the template. They squeeze the user's content into the exact layout and arrangement of the template, compromising content quality and structural coherence. The template's structure constrains rather than liberates.

## The Design MD Approach

A `design.md` file is a plain markdown document specifying:

- **Color palette**: primary, accent, background, and semantic colors
- **Typography**: font pairings, scale ratios, weights
- **Spacing and layout**: grid preferences, density, white space philosophy
- **Mood and vibe**: abstract descriptors of the desired emotional feel (e.g., "editorial," "brutalist," "soft academic")
- **Anti-patterns**: explicit bans on specific design clichés (e.g., "no purple gradients," "no instrumental serif italics")

The model then interprets these tokens creatively for the specific content at hand, producing designs that are both consistent with the system and optimized for the unique content structure.

## Origins

Discovered by [[ljg-learn]] during the development of Front-End Slides, after initial attempts with HTML templates produced rigid, content-mismatched output. The concept parallels existing design-token specifications used in professional design systems but adapts them for the specific affordances of LLM front-end generation.
