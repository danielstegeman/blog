---
applyTo: '_posts/*'
---

# Writing Style & Tone of Voice Guide

This guide describes the preferred writing style and tone for blog posts based on analysis of existing content.

## Overall Tone & Voice

### Professional yet Accessible
- Maintain a professional, authoritative tone while remaining approachable and conversational
- Write as an experienced practitioner sharing insights with peers
- Avoid overly academic language; prefer clear, direct communication
- Use "I" and personal experiences to ground abstract concepts in reality

### Pragmatic and Experience-Based
- Ground theoretical concepts in practical, real-world application
- Share personal experimentation and results: "I've experimented with this in my current project"
- Include specific outcomes and metrics when possible: "30-50% less time"
- Acknowledge both benefits and drawbacks of approaches honestly

## Content Structure & Flow

### Opening Hook
- Start with a broader observation or trend in the industry
- Connect seemingly unrelated concepts: "two seemingly independent trends to unexpectedly strengthen one another"
- Set up the premise with a personal angle: "I've experimented with this... with surprisingly strong results"

### Logical Progression
- Use clear section headers that guide the reader through your argument
- Build concepts incrementally, from foundational to applied
- Use transitional phrases to connect ideas: "However," "As a result," "In practice"

### Balanced Perspective
- Present both advantages and disadvantages
- Use phrases like "Unfortunately" and "However" to acknowledge limitations
- End with qualified conclusions rather than absolutes

## Language & Style Patterns

### Sentence Structure
- Mix shorter, punchy sentences with longer, explanatory ones
- Don't use em dashes for emphasis and clarification
- Prefer active voice: "AI tools enjoy nearly the same benefits" vs. "The same benefits are enjoyed by AI tools"

### Technical Communication
- Explain technical concepts clearly without dumbing them down
- Use concrete examples and analogies
- Define abbreviations on first use: "DRY (Don't Repeat Yourself)"
- Include practical implementation details when relevant

### Engagement Techniques
- Pose rhetorical questions: "So why not align the architecture accordingly?"
- Address the reader directly: "If you value documentation..."
- Use inclusive language: "you can," "we," "your project"

## Content Guidelines

### Focus Areas
- Software engineering practices and architecture
- AI-augmented development workflows
- Practical productivity improvements
- Personal experiences with tools and methodologies

### Evidence and Support
- Include specific results from personal experimentation
- Reference concrete projects and outcomes
- Provide actionable advice and implementation details
- Share both successes and failures/limitations

### Technical Depth
- Assume an audience of software engineering professionals
- Include sufficient technical detail without overwhelming
- Provide context for architectural decisions
- Explain the "why" behind recommendations, not just the "what"

## Structural Elements

### Introduction
- Set the stage with industry context
- Present the core thesis or observation
- Hint at personal experience or experimentation

### Body Sections
- Use descriptive subheadings
- Lead with the concept, follow with practical application
- Include both theoretical benefits and real-world constraints
- Provide specific examples and implementation details

### Conclusion
- Synthesize the key insights
- Acknowledge the broader implications
- End with a forward-looking perspective on the field
- Emphasize the human element in technology decisions

## Tone Indicators to Maintain

**Authoritative but Humble**: "I was able to use Copilot's edit mode" (claiming success) followed by "Only minor adjustments were needed" (acknowledging imperfection)

**Balanced Skepticism**: Present both the promise and limitations of new approaches

**Practical Focus**: Always return to real-world application and measurable outcomes

**Professional Growth Mindset**: Position learning and experimentation as ongoing processes

## Front Matter Requirements

### Social Media Preview Images
- **Required**: Add `image:` field to front matter when the post contains images
- **Path Format**: Use site-relative paths starting with `/blog/assets/images/YYYY-MM-DD/image.png`
- **Recommended Size**: 1200×630 pixels for optimal social media preview display
- **Purpose**: This field is automatically used by jekyll-seo-tag to generate Open Graph (og:image) and Twitter Card meta tags
- **Convention**: Use the first or most representative image from your post content
- **Posts without images**: Do not add an image field; no social preview will be generated

**Example front matter with image:**
```yaml
---
layout: post
title: "Your Post Title"
date: 2026-01-21 12:00:00 +0000
categories: [category1, category2]
tags: [tag1, tag2, tag3]
image: /blog/assets/images/2026-01-21/image.png
---
```