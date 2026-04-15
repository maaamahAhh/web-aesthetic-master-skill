---
style_name: Metro Design
aliases: Metro UI, Microsoft Metro Design, Modern UI, Windows 8 Style, Flat Metro Aesthetic, Tile-Based Design
description: The clean, bold, typographic, and grid-based design language introduced by Microsoft in 2010–2012 with Windows Phone 7 and Windows 8. It emphasizes content over chrome, large typography, flat colors, sharp edges, and live tiles — creating a modern, digital-first aesthetic that rejected skeuomorphism in favor of simplicity and clarity.
---

### Style Definition
Metro Design (also called Microsoft Design Language or Modern UI) was Microsoft’s response to the overly glossy and skeuomorphic trends of the 2000s. Inspired by Swiss typography, Bauhaus, and public signage systems (like the London Underground), it focuses on clarity, hierarchy, and content-first design. The signature element is the “Live Tile” — dynamic, rectangular blocks that display real-time information. The overall philosophy is “less is more” with bold, unapologetic typography and vibrant flat colors.

Core spirit: **Content is king.** Bold typography, generous whitespace, flat surfaces, and motion serve the information rather than decoration.

### Core Visual Characteristics (Must Strictly Follow)
- **Flat Design**: Completely flat surfaces with no bevels, gradients, shadows, or 3D effects. Pure 2D appearance.
- **Bold Typography**: Extremely large, bold sans-serif text (Segoe UI, Arial, or Helvetica). Typography carries most of the visual weight.
- **Color Palette**: Vibrant, high-contrast accent colors on dark or light backgrounds. Signature Microsoft colors: vivid blue (#0078D4), green, orange, purple, with neutral black/white/gray backgrounds. Each tile or section often has its own bold accent color.
- **Rectangular Tiles & Grid Layout**: Content organized in a strict grid of rectangular tiles (Live Tiles). Tiles can be different sizes (1x1, 2x1, 2x2, etc.).
- **Sharp Edges & Clean Lines**: No rounded corners (or very minimal). Everything has crisp 90-degree angles.
- **Minimal Ornamentation**: Very little decoration. No icons with heavy details — simple, geometric icons (often monochrome or single color).
- **Motion & Animation**: Subtle but purposeful animations — tiles flipping, content sliding in with ease, parallax effects, and smooth page transitions.

- **Overall Atmosphere**: Clean, modern, digital, bold, and efficient. The design feels fast, fresh, and focused on information delivery rather than visual flair.

### Strictly Prohibited (To Keep Authentic Metro Design Feel)
- Any 3D effects, bevels, emboss, gloss, or shadows (no skeuomorphism).
- Rounded corners on major elements (keep them sharp).
- Gradients (except very subtle ones for backgrounds).
- Ornate or detailed icons — keep them simple and geometric.
- Cluttered or chaotic layouts — maintain strong grid structure.
- Low-contrast or overly subtle typography.

### Recommended Modern Implementation (To Simulate Authentic Metro Design)
- Use a strict CSS Grid layout with rectangular tiles of varying sizes.
- Font: Segoe UI (or system sans-serif with bold weights).
- Background: Solid dark (#0F0F0F) or light (#F0F0F0) with vibrant accent tiles.
- Tiles: Use `border-radius: 0` or very small radius, solid background colors, and large text.
- Animations: CSS transitions for hover/tap states and entrance animations.
- Icons: Use simple SVG or Font Awesome with single color and minimal details.

### Example Code Snippet (Classic Metro Design Dashboard)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Metro Design Example</title>
  <style>
    body {
      margin: 0;
      background: #0F0F0F;
      color: #fff;
      font-family: 'Segoe UI', system-ui, sans-serif;
    }
    .header {
      background: #0078D4;
      padding: 20px 40px;
      font-size: 28px;
      font-weight: 600;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 12px;
      padding: 40px;
    }
    .tile {
      background: #1E90FF;
      color: white;
      padding: 20px;
      aspect-ratio: 1 / 1;
      display: flex;
      align-items: flex-end;
      font-size: 22px;
      font-weight: 600;
      transition: transform 0.2s;
    }
    .tile:hover {
      transform: scale(1.05);
    }
    .tile.large { aspect-ratio: 2 / 1; }
    .tile.accent { background: #FF8C00; }
  </style>
</head>
<body>
  <div class="header">Metro Dashboard</div>
  <div class="grid">
    <div class="tile">Mail</div>
    <div class="tile accent">Calendar</div>
    <div class="tile large">Weather<br><span style="font-size:48px;">23°</span></div>
    <div class="tile">Photos</div>
    <div class="tile">Music</div>
    <div class="tile">News</div>
  </div>
</body>
</html>