---
layout: post
title: "The bumpy road to a fully agentic development cycle"
date: 2025-12-08 12:00:00 +0200
categories: [general, architecture, ai]
tags: [ai-agents, agile, way-of-work, copilot, llm, documentation, feature-design,  context-engineering]
---

The AI agent hype is everywhere. Demos show stunning results: agents writing entire features, refactoring codebases, even debugging production issues. I experienced this myself with agentic software development on a relatively straightforward Azure DevOps pipeline, the results were impressive enough to write about. However, scaling these proof-of-concept successes to a second, vastly more complex pipeline spanning multiple sprints has revealed a more nuanced reality. Striving for a fully agentic development cycle does not only bring technical limitations, it forces us to rethink fundamental assumptions about the software development lifecycle itself.

My recent experience applying agentic development to this complex pipeline project, combined with insights from pioneers at QCon, has exposed critical challenges that were invisible when working on the simpler first pipeline. The most surprising realisation? Many of these challenges are not new at all. They are the same problems we have always faced with human developers, just amplified and made more visible by AI agents.

## From prototype to production: the scaling challenge

The transition from a straightforward pipeline to a complex multi-stage deployment workflow is not just a matter of "doing more of the same." What worked brilliantly for the first pipeline becomes unwieldy when the scope expands. The agent that confidently implemented a simple test pipeline suddenly loses track of architectural decisions across multiple environments, approval gates, and intricate dependency chains. Adapting a larger high-level-design to new design insights became difficult. Re-establishing a context in the middle of some refactoring work caused fixation on the wrong code. Context that fit comfortably in a chat session for a two-day pipeline becomes overwhelming noise for a multi-sprint implementation.

At QCon, I heard someone capture this perfectly: "2025 is the year of agents. 2026 will be the year of context engineering." This resonated deeply with my experience. The bottleneck is not the agent's ability to write code, it is our ability to provide the right context at the right time.

## Context engineering: finding the sweet spot

Context is at the center of enabling a fully agentic development process, but there is a critical balance to strike. Too little context and the agent makes incorrect assumptions or asks endless clarifying questions. Too much context and the agent drowns in details, forgetting key architectural decisions or missing the bigger picture entirely.

I have observed this pattern repeatedly. When I provide a comprehensive design document with every architectural decision, the agent fixates on implementation details and loses sight of the overall goal. When I provide only a user story, it makes questionable architectural choices that require extensive rework. The sweet spot lies somewhere in between, but finding it requires experimentation and iteration.

This is one of the most fundamental challenges facing agentic development at scale. We need new patterns for structuring context that help agents maintain the right level of abstraction while still having access to necessary details. The solution is not just technical, it requires rethinking how we organize and communicate information throughout the development lifecycle.

Amazon recently introduced a standard operating procedures framework for agentic workflows, recognizing this exact challenge. Just as humans rely on SOPs to maintain consistency and quality in complex processes, AI agents benefit from the same structured guidance. The parallel is striking: both humans and agents perform better with clear, documented procedures that provide the right context at the right time.

## The development cycle adaptations

Most current development processes rest on a fundamental assumption: writing code is time-consuming and expensive relative to planning and documentation. Agentic development fundamentally changes this relationship. The cost of implementation is rapidly moving towards zero.

This shift has profound implications for how we work. The agile principle "working software over comprehensive documentation" becomes more relevant than ever. In a world where an agent can generate working software in minutes, we can explore ideas through implementation rather than extensive upfront planning. Most of the development cycle now happens within a chat session with your agent. When paired with fast continuous delivery, you can gather feedback from end users even faster than before.

This even shorter feedback cycle allows developers to accelerate their "fail fast" approach. At Anthropic, this way of developing was used to great success for refining their console input module. Agents allowed them to resolve numerous edge cases reported by Claude CLI users with remarkable speed, iterating through solutions that would have taken much longer in traditional development cycles.

Agentic development opens the door to new possibilities. How many times have you compromised end user value for the sake of reusing an existing solution, even though you knew it did not fully fit your use case? Agents allow you to experiment rapidly with complex abstractions fully tailored to your specific needs. In my own work on the Azure DevOps pipeline, I used Copilot to create complex logic to parse JSON and load it into pipeline variables. JSON allowed a far better configuration structure than the default YAML variable notation in pipelines. This is something that would have taken many days to experiment with and iterate on without AI assistance. Without it, I would have settled for an easier but compromised solution that would have made the configuration harder to maintain. 

## New technology, old problems

Many of the challenges we face with agentic development are not new. Humans and LLMs have more in common than you might think. The problems are just more exaggerated and visible with AI agents. For instance, people also make mistakes when missing context or being overwhelmed with it. We are just better at managing context in our minds, filtering relevant from irrelevant information on the fly.

This realization is both humbling and encouraging. We already have safeguards in place to mitigate these shortcomings: code reviews catch mistakes from insufficient context, tests verify behavior regardless of how code was written, static analysis enforces standards consistently. These safeguards were designed for human developers but apply equally well to agent-generated code.

However, we should not assume existing safeguards are sufficient. Even with human developers, our processes are not perfect. Incidents and bugs still happen. Reviews miss issues, tests have gaps, analysis tools produce false positives that get ignored. The difference is that agents can produce code faster than our review processes were designed to handle. A human might write 200 lines of code per day. An agent might write 2000. Can our review processes scale accordingly?

The answer is probably not without adaptation. But the adaptation required is not revolutionary. It is evolutionary. Better automated testing, CI/CD, more sophisticated static analysis, clearer architectural guidelines that agents can follow. Many organizations are already moving in this direction for human developers. Agentic development just accelerates the urgency.

Research from Sonar highlights why we cannot simply wait for better models to solve these problems. Their analysis showed that newer models actually exhibited regression in some areas of code generation compared to earlier versions. We cannot rely on model improvements alone to address the challenges of agentic development. The solution lies in adapting our processes, not waiting for perfect AI.

## Looking forward: the human element remains central

The bumpy road to fully agentic development is revealing something important: the technology is not the primary constraint. The constraint is our ability to structure problems, communicate context, and maintain architectural coherence at scale. These are fundamentally human skills.

As we move into 2026 and the era of context engineering, success will depend on our ability to adapt our processes and architectures for collaboration with AI agents. This means rethinking documentation practices, developing new patterns for context structuring, and evolving our safeguards to handle the increased velocity of agent-generated code.

The exciting part? We are not starting from zero. The problems are familiar, just amplified. The solutions will build on practices we already know work. And the potential gains in productivity and capability are substantial enough to make the bumpy journey worthwhile. The road ahead is challenging, but the destination, a development process that truly leverages both human insight and AI capability, is worth reaching. 