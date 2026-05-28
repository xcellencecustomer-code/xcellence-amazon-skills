---
name: amazon-profitable-cpc-evaluator
description: evaluate profitable amazon cpc by prioritizing real product economics, conversion quality, and tacos targets before judging whether a cpc is good, acceptable, dangerous, or misleading. use when the user wants to calculate a supportable cpc, compare real cpc against profitable cpc, or make bidding decisions based on price, conversion, tacos, and data reliability.
---

# Amazon Profitable CPC Evaluator

Evaluate Amazon CPC with a strict rule: prioritize real product economics, conversion quality, and TACOS targets before giving a final judgment. If important conversion, TACOS, or context inputs are missing, explicitly warn the user before presenting a final verdict.

## Overview

Use this skill for CPC work that must balance:
- selling price
- conversion rate
- TACOS target
- product economics
- uncertainty in the data
- bid risk
- business decision quality

This skill is for profitable CPC evaluation and target definition, not for generic bid folklore. It does not assume that a cheap CPC is automatically good.

## Core rules

- Never judge a CPC in isolation.
- Always connect CPC to:
  - selling price
  - conversion rate
  - TACOS target
  - real business context
- Do not use generic rules such as "0.50 is expensive" without product context.
- Treat CPC as a ceiling problem, not just a bidding problem.
- Distinguish clearly:
  - good CPC
  - acceptable CPC
  - dangerous CPC
  - misleading CPC
- When data is unstable, say so explicitly.
- End with a decision and operating zone, not just a number.

## Mandatory data transparency

Before producing a final judgment, determine which of these cases applies.

### Case 1: key data is available

Preferred inputs:
- selling price
- current or target TACOS
- conversion data, ideally from a meaningful window such as 28 days
- enough volume to judge whether the conversion rate is stable
- current CPC if the user wants a comparison verdict

When these inputs are available:
- use them as the primary decision layer
- calculate supportable CPC
- create prudent, median, and aggressive zones when possible
- compare current CPC against those zones
- explain the business implications

### Case 2: important data is missing

Before giving the final verdict, explicitly say that:
- the evaluation will be partial or provisional
- the result is based on incomplete conversion, TACOS, or context inputs
- the output should not be treated as a fully reliable CPC target until the missing data is added

Use direct language. Do not hide this limitation.

## Supported tasks

Use this skill when the user wants to:
- calculate a profitable CPC ceiling
- define a realistic bidding zone
- compare actual CPC to a supportable CPC
- evaluate whether current bid levels are safe
- understand how price, conversion, and TACOS interact
- make cautious, normal, or offensive CPC decisions
- judge whether a CPC is good, acceptable, dangerous, or misleading

## Evaluation sequence

Follow this sequence unless the user explicitly asks for only one subtask.

1. Confirm data completeness
2. State whether the evaluation is complete or provisional
3. Define the conversion inputs
4. Define the TACOS target
5. Calculate profitable CPC
6. Build low, median, and high CPC scenarios when possible
7. Compare actual CPC to supportable CPC
8. Classify the current CPC
9. Give the business decision and vigilance points

Use the guidance in `references/calculation-framework.md`.

## Core formula logic

Use this core formula unless the user provides a different accounting logic:

### Profitable CPC
profitable cpc = selling price × conversion rate × tacos target

Interpretation:
- selling price gives the economic size of a sale
- conversion rate gives the probability that a click becomes a sale
- TACOS target defines the share of revenue that can go to ads

The result is a supportable CPC ceiling under the chosen assumptions.

## Conversion uncertainty logic

Do not treat one observed conversion rate as absolute truth.

When possible, build:
- low conversion scenario
- median conversion scenario
- high conversion scenario

Use this to produce:
- prudent CPC
- median CPC
- aggressive CPC

Use the guidance in `references/conversion-uncertainty.md`.

## Business interpretation logic

A CPC can only be judged after reviewing:
- the price of the product
- the conversion reality
- the TACOS target allowed by the product
- the volume and quality of the data
- whether the product is in cautious, normal, or aggressive mode
- whether the current CPC depends on overly optimistic assumptions

A low CPC can be misleading.
A high CPC can be acceptable if the product converts extremely well and supports it economically.
Always explain why.

## Default classification language

Use these labels:
- good
- acceptable
- dangerous
- misleading

You may also add zone language such as:
- prudent
- normal
- aggressive

## Output style

Use practical, structured outputs with clear headings.

A sensible default output is:
1. Data completeness status
2. Conversion assumptions
3. Profitable CPC low / median / high
4. Current CPC classification
5. CPC zone to target
6. Key vigilance points
7. Final business verdict

## Quality checks

Before finalizing, verify:
- the CPC was not judged alone
- the conversion data was used or clearly marked as missing
- the TACOS target is explicit
- the user understands that the result is a ceiling, not blind bidding advice
- uncertainty is addressed when data is weak
- the user has been warned if key inputs are missing

## Mistakes to avoid

- calling a CPC good just because it is low
- using one fragile conversion rate as certainty
- ignoring TACOS constraints
- ignoring product price
- ignoring low sample size
- pretending a partial calculation is fully reliable

## Example requests

- "What CPC can this product support?"
- "Is my current CPC profitable?"
- "Calculate my profitable CPC."
- "Give me a safe, normal, and aggressive CPC zone."
- "Tell me if this CPC is dangerous or acceptable."
