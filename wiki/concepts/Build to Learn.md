---
type: concept
title: "Build to Learn"
created: 2026-07-02
updated: 2026-07-02
tags:
  - concept
  - learning
  - ai-coding
  - education
  - computer-science
status: developing
address: c-000085
related:
  - "[[ljg-learn]]"
  - "[[Vibe Coding]]"
  - "[[Code as a Medium for Storytelling]]"
  - "[[Opinionated Products]]"
sources:
  - "[[Code as a Medium for Storytelling]]"
complexity: basic
domain: "ai-coding"
aliases:
  - "build first learn later"
  - "reverse CS education"
---

# Build to Learn

A philosophy of computer science education in the AI era: instead of the traditional bottom-up approach (foundational courses → advanced topics → building), learners should **build first with AI agents, then learn how it works under the hood**. The best CS course is your own vibe-coded project.

## Traditional vs. Build-to-Learn

| Traditional | Build to Learn |
|-------------|----------------|
| Bottom-up: foundations first | Top-down: build first, then drill down |
| Learn syntax, then algorithms, then systems | Describe an idea, ship a product, then ask "how does this work?" |
| CS curriculum as prerequisite | Your own codebase as curriculum |
| Theory before practice | Practice generates curiosity for theory |

## Implementation: Codebase to Course

The concept was operationalized as a tool that takes any GitHub repo or local codebase and auto-generates an interactive HTML-based CS course. Features include:

- **Layman translations**: hover over technical terms for plain-English explanations
- **Side-by-side code views**: original code next to English translation
- **Interactive quizzes**: test understanding of key concepts
- **Data flow animations**: trace user journeys through the system visually
- **Component group chats**: simulate APIs and technologies talking to each other in a chat format

## Core Insight

When a learner has built something themselves, they have intrinsic motivation to understand how it works. The codebase is personally meaningful. The learning is driven by genuine curiosity rather than curriculum requirements. AI agents make this approach viable because they can explain the codebase in context, at the learner's level, on demand.