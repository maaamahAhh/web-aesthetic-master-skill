---
style_name: Cyberpunk
aliases: Cyberpunk Aesthetic, Neon Futurism, Cyberpunk UI, Neon Dystopia Design, High-Tech Low-Life Aesthetic, Blade Runner Style, Night City UI
description: A dark, immersive, and high-contrast design style inspired by cyberpunk fiction. It features deep black backgrounds, vibrant neon glows (cyan, magenta, electric pink, acid green), glitch effects, scan lines, holographic elements, and gritty futuristic details to evoke a dystopian high-tech world of rain-slicked streets, megacities, and digital rebellion.
---

### Style Definition
Cyberpunk design draws from classic sci-fi works like *Blade Runner*, *Neuromancer*, and *Cyberpunk 2077*. It contrasts advanced technology with urban decay — sleek neon against gritty darkness — creating a tense, atmospheric, and rebellious visual language.

In 2026, Cyberpunk remains a dominant edgy trend, often blended with glitch art, surveillance, or retro-futurism. It is widely used in creative portfolios, gaming sites, music/fashion campaigns, tech product showcases, and any project aiming to convey futuristic energy, digital rebellion, or dystopian commentary.

**Core spirit:** **High-tech, low-life.** Neon lights piercing eternal night. Technology feels both seductive and dangerous. The interface should feel alive with electric energy, digital corruption, and raw urban intensity.

