---
style_name: Surveillance
aliases: Surveillance Aesthetic, CCTV Dystopia, Surveillance UI, Dystopian Monitoring Design, Security Camera Aesthetic, Panopticon UI, Big Brother Aesthetic
description: A tense, dystopian design style that emulates constant surveillance through security camera feeds, tracking overlays, biometric HUD elements, monochrome or infrared palettes, glitch artifacts, scan lines, and digital warning interfaces. It evokes themes of observation, control, privacy erosion, and technological paranoia while delivering a raw, high-contrast, utilitarian visual language.
---

### Style Definition
Surveillance design draws directly from real-world CCTV systems, security monitoring rooms, and dystopian sci-fi (1984, Black Mirror, cyberpunk). It transforms the anxiety of being watched into a deliberate aesthetic using functional UI elements like targeting reticles, timestamped feeds, recognition boxes, and data overlays.

In 2026, this style has evolved from niche commentary on privacy into a mainstream edgy trend, especially among Gen-Z creators and brands exploring digital tension, AI oversight, and data control. It pairs well with glitch art, cyberpunk, or raw brutalism but focuses on the cold, mechanical feel of constant monitoring. Ideal for experimental portfolios, privacy-focused tech, music/fashion campaigns, or any project aiming to provoke thought about visibility and control.

**Core spirit:** **You are being watched.** Use the language of security systems — cold precision, digital corruption, and oppressive functionality — to create immersive tension and cultural commentary without sacrificing core readability where needed.

### Core Visual Characteristics (Must Strictly Follow)
- **CCTV / Security Feed Look**: Grainy or low-resolution textures, desaturated or infrared color palettes (green night-vision, red alerts, monochrome), subtle static and noise.
- **Tracking & Targeting Overlays**: Thin outline boxes (recognition frames), crosshairs, scanning lines, and bounding rectangles that highlight elements as if being tracked.
- **System Typography & Data Readouts**: Monospace or terminal-style fonts, timestamps, coordinates, status logs ("SUBJECT DETECTED", "SIGNAL LOCKED"), and HUD-style text.
- **Digital Distortion & Glitch**: Light RGB shifts, scan lines, horizontal jitter, pixelation, or momentary corruption effects to simulate unstable feeds.
- **High-Contrast Warning Elements**: Red accents for alerts, flashing indicators, caution stripes, or "REC" overlays. Cold blues/grays for base interface.
- **Exposed Structure**: Grid-based layouts resembling multi-camera monitors, visible scan lines, and mechanical borders.
- **Selective Application**: Apply surveillance effects primarily to hero sections, images, or interactive elements — maintain hierarchy so critical content remains legible.
- **Overall Atmosphere**: Tense, oppressive, paranoid, mechanical, futuristic yet retro, and unsettlingly functional. The interface feels like a live security control room.

### Strictly Prohibited (To Keep Authentic Surveillance Feel)
- Soft gradients, glassmorphism, or warm organic textures that soften the cold mechanical feel.
- Overly vibrant or playful colors that reduce the dystopian tension.
- Excessive constant animations causing motion sickness or performance issues.
- Poor contrast that makes text unreadable over noisy/glitchy backgrounds.
- Random glitches without purpose — effects must feel like realistic signal interference or monitoring tools.
- Ignoring usability: the "watched" feeling should enhance the message, not make navigation impossible.
- Heavy, unoptimized assets that break the low-fi CCTV illusion.

### Recommended Modern Implementation (To Simulate Authentic Surveillance Design)
- **CSS Core**: Use `filter: contrast(1.2) brightness(0.9)` or hue-rotate for night-vision/infrared looks. Add scan lines with repeating linear gradients or background patterns. Create tracking boxes with thin borders and subtle animations.
- **Glitch & Distortion**: Combine CSS keyframes for light jitter, RGB split via multiple pseudo-elements, or `mix-blend-mode` for static. Use `clip-path` for feed-like framing.
- **Advanced Options**: Integrate Three.js/WebGL post-processing (GlitchPass, ScanlineShader) for realistic corruption. Add subtle video-like grain with SVG noise or canvas.
- **Performance Optimization**: Keep effects lightweight with CSS where possible. Use compressed textures for grain. Respect `prefers-reduced-motion` with a "stable feed" fallback. Test on mobile for jank.
- **Typography**: Monospace fonts (e.g., 'Courier New', 'IBM Plex Mono', or system `monospace`). Uppercase labels, green/red text for status.
- **Accessibility First**: Ensure sufficient contrast for essential text (WCAG AA minimum). Provide reduced-motion mode. Use semantic HTML and ARIA for dynamic elements. Avoid making the entire UI disorienting.
- **Tools**: CSS animations + filters, GSAP for triggered glitches, Kittl or Figma for prototyping HUD elements.

### Example Code Snippet (Surveillance Dashboard with CCTV Feed Effect)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Surveillance Aesthetic Example</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: #0a0a0a;
      color: #00ff41; /* classic night-vision green */
      font-family: 'Courier New', monospace;
      overflow: hidden;
      position: relative;
    }

    .surveillance-container {
      width: 100%;
      height: 100%;
      background: 
        linear-gradient(transparent 50%, rgba(0, 255, 65, 0.03) 50%),
        #111;
      background-size: 100% 4px; /* scan lines */
      position: relative;
      border: 12px solid #222;
      box-shadow: inset 0 0 80px rgba(0, 0, 0, 0.9);
    }

    .feed {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 620px;
      height: 380px;
      background: #000;
      border: 4px solid #00ff41;
      box-shadow: 0 0 40px rgba(0, 255, 65, 0.4);
      overflow: hidden;
    }

    .feed::before {
      content: "";
      position: absolute;
      inset: 0;
      background: repeating-linear-gradient(
        to bottom,
        transparent 0px,
        transparent 2px,
        rgba(0, 255, 65, 0.08) 2px,
        rgba(0, 255, 65, 0.08) 4px
      );
      pointer-events: none;
      animation: scan 6s linear infinite;
    }

    @keyframes scan {
      0% { transform: translateY(-100%); }
      100% { transform: translateY(100%); }
    }

    .tracking-box {
      position: absolute;
      top: 80px;
      left: 120px;
      width: 180px;
      height: 220px;
      border: 2px solid #ff0044;
      box-shadow: 0 0 12px #ff0044;
      animation: tracking-jitter 0.8s infinite alternate;
    }

    @keyframes tracking-jitter {
      0% { transform: translate(0, 0); }
      100% { transform: translate(2px, -2px); }
    }

    .hud-text {
      position: absolute;
      bottom: 20px;
      left: 20px;
      font-size: 1.1rem;
      text-transform: uppercase;
      letter-spacing: 2px;
    }

    .status {
      position: absolute;
      top: 20px;
      right: 20px;
      color: #ff0044;
      font-size: 1rem;
      animation: pulse 1.5s infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.4; }
    }

    h1 {
      position: absolute;
      top: 30px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 2.8rem;
      color: #ff0044;
      text-shadow: 0 0 10px #ff0044;
      letter-spacing: 6px;
      text-transform: uppercase;
    }
  </style>
</head>
<body>
  <div class="surveillance-container">
    <h1>SURVEILLANCE ACTIVE</h1>
    
    <div class="feed">
      <!-- Simulated feed content -->
      <div class="tracking-box"></div>
    </div>

    <div class="hud-text">
      SUBJECT ACQUIRED • 2026-04-15 19:42:13<br>
      LOCATION: UNKNOWN • SIGNAL STRENGTH: 87%
    </div>

    <div class="status">REC • LIVE FEED</div>
  </div>
</body>
</html>