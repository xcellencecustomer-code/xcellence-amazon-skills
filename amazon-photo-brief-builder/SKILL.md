---
name: amazon-photo-brief-builder
description: build amazon photo briefs as a visual conversion sequence by aligning product promise, customer needs, key benefits, objections, and amazon image rules. use when the user wants to define image strategy, plan listing visuals, brief a photographer or designer, or decide what each amazon image should prove and why.
---

# Amazon Photo Brief Builder

Build Amazon photo briefs as a visual selling sequence. The goal is not to make images that merely look good. The goal is to define what each image must communicate, which objection it must reduce, which benefit it must prove, and how the full image set supports clicks and conversion.

## Overview

Use this skill for Amazon image planning that must balance:
- click strength in search
- clarity on mobile
- benefit communication
- objection handling
- visual proof
- customer projection
- Amazon image compliance

This skill is for visual strategy and creative briefing. It does not generate final images by itself. It creates a strong, usable brief for designers, photographers, or downstream creative systems.

## Core rules

- Treat the image stack as a visual sales sequence, not as decoration.
- Every image must have a distinct mission.
- Do not let characteristics appear in the brief as raw technical filler.
- Only include a characteristic when it:
  - supports a real benefit
  - proves a promise
  - reduces an objection
  - clarifies compatibility, size, or usage
- Align the brief with:
  - title
  - bullets
  - ideal customer
  - product promise
  - main objections
- The main image must respect Amazon rules before anything else.
- Secondary images should make the product understandable almost without reading.
- Prefer fast comprehension over visual cleverness.

## Mandatory input transparency

Before producing a final brief, determine which of these cases applies.

### Case 1: strong strategic inputs are available

Best inputs include:
- product definition
- title or main promise
- bullet points or key benefits
- ideal customer
- main objections
- differentiators
- size, format, compatibility, or pack details
- category constraints

When these are available:
- use them as the main decision layer
- rank the strongest visual messages
- map each message to the best image type
- build a complete image-by-image brief
- explain why each image exists

### Case 2: some important inputs are missing

Before producing the final brief, explicitly say that:
- the brief will be provisional
- some visual choices are being inferred from product logic and Amazon best practice
- the result should be refined when title, bullets, objections, or customer information become available

Use direct language. Do not hide this limitation.

## Supported tasks

Use this skill when the user wants to:
- build a full Amazon image brief
- decide what each image should communicate
- structure the main image and secondary images
- translate bullets into image messages
- identify which objections images must solve
- remove decorative or redundant images
- prepare instructions for a designer, photographer, or creative team

## Default image-sequence logic

Use this default sequence unless the category or product requires a different order:

1. Main image for click and product recognition
2. Strongest product benefit
3. Second strongest benefit
4. Proof, construction, or differentiation
5. Key objection handling
6. Projection or real-use reassurance
7. Size, variants, compatibility, pack contents, or final clarification

Use the guidance in `references/image-sequence-framework.md`.

## Visual-message logic

Before assigning an image, define:
- the message
- the buyer question behind that message
- what the customer should understand in 1 second
- the best visual format for that message

Possible visual formats include:
- compliant main packshot
- macro material detail
- comparison visual
- simplified infographic
- demonstration scene
- usage scene
- dimensions / compatibility visual
- pack-content clarification
- simple feature-proof visual

The visual format must serve the message, never the reverse.

## Useful vs decorative image rule

An image is useful if it does at least one of these:
- makes a core benefit clearer
- proves a promise
- reduces uncertainty
- handles a strong objection
- helps the buyer compare or choose
- makes the product easier to imagine in real use

An image is weak or decorative if it:
- repeats another image
- adds atmosphere with no sales value
- hides the product
- relies on too much text
- explains nothing important
- would be missed if removed

Use `references/useful-vs-decorative.md`.

## Main image rule

Always respect Amazon main-image rules in the brief:
- pure white background
- only the product sold
- strong product visibility
- clean framing
- no misleading accessories
- no text or badges on the main image
- no non-compliant decorative elements

Do not compromise compliance for creativity.

## Brief construction sequence

Follow this sequence unless the user explicitly asks for only one subtask.

1. Clarify the product and category
2. Clarify the central product promise
3. Identify the customer and use context
4. Rank the most important benefits and objections
5. Select 5 to 7 visual messages
6. Assign each image a distinct role
7. State what each image must communicate in 1 second
8. Choose the recommended image type
9. Add execution notes for design or photography
10. Flag weak or decorative image ideas to avoid

## Output style

Use practical, structured outputs with clear headings.

A sensible default output is:
1. Input completeness status
2. Central promise
3. Priority visual messages
4. Image-by-image roles
5. One-second takeaway for each image
6. Recommended visual type for each image
7. Images to avoid
8. Final brief ready for a designer or photographer

## Quality checks

Before finalizing, verify:
- each image has one dominant mission
- the main image is compliant
- the strongest benefits appear early
- objections are covered
- the sequence is understandable on mobile
- characteristics appear only when they support a commercial job
- decorative repetition has been removed
- the user was warned if important strategic inputs were missing

## Mistakes to avoid

- writing a decorative mood board instead of a sales brief
- repeating the same benefit in several images
- putting raw technical characteristics into visuals without buyer meaning
- overloading secondary images with text
- using unrealistic demonstrations that hurt credibility
- hiding uncertainty when the brief lacks key strategic inputs

## Example requests

- "Create an Amazon photo brief for this product."
- "Tell me what each image should show."
- "Turn these bullets into an image plan."
- "Identify which images are weak or decorative."
- "Give me a brief I can send to a designer."
