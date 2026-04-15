---
style_name: Dark Mode OLED
aliases: Deep Dark OLED, OLED Dark Aesthetic, Dark OLED Luxury, True Black Dark Mode, Deep Dark UI
description: The premium, immersive, and luxurious dark theme optimized for OLED/AMOLED displays. It features true or near-true black backgrounds (#000000 or #0A0A0A), subtle layered dark grays for depth, high-contrast light text, minimal visual noise, and a sophisticated, elegant atmosphere that maximizes battery efficiency while delivering a high-end, cinematic feel.
---

### Style Definition
Dark Mode OLED (also called Deep Dark or OLED Luxury) is a refined dark theme specifically optimized for OLED and AMOLED screens, where true black pixels turn completely off to save power. It goes beyond basic dark mode by creating rich depth through layered dark surfaces, excellent contrast, and restrained elegance. This style is popular in luxury brands, tech products, media apps, and high-end portfolios, evoking a sense of premium quality, mystery, and modernity.

Core spirit: **Luxury through darkness.** Use deep blacks for true depth and battery savings, layered grays for hierarchy, and minimal elements to create a calm, focused, cinematic experience.

### Core Visual Characteristics (Must Strictly Follow)
- **True / Near-True Black Backgrounds**: Primary background uses #000000 or very dark shades (#0A0A0A, #111111) to maximize OLED power savings and create infinite depth.
- **Layered Dark Surfaces**: Use multiple shades of dark gray (#1A1A1A, #212121, #2A2A2A) for cards, panels, and elevated surfaces to express hierarchy and depth without shadows.
- **High-Contrast Text**: Light text (#E0E0E0, #F5F5F5, or pure white for headings) with excellent readability. Avoid pure white for body text to reduce eye strain.
- **Minimal Visual Noise**: Extremely restrained design — few borders, subtle or no shadows, clean lines, and generous whitespace.
- **Accent Colors**: Desaturated or muted accents (soft cyan, deep purple, warm gold, or brand-specific tones) used sparingly for highlights. Avoid highly saturated neon colors.
- **Typography**: Clean, modern sans-serif fonts with excellent hierarchy. Large, confident headings and highly legible body text.
- **Imagery**: High-contrast or cinematic photography, often with dark tones that blend seamlessly into the background.

- **Overall Atmosphere**: Sophisticated, luxurious, immersive, calm, and premium. The design feels deep, elegant, and high-end — like a luxury watch or flagship smartphone interface.

### Strictly Prohibited (To Keep Authentic Dark OLED Feel)
- Light themes or bright backgrounds.
- Heavy gradients, gloss, or skeuomorphic effects (keep it flat or subtly layered).
- Excessive saturated colors or neon accents that cause visual vibration.
- Cluttered layouts or too many UI elements.
- Pure white backgrounds for any surface (except very small highlights).
- Harsh, unrefined contrasts that cause eye strain.

### Recommended Modern Implementation (To Simulate Authentic Dark OLED)
- Use true black (#000000) for the main background to maximize OLED battery savings.
- Define layered surfaces with CSS custom properties (e.g., --surface-1: #121212; --surface-2: #1F1F1F).
- Ensure WCAG contrast ratios (at least 4.5:1 for normal text, higher for headings).
- Add subtle elevation through lighter dark grays instead of heavy shadows.
- For images: Use dark-themed or high-contrast assets that integrate with the deep background.

### Example Code Snippet (Dark OLED Luxury Page)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Dark OLED Luxury Example</title>
  <style>
    :root {
      --bg: #000000;
      --surface: #121212;
      --surface2: #1F1F1F;
      --text: #E0E0E0;
      --accent: #00D4FF;
    }
    body {
      margin: 0;
      background: var(--bg);
      color: var(--text);
      font-family: 'Helvetica Neue', system-ui, sans-serif;
      min-height: 100vh;
    }
    .container {
      max-width: 980px;
      margin: 0 auto;
      padding: 120px 60px;
    }
    h1 {
      font-size: 68px;
      font-weight: 600;
      line-height: 1.1;
      letter-spacing: -2px;
      margin: 0 0 40px;
    }
    .card {
      background: var(--surface);
      padding: 40px;
      border-radius: 12px;
      margin-top: 60px;
    }
    button {
      background: var(--accent);
      color: #000;
      border: none;
      padding: 16px 48px;
      font-size: 17px;
      font-weight: 600;
      border-radius: 8px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Depth in Darkness</h1>
    <p style="font-size:22px; max-width:620px;">True black. Subtle layers. Pure focus.</p>
    
    <div class="card">
      <p style="font-size:19px;">Optimized for OLED. Designed for elegance.</p>
      <button>Experience the Depth</button>
    </div>
  </div>
</body>
</html>