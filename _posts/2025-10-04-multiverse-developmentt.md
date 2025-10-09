---
layout: post
title: "Multiverse Development Cycle with Agents"
date: 2025-10-04 12:00:00 +0000
categories: [general]
tags: []
---

For decades, the software development lifecycle has followed a well-established, linear path. Whether using waterfall, agile, or even DevOps-inspired approaches, the process typically moves step by step: requirements are gathered, designs are created, code is implemented, tests are written and executed, and finally, the product is deployed and maintained. Each phase is expected to build on the previous one, with clear boundaries and plenty of review in between.

However, in practice, this process is sometimes far from perfect. How often have you meticulously followed all the steps, only to discover during implementation that your analysis and design are technically unfeasible? Or that acceptance tests reveal completely unexpected requirements? Agile methodology attempts to solve this by making cycles shorter and work increments smaller. 

Today, however, the rise of AI-powered tools and agentic workflows is challenging this fundamental assumption. What if development didn’t have to be a straight line from start to finish? What if, instead, we could move fluidly between any stage, or even work on multiple phases at once? When you fully incorporate agentic AI into your way-of-work, your team becomes much more agile.

## Everything
When ChatGPT first launched, developers quickly began using it to write code. As LLMs have evolved and improved, they've expanded into every other stage of development. I now use Copilot to help formulate user stories and create designs daily. Each development stage builds context that feeds AI agents with richer information. In a [previous blog post](./2025-06-12-feature-slicing-ai-augmented-engineering.md) I used a feature design document to generate the implementation. But AI was not used when writing the design document or refining the user story before that.

However, using AI agents at every stage is just the beginning—you can also leverage them to transition seamlessly between stages.

## Everywhere

As moving between stages becomes easier, each stage's focus shifts from rigid process to flexible perspective. Linear development often brings new insights, particularly when working with unfamiliar products or tech stacks. Why not leverage these insights to revisit earlier processes and adapt your acceptance criteria based on implementation discoveries? 

AI agents can review gaps between stages and evaluate whether changes were deliberate decisions or oversights. Traditional linear processes rely on human gatekeepers before stage transitions, but AI enables bidirectional validation. This achieves the ultimate goal of any other agile process; to shorten the feedback cycle.

To facilitate these perspectives, I have created chat modes to reflect each viewpoint. Refinement mode reviews or adapts the user story by looking at other stages. Architect mode does the same for the design. I have not yet found a need for an implementation chat mode, as that seems to come naturally to the GitHub Copilot Agent.

During recent development work, I encountered constraints that necessitated design changes. This even sparked renewed discussions about acceptance criteria—criteria that had supposedly been thoroughly discussed and team-approved. I found myself repeatedly switching between analysis, design, and implementation. Each decision point offered multiple perspectives on the problem for reference. Copilot helped identify gaps between analysis, design, and implementation, giving me moments to distinguish between deliberate changes and forgotten details. 

Now we have explored the transition between stages, let's fully enter the Multiverse Development Cycle.

## All at Once
Context drives everything in AI. By moving fluidly between development stages, you build comprehensive context that enables adaptation with increasing ease and consistency. Documentation and implementation no longer drift apart when requirements change or uncertainties arise. A few carefully engineered prompts keep everything synchronized. Multiple perspectives contribute to a unified state, while that unified state informs multiple perspectives. With thorough context, your AI agent can completely re-implement code from design specifications at will. When you fully adapt to this new way of working, there are many advantages:

Instead of having a separate proof of concept to develop features with technical uncertainty, this work can now be incorporated directly into the implementation stage of the development cycle. The proof of concept can be used to inform the design and analysis stages. Rather than discarding a proof of concept, you now have your first iteration of a feature.

This new cycle will also reduce the need for review by team members, increasing everyone's focus on their own work. Instead of reviewing after every stage, you can complete the full multiverse cycle once or twice, then gather feedback from team members before finalizing.

Consider another common scenario: during implementation, design changes emerge from new insights, but the corresponding documentation remains outdated. With AI, updating documentation becomes trivial—a simple prompt resolves the discrepancy.

Since the development cycle abandons linearity, you can even reconstruct forgotten user stories from existing implementation and tests, then evaluate and refine those stories as needed.

Instead of estimating and planning a feature from start to finish in a sprint, you can split your work into multiple timeboxed iteration cycles, allowing for moments of review in between. Rather than agreeing on any single stage, you focus on the end result. 

By fully embracing an AI-augmented development cycle, your team can achieve a level of agility and adaptability that surpasses what traditional frameworks offer.