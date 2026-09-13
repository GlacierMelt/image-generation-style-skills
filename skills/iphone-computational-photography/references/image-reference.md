# Image Reference Contract

Use this contract when a user requests a strict JSON prompt package. It is compatible with image relay skills because the `full_prompt_string` is directly usable as a prompt, while the other fields remain inspectable metadata.

```json
{
  "meta_data": {
    "style": "iPhone Pro Max Photography",
    "aspect_ratio": "9:16"
  },
  "prompt_components": {
    "subject": "The main subject and its visible physical details",
    "environment": "Place, season, weather, background, and social context",
    "lighting": "Natural source, direction, contrast, and Smart HDR behavior",
    "camera_gear": "One iPhone lens choice and the framing/viewpoint",
    "processing": "Apple ProRAW-inspired color, Deep Fusion-like detail, and Smart HDR",
    "imperfections": "Digital noise, realistic texture, exposure limits, and snapshot artifacts"
  },
  "full_prompt_string": "A single comma-separated or prose prompt combining the components",
  "negative_prompt": "Professional-camera look, DSLR, exaggerated bokeh, bokeh balls, anamorphic flares, cinema or studio lighting, film grain, CGI, text, logo, watermark"
}
```

Guidance:

- `subject` is not limited to people; for landscapes, describe the station, terrain, architecture, or object that must read clearly.
- Use `13mm` only when the environment is the subject and edge distortion is acceptable. Use `24mm` as the default general-purpose lens. Use `77mm` for distant wildlife, architecture, or layered mountain views.
- Do not claim that an image was literally captured by an iPhone. Phrase it as “simulate” or “iPhone-inspired” when provenance matters.
- Keep the image naturally sharp across a landscape. Computational portrait blur is appropriate only when the scene calls for a close subject and the user accepts it.
