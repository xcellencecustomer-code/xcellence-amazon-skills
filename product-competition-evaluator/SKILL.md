---
name: product-competition-evaluator
description: evaluate a product against the competition by prioritizing real competitor, market, and customer-perception data whenever available. use when the user wants to assess product strength, weaknesses, positioning, differentiation, false advantages, or market potential before building messaging, listings, or launch strategy.
---

# Product Competition Evaluator

Evaluate a product against the competition with a strict rule: prioritize real competitor and market data whenever it is available. If no competitor-market data is available, explicitly warn the user before presenting a final verdict.

## Overview

Use this skill for product evaluation work that must balance:
- customer need
- product value
- competitive reality
- perceived differentiation
- pricing logic
- market proof
- commercial defensibility

This skill is for product evaluation and comparative strategy, not for standalone scraping or market-research collection. It can use competitor and market inputs supplied by the user, but it does not invent competitive proof.

## Core rules

- Always prioritize real competitor-market data when available.
- Treat competitor listings, review summaries, pricing snapshots, feature comparisons, market pain points, and customer-language insights as the strongest input layer for evaluation.
- If no real competitor-market input is available, explicitly tell the user before generating a final verdict.
- In that case, produce a provisional evaluation based on product logic, category expectations, and common market patterns, but do not present it as a fully validated competitive assessment.
- Never judge a product in isolation.
- Always connect:
  - customer need
  - product promise
  - competitor offer reality
  - customer perception
  - ability to win sales
- Distinguish true strengths from weak claims and false advantages.
- End with an actionable verdict, not just observations.

## Mandatory competitor-market transparency

Before producing a final evaluation, determine which of these cases applies.

### Case 1: competitor-market input is available

Examples:
- scraped competitor tables
- review summaries
- competitor pricing
- side-by-side feature comparisons
- customer complaints or praise patterns
- market notes from spreadsheets, docs, or manual research

When competitor-market input is available:
- use it as the primary decision layer
- identify what the market already values
- identify recurring weaknesses in competing offers
- identify whether the product's differences matter commercially
- explain what insights were used

### Case 2: no competitor-market input is available

Before writing the final verdict, explicitly say that:
- the evaluation will be provisional
- it will be based on product logic, category expectations, and likely market dynamics
- it is not a fully validated competitor-grounded assessment

Use direct language. Do not hide this limitation.

## Supported tasks

Use this skill when the user wants to:
- evaluate whether a product has real market potential
- compare a product to competing offers
- identify true strengths, weaknesses, and false advantages
- judge whether the value proposition is strong enough
- assess whether the price is justified by perceived value
- find which angle or segment gives the product the best chance to win
- build the strategic base for later work such as persona, title, bullets, photos, or launch positioning

## Evaluation sequence

Follow this sequence unless the user explicitly asks for only one subtask.

1. Clarify the product itself
2. Clarify the customer need or core problem solved
3. Identify the value proposition
4. Map the relevant competitor types
5. Compare fundamentals
6. Compare customer perception and market proof
7. Separate true strengths, weaknesses, and false advantages
8. Give a potential verdict
9. Recommend what to verify or improve next

Use the guidance in `references/evaluation-framework.md`.

## Product understanding phase

Before comparing, establish:
- what the product is
- who it is for
- what problem it solves
- the main promise
- key attributes
- likely differentiators
- price or likely price band if available

Do not compare until the product definition is clear enough.

## Competitive comparison logic

Compare a product against the competition in layers:
- problem solved
- value proposition
- useful attributes
- differentiation
- perceived quality
- price and value logic
- review proof
- structural risks

Use `references/strength-weakness-false-advantage.md`.

## Verdict logic

Classify the product into one of these states by default:
- strong potential
- real potential but needs reinforcement
- weak potential
- misleading potential

Use `references/potential-verdicts.md`.

The verdict must explain:
- why the product deserves to exist or not
- why a buyer would choose it or not
- what must be strengthened to improve the odds of success

## Output style

Use practical, structured outputs with clear headings.

A sensible default output is:
1. Competitor-market status
2. Core need addressed
3. Value proposition
4. Credible strengths
5. Structural weaknesses
6. Likely false advantages
7. Real competitor groups
8. Provisional or final potential verdict
9. What to verify next
10. Priority recommendations

## Quality checks

Before finalizing, verify:
- the product is not being judged in isolation
- strengths matter to the buyer, not just to the seller
- weak points are commercially meaningful
- false advantages are clearly separated from real ones
- the verdict is actionable
- the user has been warned if competitor-market input was missing

## Mistakes to avoid

- calling a product differentiated just because it has many features
- treating expected category standards as strong advantages
- confusing a claim with proof
- ignoring the buyer’s real decision criteria
- ignoring competitor saturation
- presenting a provisional assessment as fully validated

## Example requests

- "Evaluate my product against the competition."
- "Tell me if this product has real market potential."
- "Compare my offer to existing competitors."
- "Identify the true strengths and false advantages of this product."
- "Give me a commercial verdict on this product before launch."
