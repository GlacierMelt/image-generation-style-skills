# Video Adaptation

Add these constraints to a video prompt after the scene and shot design are established:

## Temporal Camera Behavior

- Simulate a handheld iPhone with restrained stabilization: small human micro-movements, no floating drone motion, no impossible acceleration, and no abrupt lens switching.
- Keep one lens and a consistent field of view within each shot. Use a gentle push-in, pan, or walking move only when it supports the subject.
- Preserve believable autofocus transitions, exposure adaptation, and motion blur. These changes should be gradual rather than flickering frame to frame.

## Computational Look Over Time

- Maintain stable Apple ProRAW-inspired color, Smart HDR highlight recovery, and Deep Fusion-like fine detail throughout the shot.
- Keep snow, skin, water, foliage, metal, and fabric temporally coherent. Do not let textures crawl, shimmer, sharpen, or melt between frames.
- Allow subtle mobile-camera imperfections: faint shadow noise, occasional highlight clipping, and natural rolling-shutter character only when motion makes it plausible. Do not add film grain or a fake cinematic LUT.

## Video Negatives

Add only the negatives relevant to the shot: DSLR/pro-camera look, anamorphic flare, cinema bokeh, bokeh balls, studio lighting, artificial HDR halos, excessive sharpening, frame flicker, texture crawling, focus pumping, exposure pulsing, warped architecture, unstable horizon, text, logos, and watermarks.

## Example Style Block

```text
iPhone 16/17 Pro Max mobile-photography simulation, 24mm Main camera for this shot, restrained handheld stabilization, natural autofocus and exposure adaptation, Apple ProRAW-inspired color, Smart HDR highlight retention, Deep Fusion-like texture detail, authentic surface texture, subtle shadow digital noise, physically coherent motion blur, stable lens and color across frames, no DSLR look, no anamorphic flare, no cinematic bokeh, no frame flicker or texture crawling.
```
