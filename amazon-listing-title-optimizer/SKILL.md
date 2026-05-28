---
name: amazon-listing-title-optimizer
description: optimize amazon listing titles by prioritizing real amazon keyword data first, then balancing search relevance, clarity, readability, and conversion. use when the user wants to create, improve, compare, or clean up amazon product titles, especially when keyword lists, search terms, or marketplace constraints are available.
---

# Amazon Listing Title Optimizer

Build and improve Amazon listing titles with a strict rule: prioritize real Amazon keyword data whenever it is available. If no real keyword data is available, explicitly warn the user before presenting a final title.

## Overview

Use this skill for Amazon title work that must balance:
- keyword relevance
- product clarity
- readability
- conversion potential
- marketplace discipline

This skill is for title optimization, not standalone keyword research. It can use keyword data provided by the user, but it does not invent search volume data.

## Core rules

- Always prioritize real Amazon keyword data when available.
- Treat provided Amazon search terms, validated keyword lists, marketplace term reports, or other user-supplied Amazon keyword inputs as the primary source for title decisions.
- If no real Amazon keyword data is available, explicitly tell the user before generating final titles.
- In that case, produce a marketplace-informed title based on product logic and best judgment, but do not present it as fully keyword-validated.
- Do not imply maximum SEO optimization without real keyword evidence.
- Do not stuff keywords or create unreadable titles.
- Prefer titles that identify the product quickly and clearly.
- Remove weak, vague, repetitive, or filler language.
- Keep only the words that truly earn their place in the title.

## Mandatory keyword transparency

Before producing a final title, determine which of these cases applies.

### Case 1: real Amazon keyword data is available

Examples:
- search term lists from Helium 10, Data Dive, Jungle Scout, Amazon Ads, Search Query Performance, or manual Amazon query analysis
- user-provided keyword priorities
- validated search phrases from marketplace work

When keyword data is available:
- use it as the primary decision layer
- identify the likely main keyword
- identify secondary and supporting keywords
- decide which terms belong in the title versus bullets or backend fields
- explain what was kept and what was excluded

### Case 2: no real Amazon keyword data is available

Before writing the final title, explicitly say that:
- the title will be optimized from product logic and marketplace best judgment
- the result may be strong commercially and structurally
- but it is not the most defensible keyword-optimized title possible without real search data

Use direct language. Do not hide this limitation.

## Supported tasks

Use this skill when the user wants to:
- create a new Amazon title from a product description
- improve or clean up an existing title
- compare several title options
- remove keyword stuffing
- decide what belongs in the title versus bullet points
- build title variants such as:
  - more SEO-focused
  - more readable
  - more conversion-focused

## Title construction logic

Build titles as a priority stack, not as a keyword dump.

Default construction order:
1. Brand, when required or strategically useful
2. Core product name or product type
3. Main buying attribute or main keyword qualifier
4. Critical size, capacity, quantity, compatibility, or model detail
5. One or two high-value differentiators
6. Optional context or usage only if it genuinely improves clarity or targeting

Use the guidance in `references/title-framework.md`.

## Keyword selection logic

Separate keywords into tiers.

### Tier 1: essential product-defining terms
These identify the product directly. They usually belong early in the title.

### Tier 2: decision-shaping qualifiers
These improve precision, filtering, and buyer confidence.

### Tier 3: secondary or removable terms
These may help elsewhere in the listing, but do not always deserve title placement.

Use the decision rules in `references/keyword-priority.md`.

## Optimization workflow

Follow this sequence unless the user requests only one subtask.

1. Check whether real Amazon keyword data is available
2. State the keyword-data status clearly
3. Identify the main product term
4. Identify title-worthy attributes
5. Rank title elements by importance
6. Build 1 to 3 title variants
7. Recommend the strongest version
8. Explain what was kept, removed, and why

## Existing-title cleanup workflow

When the user provides an existing title:
1. Diagnose what is wrong
2. Identify:
   - redundancies
   - weak adjectives
   - filler claims
   - poor ordering
   - bad readability
3. Keep the highest-value terms
4. Rewrite into cleaner alternatives
5. Explain why the final version is stronger

## Output style

Use practical, structured outputs with clear headings.

A sensible default output is:
1. Keyword-data status
2. Main keyword
3. Elements worth keeping
4. Priority order
5. Title variants
6. Recommended title
7. Why it is best
8. What was excluded and why

When the user asks for a rewrite of an existing title, add:
- what is wrong with the original
- what must be removed
- what must stay

## Quality checks

Before finalizing, verify:
- the product is identifiable in under two seconds
- the likely main keyword appears clearly
- the title is readable by a human
- repeated or vague terms are removed
- the title does not feel like raw keyword stuffing
- excluded terms have a reason for being excluded
- the user has been warned if no real Amazon keyword data was provided

## Mistakes to avoid

- pretending a title is fully SEO-optimized without keyword data
- keeping every possible keyword
- repeating synonyms that do the same job
- using vague filler such as premium, high quality, professional, excellent, comfortable, or practical unless there is a rare category-specific reason
- making the title sound like a search query dump
- hiding important tradeoffs from the user

## Example requests

- "Improve this Amazon title."
- "Create a title from these keywords and product details."
- "Give me 3 Amazon title variants and choose the best one."
- "Tell me what to remove from this stuffed title."
- "Use these Amazon search terms to build a better title."
