---
layout: post
title: "The fundamentals of context engineering"
date: 2026-01-21 12:00:00 +0000
categories: [general, ai, architecture]
tags: [context-engineering, ai-agents, software-development, prompts, llm]
---

These days I only manually edit a line of code here or there on rare occasions. It's not because I have switched to being a Product Owner, but rather because Copilot is doing almost all of it. I have never written (and deleted) so many lines of code before. To me, it is the most agile way of making software right now. It lets me iterate fast, gather feedback and improve software. In my experience, it has been incredibly effective. That's why I am always incredibly surprised to hear people discarding AI saying: "It never does what I want!" My response is always: "You need to invest more in context engineering." In this blogpost, I'll explain how to get the most out of context engineering and share how to utilize agents to further enhance your capabilities. You can find some examples of my context engineering prompts and agents on my [Agentic development examples Github](https://github.com/danielstegeman/Agentic-development-examples/).

![GitHub pull request diff showing 18,471 lines added in green and 7,854 lines removed in red, demonstrating extensive code changes](../assets/images/2026-01-19/image.png)

My current context engineering process is the result of months of non-stop improvements to my workflow with AI driven development. Each day I try new stuff, big or small. Even with my first blogpost about [feature slicing and ai]({{ site.baseurl }}{% post_url 2025-06-12-feature-slicing-ai-augmented-engineering %}) I was talking about context engineering, even when the term didn't exist yet, and now, half a year later, I've even changed my job title on LinkedIn to context engineer. Recently, I have used it to generate and iterate through thousands of lines of code in a matter of days, all while increasing quality and consistency. So let's dive into the fundamentals of context engineering.

**LLM fundamentals**

To be able to successfully context engineer, you need to understand the fundamentals of how LLMs work. An LLM predicts the next word it will generate based on the previous words, also referred to as tokens, in the input it has received. An LLM can only answer with information from pretrained data. This is all text-based data with no fundamental understanding of the world. 

**What is context engineering?**

Context engineering is all about providing your LLM with more information than the pretrained data. Tools have, and continue to, evolve rapidly, but the core fundamentals have stayed mostly the same. It has been enhanced massively by the recent growth in agent related tools. Most of these fundamentally serve the purpose of context engineering. Instead of providing all of the context in a single prompt, you can now have the agent gather context for itself. When an LLM generates text, it is itself providing context for the next token it will generate. By chaining these generations together, you can have the LLM describe context for itself. Agents make good use of this by having multiple steps to gather context, plan work, execute work and review work. This is why I still prefer to use the Claude 4.5 Haiku model, as it tends to generate a lot more output without further prompting.

**Core cycle of context engineering**

***Define the goal***

Whatever I am prompting, I always start with defining a clear goal. What do I want to achieve? This is the most important part of context engineering. If you don't know what you want, you can't expect the LLM to help you. Be very specific. The more specific, the better. As this is the first context you are providing, it will always be a focus point for the LLM. Everything else you provide will be interpreted in the light of this goal.

***Always follow a plan***

The next step after defining the goal is ensuring the agent has a clear plan to achieve it. Github Copilot's introduction of Plan mode as their first agent feature highlights this importance. This is not a coincidence. A clear plan helps the LLM to structure its thoughts and actions. It also helps to break down complex tasks into smaller, manageable steps with consistent results. 

***Execute the work***

Once you have a goal and a plan, you can have the agent execute its defined work. If you are unsure about the results it will produce, you can always ask the agent to include examples of what it will produce. This will help you to understand if the agent is on the right track before it produces a lot of work that you might not want.

***Review and improve***

Review whatever work the agent has done. If it is not satisfactory, provide feedback and have it improve the work. Sometimes providing feedback is enough. Other times you need to rework your original prompts to provide more context or clarity. I always aim for the classic 80/20 rule: get about 80% correctness on what I want in the first iteration. After that I can adjust with feedback and improvements.

**Shift-left control**

Proper context engineering helps you stay in control of what the agent is doing. Similar to how shift-left in software development moves testing and quality checks earlier in the development cycle, context engineering allows you to add human-in-the-loop checkpoints before the agent executes work. By reviewing and controlling what the agent is going to do at the next step, rather than only reviewing after completion, you can prevent wasted effort and maintain direction. This helps avoid the frustration of completely repeating your prompts in endless cycles of 'no, do this instead'. This will also help you stay within your premium token limits.

**Context engineering through custom agents**

Custom agents have turbocharged context engineering. Instead of having to repeat plans and goals in every prompt, I can now have predefined agents to provide the necessary guidance. It also makes the output way more consistent. When utilized correctly, I have successfully created refined user stories and implemented them with only a handful of extra sentences to guide the agent. To make the behaviour of all the agents more consistent, I started with an agent that creates other agents. This meta-agent ensures that all agents follow the same structure and guidelines. This has made it way easier to manage multiple agents for different tasks. You can use this agent yourself by checking out my [Agentic development examples Github](https://github.com/danielstegeman/Agentic-development-examples/blob/main/.github/agents/agent-curator.agent.md).

**Limitations**

Context engineering is not a silver bullet. There are still limitations to what LLMs can do. They can only work with text-based data. It is hard to context engineer for: "My Windows process is stuck and shows no errors", so you have to know when you have to solve a problem the old fashioned way.
They also have a limited context window. This means that if you provide too much context, the LLM will start forgetting things and possibly contradict itself. This is commonly referred to as Context Degradation Syndrome. Claude 4.5 has a token limit of 400 000, but degradation will occur well before that. This can be remediated by using multiple subagents, more on this in a later blog. 
Additionally, LLMs can sometimes still produce incorrect outputs, even if the context has been carefully curated. This is why the review and improvement step is crucial in the context engineering process. Staying critical of the output all the time can be difficult. Luckily, teammates will still happily point out when you have been vibe coding a little too much.

**Conclusion**

Context engineering is a fundamental skill for anyone looking to leverage LLMs and AI agents effectively. By defining clear goals, following structured plans, executing work, and reviewing outputs, you can harness the full potential of AI-driven development. Custom agents further enhance this process by providing consistent behavior and reducing the need for repetitive prompts. Embrace context engineering to stay in control and achieve your desired outcomes efficiently. 