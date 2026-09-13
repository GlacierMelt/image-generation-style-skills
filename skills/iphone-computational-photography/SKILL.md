---
name: iphone-computational-photography
description: Shape realistic iPhone computational-photography prompts for image and video generation, especially when another relay or video skill needs a reusable visual-style reference.
---

# iPhone Computational Photography

Use this skill as a style layer for downstream image and video generation skills. It translates a scene brief into a realistic high-end mobile-photography treatment; it does not choose models, call APIs, manage credentials, or override a downstream tool's size, duration, frame rate, or aspect ratio.

## Priority and Scope

- Preserve the user's explicit subject, setting, mood, aspect ratio, duration, and delivery format.
- Apply this style only when requested or when the downstream task explicitly asks for an iPhone/mobile-photography reference.
- If the user explicitly requests another camera or visual style, keep that request authoritative and use only compatible parts of this guide.
- Do not invent extra people, products, logos, signage, or narrative events merely to make a vague prompt longer.

## Prompt Shaping

1. Identify the medium: still image or video. For a vague brief, concretize only the missing details that affect the image: location, time, weather, light direction, composition, materials, and realistic environmental traces.
2. Choose one plausible iPhone lens: 24mm-equivalent Main for general scenes, 13mm Ultra Wide for expansive spaces, or 77mm Telephoto for distant subjects and compressed layers. Do not list multiple lenses unless the downstream video is intentionally a multi-shot sequence.
3. Describe the mobile image pipeline: Apple ProRAW-inspired color, Smart HDR dynamic range, Deep Fusion-like texture retention, restrained sharpening, and natural white balance.
4. Add realism cues: authentic surface texture, imperfect but believable exposure, faint digital noise in shadows, minor motion blur when movement implies it, and natural snapshot framing. Use digital noise, never film grain, unless the user requests a filter.
5. End with practical negatives: DSLR/professional-camera look, exaggerated cinematic bokeh, bokeh balls, anamorphic flares, studio lighting, artificial HDR halos, CGI/plastic textures, text, logos, and watermarks. Remove any negative that conflicts with an explicit user requirement.

## Downstream Integration

- For `gpt-image-2-relay` or `nano-banana-relay`, append the generated `full_prompt_string` or style block to the user's prompt. Leave the selected model, relay profile, quality, size, and reference-image behavior unchanged.
- For video-generation skills, preserve their existing duration, FPS, aspect ratio, audio, and shot structure. Add the temporal guidance in [references/video-adaptation.md](references/video-adaptation.md) so exposure, focus, texture, and camera motion remain coherent across frames.
- For a standalone image prompt request, use the JSON contract in [references/image-reference.md](references/image-reference.md) when the user asks for JSON or programmatic output. Otherwise return a concise reusable style block.
- Never put API keys, relay URLs, CLI commands, or tool-specific credentials into the style block.

## Output Contract

The reusable style block should name: medium, lens, framing, light, processing, realism imperfections, and negatives. Keep it specific enough to paste into another skill, but do not restate the entire scene when the downstream prompt already contains it.

Read the image reference only for structured image output. Read the video adaptation reference only when the target is a generated video.
