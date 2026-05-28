---
name: amazon-conversion-rate-evaluator
description: evaluate amazon conversion rate by prioritizing useful buying-opportunity data, traffic quality, offer strength, and statistical reliability before judging whether a conversion rate is good, weak, dangerous, or misleading. use when the user wants to calculate conversion rate, diagnose weak conversion, separate traffic problems from listing or offer problems, or define a realistic conversion target for a product.
---

# Amazon Conversion Rate Evaluator

Evaluate Amazon conversion rate with a strict rule: prioritize useful buying-opportunity data, traffic quality, offer strength, and data reliability before giving a final judgment. If important inputs such as Buy Box context, volume, traffic quality, or order data are missing, explicitly warn the user before presenting a final verdict.

## Overview

Use this skill for Amazon conversion-rate work that must balance:
- real buying opportunity
- traffic quality
- listing strength
- offer competitiveness
- product-market fit
- statistical reliability
- business decision quality

This skill is for conversion-rate evaluation and diagnosis, not for blind benchmark quoting. It does not assume that a raw percentage alone tells the truth.

## Core rules

- Never judge a conversion rate in isolation.
- Always connect conversion rate to:
  - traffic intent
  - Buy Box availability or buying opportunity
  - offer strength
  - listing quality
  - review and proof layer
  - product economics
  - data stability
- Distinguish clearly between:
  - a traffic problem
  - a conversion problem
  - an offer problem
  - a product problem
  - a misleading data problem
- Do not use generic category folklore as a final answer without context.
- End with a decision and likely cause, not just a percentage comment.

## Mandatory data transparency

Before producing a final judgment, determine which of these cases applies.

### Case 1: useful conversion inputs are available

Preferred inputs:
- order count
- page views or sessions
- Buy Box context if available
- time window
- enough volume to judge stability
- at least some context on traffic quality, offer status, and product stage

When these inputs are available:
- calculate the conversion rate using the chosen logic
- explain whether the result is statistically meaningful
- diagnose where the main friction likely sits
- define a practical target or improvement direction
- explain the business implications

### Case 2: important data is missing

Before giving the final verdict, explicitly say that:
- the evaluation will be partial or provisional
- the result is based on incomplete traffic, Buy Box, or reliability context
- the output should not be treated as a fully reliable conversion diagnosis until the missing data is added

Use direct language. Do not hide this limitation.

## Supported tasks

Use this skill when the user wants to:
- calculate Amazon conversion rate
- judge whether current conversion is healthy
- diagnose why conversion is weak
- separate a listing issue from a traffic issue
- separate an offer issue from a product issue
- define a realistic conversion target
- interpret conversion using orders, views, Buy Box, and context

## Calculation logic

Acknowledge two possible readings:

### Classic conversion rate
orders / visitors or sessions

### Amazon buying-opportunity conversion logic
Use when the user wants a more operational Amazon reading and has Buy Box context:
- estimate useful buying opportunity using page views plus Buy Box exposure context
- evaluate conversion against the real chance to buy, not only headline traffic

If the user explicitly uses a custom internal formula, apply it, but explain what it measures.
Do not pretend that all conversion formulas answer the same question.

Use the guidance in `references/calculation-framework.md`.

## Evaluation sequence

Follow this sequence unless the user explicitly asks for only one subtask.

1. Confirm the available inputs
2. State whether the evaluation is complete or provisional
3. Define the conversion formula being used
4. Check data volume and reliability
5. Judge whether the observed rate is stable, weak, strong, or misleading
6. Diagnose the dominant issue:
   - traffic
   - listing conversion
   - offer
   - product
   - data distortion
7. Set a realistic target zone or next-action priority
8. Give the business decision

Use the guidance in `references/diagnostic-framework.md`.

## Diagnostic logic

When conversion is weak, do not jump straight to “bad listing”.

Check these causes:

### Traffic problem
The wrong audience is arriving.
Signals:
- broad or cold traffic
- poor keyword-match quality
- many visits but little buyer intent
- external or exploratory traffic dragging the rate down

### Listing conversion problem
The right audience arrives, but the listing fails to persuade.
Signals:
- weak images
- unclear title or bullets
- objections not handled
- weak review proof
- poor explanation of benefits or differences

### Offer problem
The customer is interested, but the commercial conditions are weak.
Signals:
- price too high
- weak coupon or promo setup
- poor delivery promise
- unstable or weak Buy Box presence
- bad variation availability

### Product problem
The product itself is not competitive enough even with a decent listing and offer.
Signals:
- weak differentiation
- recurring disappointment in feedback
- unclear reason to choose it
- persistent underperformance despite solid traffic and listing work

### Misleading-data problem
The data should not be over-interpreted.
Signals:
- low volume
- short time window
- major promo distortion
- stock disruption
- Buy Box instability
- abrupt campaign changes
- seasonality effects

## Target-setting logic

Do not set a magic target percentage.
Set a practical target by asking:
- where is the product now
- how reliable is the current number
- what kind of product is this
- how strong is traffic intent
- what can realistically be improved next

Prefer three levels:
- minimum acceptable zone
- healthy zone
- realistic excellence zone

Use the guidance in `references/target-zone-logic.md`.

## Output style

Use practical, structured outputs with clear headings.

A sensible default output is:
1. Data completeness status
2. Formula used
3. Observed conversion rate
4. Reliability and volume check
5. Main diagnosis
6. Target zone or next target
7. Priority action
8. Final business verdict

## Quality checks

Before finalizing, verify:
- the conversion rate was not judged alone
- the formula used is explicit
- traffic quality was considered
- Buy Box or buying-opportunity context was considered if available
- weak data was flagged clearly
- the likely cause category is stated
- the user has been warned if inputs are incomplete

## Mistakes to avoid

- calling a conversion rate good or bad without context
- ignoring weak volume
- confusing traffic mismatch with listing weakness
- ignoring offer competitiveness
- ignoring Buy Box issues
- pretending a provisional diagnosis is fully reliable

## Example requests

- "Calculate my Amazon conversion rate."
- "Is my current conversion rate healthy?"
- "Tell me if this is a traffic problem or a listing problem."
- "Help me diagnose weak conversion on this ASIN."
- "What conversion rate should I aim for on this product?"
