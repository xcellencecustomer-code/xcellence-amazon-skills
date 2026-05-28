---
name: amazon-listing-bullets-writer
description: write and optimize amazon listing bullet points with conversion-first structure, prioritizing market reviews and competitor review insights whenever available. use when the user wants to create, improve, diagnose, or restructure amazon bullet points, especially when customer reviews, market feedback, objections, and category expectations are available.
---

# Amazon Listing Bullets Writer

Write and optimize Amazon bullet points with a strict rule: prioritize market reviews and competitor review insights whenever they are available. If no review-market base is available, explicitly warn the user before presenting final bullet points.

## Overview

Use this skill for Amazon bullet point work that must balance:
- conversion
- customer clarity
- objection handling
- natural keyword integration
- persuasive structure
- marketplace realism

This skill is for bullet writing and bullet optimization, not for standalone review scraping or review research. It can use review insights supplied by the user, but it does not invent review evidence.

## Core rules

- Always prioritize real market-review evidence when available.
- Treat competitor reviews, market reviews, category complaints, recurring praise, and customer-language notes as the strongest input layer for bullet decisions.
- If no real review-market input is available, explicitly tell the user before generating final bullets.
- In that case, produce bullets based on product logic, category expectations, audience needs, and common objections, but do not present them as fully market-validated bullets.
- Do not write bullets as generic description blocks.
- Do not make all bullets sound the same.
- Give each bullet a distinct job in the persuasion flow.
- Focus on benefits first, then support them with the right characteristics.
- Use characteristics only when they help buying decisions.
- Keep keywords natural and readable.
- Avoid vague filler such as premium, high quality, practical, excellent, or superior unless category-specific proof makes them genuinely useful.

## Mandatory review-market transparency

Before producing final bullets, determine which of these cases applies.

### Case 1: review-market input is available

Examples:
- competitor review summaries
- extracts from positive or negative reviews
- recurring complaint lists
- customer language notes
- review-based objection summaries
- category pain points gathered from the market

When review-market input is available:
- use it as the primary decision layer for bullet structure
- identify the strongest desired benefits
- identify the strongest objections and frustrations
- identify the customer words that improve resonance
- decide which bullets should carry desire, proof, differentiation, and reassurance
- explain what insights were used

### Case 2: no review-market input is available

Before writing final bullets, explicitly say that:
- the bullets will be written from product logic, category expectations, target audience, and common objections
- the result may still be commercially strong and well structured
- but it is not the most market-validated bullet set possible without review input

Use direct language. Do not hide this limitation.

## Supported tasks

Use this skill when the user wants to:
- create a new set of Amazon bullets from product details
- improve or rewrite existing bullets
- diagnose weak, repetitive, or generic bullets
- structure bullets for better conversion
- decide what each bullet should focus on
- turn product attributes into buyer-facing benefits
- integrate objections, differentiation, and reassurance into bullet flow

## Default persuasion structure

Build bullets as a mini conversion path, not as a random feature list.

Default bullet sequence:
1. Main value or strongest buying promise
2. Second strong value that reinforces desire
3. Useful concrete or technical support with buyer language
4. Key differentiator or “why this one”
5. Reassurance, confidence, brand, or reduced-risk close

Use the guidance in `references/bullet-framework.md`.

## Bullet writing logic

Each bullet must do one main job:
- attract
- convince
- clarify
- differentiate
- reassure

Do not overload one bullet with too many missions.
Do not repeat the same promise across multiple bullets.

## Keyword and language logic

Bullet points may contain useful keywords, but never at the expense of readability.

Use customer-facing language.
Prefer:
- language buyers use
- language that resolves doubts
- language that clarifies usage
- language that supports comparison

Do not make bullets sound like SEO stuffing.

Use the guidance in `references/benefit-characteristic-balance.md`.

## Existing-bullet optimization workflow

When the user provides existing bullets:
1. Diagnose weak spots
2. Identify:
   - generic claims
   - repeated ideas
   - technical overload
   - weak hierarchy
   - missing objections
   - weak close or weak reassurance
3. Decide what to keep
4. Rewrite into stronger bullets
5. Explain why the new set converts better

Use `references/rewrite-checklist.md`.

## Writing style

Default style:
- start each bullet with a short, scannable lead-in in uppercase when appropriate
- keep the promise visible early
- connect the feature to the benefit
- write for fast scanning
- keep the tone concrete and commercially credible

Do not force uppercase lead-ins if the user wants a cleaner or softer style, but treat them as a strong default.

## Output style

Use practical, structured outputs with clear headings.

A sensible default output is:
1. Review-market status
2. Main promise
3. Second strongest value
4. Which features truly deserve a bullet
5. Full set of 5 bullets
6. Role of each bullet
7. What was excluded and why
8. Weakness or redundancy check

When rewriting existing bullets, also include:
- what is weak in the current version
- what should be removed
- what should stay
- why the new sequence is stronger

## Quality checks

Before finalizing, verify:
- bullet 1 gives a real buying reason
- bullet 2 adds a different value
- bullet 3 makes the offer more concrete
- bullet 4 creates preference
- bullet 5 reduces risk or increases confidence
- the bullets are not redundant
- the language is not generic or empty
- the user has been warned if review-market input was missing

## Mistakes to avoid

- pretending bullets are market-validated without review input
- writing five feature descriptions with no persuasion order
- using vague marketing filler
- repeating the same comfort, quality, or practicality claim in several bullets
- writing bullets that sound algorithmic instead of buyer-facing
- forgetting objections and reassurance

## Example requests

- "Write 5 Amazon bullets for this product."
- "Improve these existing Amazon bullet points."
- "Turn these product benefits into stronger bullets."
- "Use these competitor review insights to write better bullets."
- "Tell me what is weak or repetitive in these bullets."
