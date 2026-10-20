---
type: concept
title: "Content Remixing"
created: 2026-07-02
updated: 2026-07-02
tags:
  - concept
  - content
  - ai
  - transformation
  - personalization
status: developing
address: c-000084
related:
  - "[[ljg-learn]]"
  - "[[Code as a Medium for Storytelling]]"
  - "[[Vibe Coding]]"
sources:
  - "[[Code as a Medium for Storytelling]]"
complexity: basic
domain: "ai-coding"
aliases:
  - "content transformation"
  - "format remixing"
---

# Content Remixing

The practice of using LLMs to transform a single piece of content into multiple formats optimized for different consumption preferences. The insight: everyone consumes content differently, and AI agents now make it trivial to remix any source into the format that best suits the individual.

## Common Remix Targets

| Source Format | Remix Targets |
|---------------|---------------|
| Long podcast / video | Magazine article, business biography, briefing document, newsletter |
| Transcript | Physical book chapter, ebook, tweet thread |
| Raw data | Interactive dashboard, visual chart |
| Codebase | Interactive CS course, layman explanation |

## Why Generic Summaries Fail

The key challenge: generic AI summaries are too brief, too generic, and strip out the best parts (quotes, anecdotes, personality). Effective remixing requires:

1. **Preserving the best quotes and anecdotes** from the original
2. **Mapping to a narrative structure** that is intrinsically readable (e.g., New Yorker-style magazine, Shoe Dog-style business biography)
3. **Explaining technical concepts** in layman language without dumbing down
4. **Maintaining the author's voice** while adapting the format

## Examples

- [[ljg-learn]] remixed the *Acquired* podcast into a printed physical book, with each episode as a 20-page chapter written in the style of a business biography
- YouTube transcripts remixed into magazine articles for easier reading, then optionally converted to EPUB and delivered as a weekly newsletter to the inbox

## The Prompting Approach

Rather than crafting precise prompt engineering, the recommended approach is **brain dumping**: rambling unstructured thoughts about what you want, including personal preferences and taste, and letting the LLM structure it into a coherent prompt. Voice input is particularly effective for this.