### Core Visual Characteristics (Must Strictly Follow)
- **Dark Base with Neon Accents**: Near-black or deep charcoal backgrounds paired with intense neon colors — electric cyan (#00f3ff), hot magenta/pink (#ff0055), acid green (#39ff14), and violet.
- **Glowing & Holographic Effects**: Strong neon glows via multiple `text-shadow`/`box-shadow` layers, holographic transparency, and subtle reflections.
- **Digital Distortion**: Light glitch effects, RGB channel shifts, scan lines, static noise, and chromatic aberration for a corrupted signal feel.
- **Futuristic Typography**: Bold, condensed futuristic fonts (e.g., Orbitron, Rajdhani, or monospace like Share Tech Mono) with sharp angles, tracking, and occasional glitch animation.
- **Grid & HUD Elements**: Subtle cyber grids, data overlays, targeting reticles, status bars, or terminal-style readouts.
- **Atmospheric Details**: Rain/slick reflections (simulated), metallic/chrome textures, angled panels, and low-fi CRT or VHS-inspired artifacts.
- **High Contrast & Tension**: Extreme light/dark contrast to make neon "pop" while maintaining readability on key content.
- **Overall Atmosphere**: Dark, electric, gritty, rebellious, immersive, and dystopian. The interface should feel like walking through a rain-drenched neon megacity at night.

### Strictly Prohibited (To Keep Authentic Cyberpunk Feel)
- Bright, clean, or pastel palettes that remove the dark dystopian mood.
- Soft blurs, glassmorphism, or warm organic textures that soften the gritty high-tech edge.
- Overuse of heavy constant animations causing motion sickness or performance issues.
- Poor contrast — neon must enhance readability, not obscure it.
- Excessive low-fi degradation that makes content unreadable or the UI unusable.
- Ignoring accessibility — provide reduced-motion fallbacks and maintain WCAG contrast on critical text.
- Pure decoration without purpose; every glitch or glow should enhance the futuristic tension.

### Recommended Modern Implementation (To Simulate Authentic Cyberpunk Design)
- **CSS Core**: Dark background with repeating subtle grid patterns. Use multiple layered `text-shadow` and `box-shadow` for neon glow (e.g., `0 0 10px #00f3ff, 0 0 20px #00f3ff`). Create scan lines with repeating linear gradients and light animation.
- **Glitch Effects**: Multiple pseudo-elements with `clip-path` + keyframes for RGB split and jitter. Use `filter: brightness()` or `hue-rotate()` sparingly.
- **Advanced Techniques**: Three.js/WebGL for holographic 3D elements, rain effects, or post-processing (bloom, glitch pass). GSAP for triggered neon flickers or hover distortions.
- **Performance Optimization**: Prefer CSS for glows and scan lines. Compress any background assets. Limit WebGL to hero sections. Always include `prefers-reduced-motion` support that disables heavy animations.
- **Typography**: Combine futuristic sans (Orbitron) for headlines with monospace for data/HUD elements. Add subtle letter-spacing and uppercase usage.
- **Accessibility First**: Ensure neon text meets contrast ratios against dark backgrounds. Provide stable fallback styles. Support keyboard navigation and screen readers. Test for vestibular issues with motion.
- **Tools**: Pure CSS for most effects, GSAP/ScrollTrigger for interactions, Three.js for advanced scenes, and noise generators for static/grain.

### Example Code Snippet (Cyberpunk Neon Glitch Card)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Cyberpunk Example</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: #0a0a0a;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Orbitron', system-ui, sans-serif;
      overflow: hidden;
      position: relative;
    }

    /* Subtle cyber grid background */
    body::before {
      content: "";
      position: absolute;
      inset: 0;
      background-image: 
        linear-gradient(rgba(0, 243, 255, 0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0, 243, 255, 0.03) 1px, transparent 1px);
      background-size: 40px 40px;
      pointer-events: none;
    }

    .cyber-card {
      width: 380px;
      background: rgba(15, 15, 25, 0.95);
      border: 2px solid #00f3ff;
      box-shadow: 
        0 0 20px #00f3ff,
        0 0 40px rgba(255, 0, 85, 0.4),
        inset 0 0 20px rgba(0, 243, 255, 0.2);
      padding: 48px 36px;
      text-align: center;
      position: relative;
      overflow: hidden;
      clip-path: polygon(0 0, 100% 0, 100% 92%, 94% 100%, 0 100%);
    }

    .cyber-card::before {
      content: "";
      position: absolute;
      inset: 0;
      background: repeating-linear-gradient(
        to bottom,
        transparent 0px,
        transparent 3px,
        rgba(0, 243, 255, 0.06) 3px,
        rgba(0, 243, 255, 0.06) 6px
      );
      animation: scanline 8s linear infinite;
      pointer-events: none;
    }

    h1 {
      font-size: 2.8rem;
      color: #fff;
      margin: 0 0 12px 0;
      text-shadow: 
        0 0 10px #00f3ff,
        0 0 20px #00f3ff,
        0 0 40px #ff0055;
      letter-spacing: 4px;
      position: relative;
    }

    .glitch {
      position: relative;
    }

    .glitch::before,
    .glitch::after {
      content: attr(data-text);
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
    }

    .glitch::before {
      color: #ff0055;
      animation: glitch-1 2s infinite linear alternate-reverse;
      clip-path: polygon(0 0, 100% 0, 100% 35%, 0 35%);
      left: 2px;
    }

    .glitch::after {
      color: #00f3ff;
      animation: glitch-2 2.5s infinite linear alternate-reverse;
      clip-path: polygon(0 65%, 100% 65%, 100% 100%, 0 100%);
      left: -2px;
    }

    p {
      color: #a0f0ff;
      font-size: 1.1rem;
      opacity: 0.9;
      margin: 0;
    }

    @keyframes scanline {
      0% { transform: translateY(-100%); }
      100% { transform: translateY(300%); }
    }

    @keyframes glitch-1 {
      0% { transform: translate(0); }
      20% { transform: translate(-3px, 3px); }
      40% { transform: translate(3px, -3px); }
      100% { transform: translate(0); }
    }

    @keyframes glitch-2 {
      0% { transform: translate(0); }
      30% { transform: translate(4px, 2px); }
      60% { transform: translate(-2px, -4px); }
      100% { transform: translate(0); }
    }
  </style>
</head>
<body>
  <div class="cyber-card">
    <h1 class="glitch" data-text="NIGHT CITY">NIGHT CITY</h1>
    <p>NEON RUNS THROUGH OUR VEINS.<br>STAY ONLINE.</p>
  </div>
</body>
</html>