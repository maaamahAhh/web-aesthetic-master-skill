---
style_name: Synthwave
aliases: Synthwave Aesthetic, Outrun, Retrowave, Retro Wave, Neon Outrun, 80s Synthwave UI
description: A vibrant, nostalgic retro-futuristic design style inspired by 1980s synth music, Outrun video games, and sci-fi films. It features dark backgrounds, intense neon colors (cyan, magenta, pink, purple), glowing grids, perspective horizons, chrome typography, sunsets, and subtle glitch or scan-line effects to evoke a dreamy, high-speed night drive through a neon-lit retro future.
---

### Style Definition
Synthwave (also known as Outrun or Retrowave) draws heavily from 1980s electronic music aesthetics, arcade games like *Out Run*, and films such as *Blade Runner* and *Tron*. It romanticizes a stylized vision of the 80s future — endless highways at dusk, chrome sports cars, and glowing cityscapes — blending nostalgia with optimistic retro-futurism.

In 2026, Synthwave continues as a popular nostalgic trend, often blended with cyberpunk, vaporwave, or Y2K elements. It is ideal for music platforms, gaming sites, fashion brands, creative portfolios, and any experience aiming to deliver high-energy, atmospheric, and emotionally evocative visuals.

**Core spirit:** **Drive into the neon night.** Create immersive, high-octane digital experiences that feel like cruising through a synth-drenched 1986 sunset — bold, glowing, and unapologetically retro-futuristic.

### Core Visual Characteristics (Must Strictly Follow)
- **Signature Neon Palette**: Electric cyan (#00f3ff), hot magenta/pink (#ff00aa), deep purple, and vibrant teal against near-black or dark navy backgrounds. Strong contrast with glowing accents.
- **Perspective Grids & Horizons**: Classic receding checkerboard or wireframe grids fading into a sunset or horizon line, creating depth and speed.
- **Glowing & Chrome Elements**: Strong neon glows via layered shadows, chrome/metallic typography, reflective highlights, and holographic effects.
- **Retro-Futuristic Typography**: Bold, condensed sans-serifs with heavy tracking, uppercase styling, and occasional chrome or outlined effects. Fonts often evoke 80s arcade or sci-fi posters.
- **Atmospheric Details**: Subtle scan lines, light VHS distortion, palm trees or sports car silhouettes (optional), sunset gradients, and geometric shapes with motion blur or light trails.
- **Dynamic Energy**: Elements that feel fast and alive — glowing lines, subtle animations, and high-contrast compositions.
- **Overall Atmosphere**: Energetic, nostalgic, dreamy, cinematic, and exhilarating. The interface should feel like the soundtrack to a high-speed night drive — pulsing with neon and retro cool.

### Strictly Prohibited (To Keep Authentic Synthwave Feel)
- Bright, clean pastel or modern minimalist palettes that remove the dark neon contrast.
- Heavy dystopian glitch or surveillance elements that shift it too far into cyberpunk territory.
- Overly soft blurs, glassmorphism, or organic textures that dilute the sharp retro-digital edge.
- Poor contrast or illegible text over busy neon backgrounds.
- Excessive constant animations causing performance issues or motion sickness.
- Random 80s elements without cohesive neon grid, glow, and horizon composition.
- Ignoring accessibility — neon effects must support readable text and reduced-motion options.

### Recommended Modern Implementation (To Simulate Authentic Synthwave Design)
- **CSS Core**: Dark background with neon gradients. Create glowing text/buttons using multiple `text-shadow` and `box-shadow` layers (e.g., `0 0 10px #00f3ff, 0 0 30px #ff00aa`). Build perspective grids with CSS transforms (`perspective` + `rotateX`) or repeating linear gradients.
- **Horizon & Depth**: Use layered backgrounds with sunset gradients and receding grid lines. Add light motion blur or trailing effects with CSS animations.
- **Typography & Glow**: Condensed futuristic fonts with heavy `letter-spacing`. Apply chrome effects via gradient text (`background-clip: text`) and strong outer glows.
- **Subtle Effects**: Light scan lines via repeating gradients and keyframes. Optional soft chromatic aberration or flicker for retro feel.
- **Performance Optimization**: Rely on CSS for glows and grids. Use optimized images for backgrounds. Lazy-load decorative assets and provide `prefers-reduced-motion` fallbacks that disable intense animations.
- **Accessibility First**: Ensure sufficient contrast for body text. Support keyboard navigation and screen readers. Offer a toned-down "stable mode" for sensitive users.
- **Tools**: Pure CSS + keyframes for most effects, GSAP/ScrollTrigger for dynamic reveals, SVG for precise grids, and inspiration from classic Outrun album art or 80s game covers.

### Example Code Snippet (Synthwave Neon Grid Hero)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Synthwave Example</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(to bottom, #1a0033, #000022);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Orbitron', system-ui, sans-serif;
      overflow: hidden;
      position: relative;
      color: #ffffff;
    }

    /* Perspective grid */
    body::before {
      content: "";
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 70%;
      background: 
        linear-gradient(rgba(0, 255, 255, 0.12) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0, 255, 255, 0.12) 1px, transparent 1px);
      background-size: 80px 80px;
      transform: perspective(900px) rotateX(72deg);
      opacity: 0.75;
      pointer-events: none;
    }

    .synth-hero {
      text-align: center;
      z-index: 2;
      position: relative;
    }

    h1 {
      font-size: 5.5rem;
      font-weight: 900;
      letter-spacing: 12px;
      text-transform: uppercase;
      margin: 0 0 20px 0;
      text-shadow: 
        0 0 15px #00f3ff,
        0 0 30px #00f3ff,
        0 0 50px #ff00aa;
      animation: neon-flicker 4s infinite alternate;
    }

    .subtitle {
      font-size: 1.8rem;
      color: #ff99ff;
      letter-spacing: 8px;
      text-shadow: 0 0 20px #ff00aa;
    }

    @keyframes neon-flicker {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.95; }
    }
  </style>
</head>
<body>
  <div class="synth-hero">
    <h1>OUTRUN</h1>
    <p class="subtitle">NEVER STOP DRIVING • 1986 FOREVER</p>
  </div>
</body>
</html>