---
style_name: Analog Horror
aliases: Analog Horror Aesthetic, VHS Horror, Retro Analog Horror, Liminal Analog Horror, Distorted Broadcast Aesthetic, Found Footage Horror UI
description: An unsettling digital horror style that emulates degraded analog media from the late 20th century, such as VHS tapes, CRT televisions, and public access broadcasts. It uses heavy grain, tracking errors, static noise, chromatic aberration, distorted imagery, and cryptic messaging to create psychological unease, nostalgia twisted into dread, and a haunting sense that something is deeply wrong with the signal.
---

### Style Definition
Analog Horror mimics the imperfect, decaying quality of outdated analog technology to present horror as "found footage" or corrupted broadcasts. It transforms familiar retro media formats into vehicles for existential dread, body horror, or surreal unease, often leaving viewers with more questions than answers.

In 2026, this style remains powerful in experimental web design, horror-themed sites, and immersive storytelling experiences. It frequently overlaps with liminal spaces (empty, eerie transitional environments) and glitchbreak aesthetics, but emphasizes the physical degradation of analog signals rather than pure digital corruption.

**Core spirit:** **The broadcast is corrupted.** Turn nostalgic, everyday media into something wrong and invasive. The interface should feel like stumbling upon a forbidden VHS tape or a hijacked public access channel that slowly reveals something terrifying beneath the surface.

### Core Visual Characteristics (Must Strictly Follow)
- **Degraded Analog Quality**: Heavy film grain, VHS tracking lines, color bleed, static snow, and low-resolution artifacts to simulate old magnetic tape or CRT displays.
- **Distorted & Uncanny Imagery**: Warped faces, elongated or distorted figures, subtle body horror, and surreal elements that feel slightly "off" or corrupted.
- **Broadcast & PSA Style**: Fake emergency alerts, public service announcements, test patterns, timestamp overlays, and dated TV graphics with cryptic or fatalistic text.
- **Eerie Color Palettes**: Desaturated or overly saturated tones — deep blues, sickly greens, washed-out yellows, or harsh reds. Often paired with flickering or bleeding colors.
- **Liminal & Empty Spaces**: Empty hallways, abandoned rooms, or transitional environments that evoke isolation and the uncanny valley, frequently combined with analog degradation.
- **Unstable Elements**: Flickering, sudden jumps, hidden frames, or slowly corrupting text and images that build psychological tension.
- **Overall Atmosphere**: Unsettling, nostalgic yet terrifying, melancholic, claustrophobic, and psychologically invasive. The interface should feel haunted by the medium itself.

### Strictly Prohibited (To Keep Authentic Analog Horror Feel)
- Clean, high-resolution, or modern glossy effects that remove the degraded analog authenticity.
- Overly bright, playful, or dopamine-driven colors that contradict the dread and unease.
- Excessive jump scares or gore — analog horror thrives on slow-building psychological tension and implication rather than explicit violence.
- Poor performance from unoptimized heavy effects; the degradation should feel intentional, not sloppy.
- Random glitches without narrative or atmospheric purpose — every distortion must heighten the sense of corrupted reality.
- Ignoring accessibility: provide reduced-motion options, maintain readable contrast for critical text, and avoid seizure-inducing strobing.
- Turning it into pure fun retro nostalgia without the underlying horror or unease.

### Recommended Modern Implementation (To Simulate Authentic Analog Horror)
- **CSS Techniques**: Use SVG filters or multiple layered backgrounds for VHS grain and static. Create tracking errors with animated repeating linear gradients. Apply `filter: contrast()`, `brightness()`, and `hue-rotate()` for color bleed and degradation.
- **Distortion Effects**: RGB split via pseudo-elements with `clip-path` and offset animations. Add scan lines, flicker, and static noise with keyframes and `mix-blend-mode`.
- **Liminal Touches**: Combine with empty, dimly lit backgrounds or low-fi textures. Use monospace or dated fonts for broadcast-style text.
- **Performance Optimization**: Prefer CSS/SVG for effects over heavy video. Compress any grain overlays. Lazy-load non-critical assets and provide a "clean signal" fallback when `prefers-reduced-motion` is enabled.
- **Hybrid Approach**: Use analog degradation on hero sections or key visuals, with clearer content areas for usability. Add subtle timestamp or "REC" overlays for authenticity.
- **Accessibility First**: Ensure sufficient contrast for essential text. Support keyboard navigation and screen readers. Warn users about potential flashing or disturbing content. Test thoroughly for cognitive and sensory impact.
- **Tools**: CSS keyframes and filters for core VHS effects, Canvas/WebGL for advanced distortion if needed, GSAP for controlled corruption animations, and inspiration from series like *Local 58*, *The Mandela Catalogue*, or *Skinamarink*.

### Example Code Snippet (Analog Horror Distorted Broadcast Card)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Analog Horror Example</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: #0a0a1f;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: monospace;
      color: #ffdddd;
      overflow: hidden;
      position: relative;
    }

    .analog-screen {
      width: 520px;
      background: #1a1a2e;
      border: 12px solid #333;
      box-shadow: 0 0 40px rgba(0,0,0,0.9);
      padding: 32px;
      position: relative;
      overflow: hidden;
    }

    /* VHS grain + static */
    .analog-screen::before {
      content: "";
      position: absolute;
      inset: 0;
      background: 
        radial-gradient(circle, rgba(255,255,255,0.04) 1px, transparent 1px),
        repeating-linear-gradient(transparent 0px, transparent 3px, rgba(255,255,255,0.06) 3px, rgba(255,255,255,0.06) 6px);
      background-size: 4px 4px, 100% 6px;
      animation: vhs-static 0.6s steps(4) infinite;
      pointer-events: none;
      opacity: 0.75;
      mix-blend-mode: overlay;
    }

    h1 {
      font-size: 2.4rem;
      text-transform: uppercase;
      letter-spacing: 4px;
      color: #ff6666;
      text-shadow: 0 0 8px #ff0000;
      margin: 0 0 20px 0;
      animation: signal-distort 1.8s infinite linear alternate-reverse;
    }

    p {
      line-height: 1.45;
      opacity: 0.85;
    }

    .timestamp {
      position: absolute;
      top: 16px;
      right: 20px;
      font-size: 0.9rem;
      color: #88ff88;
    }

    @keyframes vhs-static {
      0% { background-position: 0 0; }
      100% { background-position: 0 40px; }
    }

    @keyframes signal-distort {
      0% { transform: translate(0, 0) skew(0deg); }
      30% { transform: translate(-2px, 1px) skew(2deg); }
      70% { transform: translate(3px, -2px) skew(-3deg); }
    }
  </style>
</head>
<body>
  <div class="analog-screen">
    <div class="timestamp">REC 03:14 • 1997</div>
    <h1>THIS IS A TEST</h1>
    <p>DO NOT ATTEMPT TO ADJUST YOUR SET.<br>
    THE SIGNAL IS NOT WHAT IT SEEMS.</p>
  </div>
</body>
</html>