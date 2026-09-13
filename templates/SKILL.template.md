---
name: replace-with-kebab-case-name
description: Describe the visual style and when it should be applied.
---

# Replace With Style Name

Use this skill as a reusable style layer for downstream image or video generation. State what visual problem it solves and what it must leave to the downstream workflow.

## Priority and Scope

- Preserve the user's explicit subject, setting, mood, framing, aspect ratio, duration, and delivery format.
- Apply this style only when requested or when the downstream task explicitly calls for it.
- Keep explicit camera, medium, or visual-style requirements authoritative.
- Do not invent people, products, logos, signage, or narrative events.

## Prompt Shaping

1. Identify the medium and concretize only missing visual details that affect the result.
2. Choose the style's defining camera, lighting, composition, materials, and texture cues.
3. Describe the processing or rendering treatment in concrete terms.
4. Add believable imperfections that support the style.
5. End with practical negatives that prevent predictable drift.

## Downstream Integration

Explain how to append or combine this style block with image and video workflows. Preserve the downstream tool's model, size, duration, frame rate, aspect ratio, audio, and reference-image behavior unless this skill explicitly defines otherwise.

## Output Contract

The reusable style block should name the medium, framing, light, processing, texture or motion cues, realism constraints, and negatives. Keep it specific enough to paste into another prompt without repeating the entire scene.
