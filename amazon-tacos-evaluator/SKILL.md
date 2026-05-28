---
name: amazon-tacos-evaluator
description: evaluate amazon tacos by prioritizing real product economics and business context before judging whether a tacos is good, acceptable, dangerous, or misleading. use when the user wants to calculate tacos capacity, define a tacos target, judge current ad pressure, or make a business decision based on margin, phase, organics, and advertising dependence.
---

# Amazon TACOS Evaluator

Evaluate Amazon TACOS with a strict rule: prioritize real product economics and business context before giving a final judgment. If important cost or context inputs are missing, explicitly warn the user before presenting a final verdict.

## Overview

Use this skill for TACOS work that must balance:
- real product margin
- ad pressure
- business objective
- stage of product maturity
- organic contribution
- sustainability of the current ad level
- business decision quality

This skill is for TACOS evaluation and target definition, not for generic benchmark quoting. It does not assume that a low TACOS is automatically good.

## Core rules

- Never judge a TACOS in isolation.
- Always start from real economics:
  - selling price
  - product cost
  - amazon logistics cost
  - amazon commercial cost
- Then evaluate TACOS in context:
  - launch, stabilization, or profit phase
  - organic sales contribution
  - trend direction
  - ad dependence
  - traffic quality
  - competitive pressure
- Do not use generic rules such as "10 percent is good" without product context.
- Distinguish clearly:
  - profitable TACOS
  - acceptable TACOS
  - dangerous TACOS
  - misleading TACOS
- End with a business decision, not just a percentage comment.

## Mandatory data transparency

Before producing a final judgment, determine which of these cases applies.

### Case 1: core economic data is available

Minimum preferred inputs:
- selling price
- product cost
- amazon logistics cost
- amazon commercial cost
- current TACOS or ad spend
- product phase if possible
- at least some context on organic sales and market conditions

When these inputs are available:
- use them as the primary decision layer
- calculate margin before ads
- calculate theoretical maximum TACOS
- define a safer target zone
- classify the current TACOS
- explain the business implications

### Case 2: important cost or context data is missing

Before giving the final verdict, explicitly say that:
- the evaluation will be partial or provisional
- the result is based on incomplete economics or incomplete business context
- the output should not be treated as a fully reliable TACOS target until the missing data is added

Use direct language. Do not hide this limitation.

## Supported tasks

Use this skill when the user wants to:
- calculate the maximum TACOS a product can support
- define a reasonable TACOS target
- judge whether the current TACOS is healthy
- understand whether a TACOS is good, acceptable, dangerous, or misleading
- compare TACOS against real margin capacity
- make a business decision about ad pressure, scaling, or correction
- build a simple decision framework such as green / watch / alert / danger

## Evaluation sequence

Follow this sequence unless the user explicitly asks for only one subtask.

1. Confirm the available inputs
2. State whether the evaluation is complete or provisional
3. Calculate margin before ads
4. Convert that margin into a theoretical maximum TACOS
5. Keep a safety buffer below the theoretical maximum
6. Adjust the target zone according to business objective
7. Validate with contribution margin after ads
8. Classify the current TACOS
9. State the business decision and monitoring points

Use the guidance in `references/calculation-framework.md`.

## Core calculation logic

Use these formulas unless the user gives a different accounting logic.

### Margin before ads
margin before ads = selling price - product cost - amazon logistics cost - amazon commercial cost

### Theoretical maximum TACOS
theoretical maximum tacos = margin before ads / selling price

This is an absolute ceiling, not a target.

### Ad spend equivalent from TACOS
ad spend equivalent = selling price × tacos

### Contribution margin after ads
contribution margin after ads = margin before ads - ad spend equivalent

### Contribution margin rate after ads
contribution margin rate after ads = contribution margin after ads / selling price

Use the guidance in `references/risk-classification.md`.

## Business interpretation logic

A TACOS can only be judged after reviewing:
- whether the product is in launch, stabilization, or profit mode
- whether ads are creating or defending meaningful organic sales
- whether the current TACOS trend is improving or deteriorating
- whether traffic quality is strong or weak
- whether the product is overly dependent on ads to survive

A low TACOS can be misleading.
A high TACOS can be strategically acceptable.
Always explain why.

## Default classification language

Use these labels:
- profitable
- acceptable
- dangerous
- misleading

You may also add a target-zone interpretation such as:
- good base
- under watch
- alert
- danger

## Output style

Use practical, structured outputs with clear headings.

A sensible default output is:
1. Data completeness status
2. Margin before ads
3. Theoretical maximum TACOS
4. Current TACOS classification
5. Suggested TACOS target zone
6. Key vigilance points
7. Final business verdict

## Quality checks

Before finalizing, verify:
- the TACOS was not judged alone
- the economics were calculated or clearly marked as missing
- the ceiling and the target are not confused
- the product phase is considered
- the role of organics is considered
- the user has been warned if key inputs are missing

## Mistakes to avoid

- using category folklore instead of real economics
- calling a TACOS good just because it is low
- ignoring contribution margin after ads
- ignoring phase of product maturity
- ignoring ad dependence
- ignoring a slow TACOS deterioration trend
- pretending an incomplete calculation is fully reliable

## Example requests

- "Is my current TACOS healthy?"
- "What TACOS should I target for this product?"
- "Calculate the maximum TACOS this product can support."
- "Tell me whether this TACOS is profitable or dangerous."
- "Build me a simple TACOS decision zone for this product."
