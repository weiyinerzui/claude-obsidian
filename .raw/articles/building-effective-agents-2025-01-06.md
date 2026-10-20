---
source_url: https://www.anthropic.com/engineering/building-effective-agents
fetched: 2026-06-09
---

Building Effective AI Agents

Anthropic Engineering Blog — January 2025

By Erik S. and Barry Zhang

We've worked with dozens of teams building LLM agents across industries. Consistently, the most successful implementations use simple, composable patterns rather than complex frameworks.

"Agent" can be defined in several ways. Anthropic categorizes all variations as agentic systems but draws an important architectural distinction between workflows (systems where LLMs and tools are orchestrated through predefined code paths) and agents (systems where LLMs dynamically direct their own processes and tool usage, maintaining control over how they accomplish tasks).

When (and when not) to use agents

Find the simplest solution possible. Optimizing single LLM calls with retrieval and in-context examples is usually enough. Workflows offer predictability for well-defined tasks; agents are better when flexibility and model-driven decision-making are needed at scale.

When and how to use frameworks

Frameworks (Claude Agent SDK, AWS Strands Agents SDK, Rivet, Vellum) simplify low-level tasks but can obscure prompts and responses, making debugging harder. Start by using LLM APIs directly; many patterns can be implemented in a few lines of code. If you use a framework, ensure you understand the underlying code.

Building blocks, workflows, and agents

1. Augmented LLM — the basic building block: an LLM enhanced with retrieval, tools, and memory. Models can actively generate search queries, select tools, and determine what to retain. Recommendation: tailor capabilities to use case, provide a well-documented interface, and consider the Model Context Protocol (MCP) for third-party tool integration.

2. Prompt Chaining — decomposes a task into a sequence of steps, with each LLM call processing the output of the previous one. Programmatic checks ("gates") can be added on intermediate steps. Best for tasks that decompose cleanly into fixed subtasks. Examples: generating marketing copy then translating it; writing an outline, validating it, then writing the document.

3. Routing — classifies an input and directs it to a specialized followup task. Allows separation of concerns and more specialized prompts. Best when there are distinct categories better handled separately and classification can be accurate. Examples: directing customer service queries by type; routing easy questions to cheaper models and hard questions to more capable ones.

4. Parallelization — LLMs work simultaneously on a task and outputs are aggregated programmatically. Two variations: Sectioning (breaking into independent parallel subtasks) and Voting (running the same task multiple times for diverse outputs). Best for tasks that benefit from speed or multiple perspectives. Examples: guardrails with separate model instances for user queries and content screening; automated evals; code vulnerability review.

5. Orchestrator-Workers — a central LLM dynamically breaks down tasks, delegates to worker LLMs, and synthesizes results. Key difference from parallelization: subtasks aren't pre-defined but determined by the orchestrator based on specific input. Best for complex tasks where subtasks can't be predicted. Examples: coding products making complex multi-file changes; search tasks gathering info from multiple sources.

6. Evaluator-Optimizer — one LLM generates a response while another provides evaluation and feedback in a loop. Best when clear evaluation criteria exist and iterative refinement provides measurable value. Examples: literary translation with nuance checking; complex multi-round search tasks.

7. Agents — LLMs using tools based on environmental feedback in a loop. Agents plan and operate independently, potentially returning to humans for information or judgement. Crucial to design toolsets and their documentation clearly. Best for open-ended problems where steps can't be predicted. Examples: coding agents for SWE-bench; computer use reference implementation.

Three core principles:
1. Maintain simplicity in agent design.
2. Prioritize transparency by explicitly showing the agent's planning steps.
3. Carefully craft the agent-computer interface (ACI) through thorough tool documentation and testing.

Appendix 1: Agents in Practice

Two particularly promising applications:
A. Customer support — combines chatbot interfaces with tool integration (customer data, order history, knowledge base articles, actions like refunds). Success measured through user-defined resolutions.
B. Coding agents — code is verifiable through automated tests; agents iterate using test results as feedback. SWE-bench Verified benchmark used for evaluation.

Appendix 2: Prompt Engineering Your Tools

Tool definitions deserve as much attention as overall prompts. Suggestions:
- Give the model enough tokens to "think" before committing.
- Keep format close to what the model has seen in natural text.
- Avoid formatting overhead (line counts, string escaping).
- Invest as much effort in ACI as we do in HCI: test, iterate, poka-yoke your tools.
- Example: changing relative filepaths to absolute filepaths eliminated errors in SWE-bench agent.
