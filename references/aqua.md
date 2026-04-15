---
style_name: Aqua
aliases: Apple Aqua, Mac OS X Aqua, Apple Glossy Style, Aqua Interface, Classic Mac OS X Design
description: The iconic glossy, liquid, translucent, and highly skeuomorphic design language introduced by Apple with Mac OS X (2001–2013). Characterized by vibrant colors, gel-like buttons, water-drop highlights, brushed metal, and a sense of depth and liquidity — it defined the optimistic, premium, and playful Apple aesthetic of the early 2000s.
---

### Style Definition
Aqua was Apple’s signature visual style for Mac OS X (Cheetah to Mavericks). It replaced the more utilitarian Platinum design of classic Mac OS with a bold, glossy, almost liquid appearance. The name “Aqua” refers to its water-like, translucent qualities. It heavily used skeuomorphism — making digital elements look like real physical materials — with generous use of gradients, reflections, and highlights to create a sense of premium quality and delight.

Core spirit: **Premium, playful, and liquid.** Digital interfaces should feel alive, glossy, and joyful, like high-quality physical objects made of glass, gel, and metal.

### Core Visual Characteristics (Must Strictly Follow)
- **Glossy & Liquid Effects**: Strong specular highlights, especially a bright white “water drop” or gel highlight at the top of buttons and elements.
- **Translucency & Glass**: Semi-transparent panels with subtle blur or frosted glass effects (early version of glassmorphism).
- **Vibrant Gradients**: Smooth, colorful gradients — often blue-to-cyan, green, or purple with bright white highlights.
- **Rounded Corners**: Very generous, pill-shaped or heavily rounded buttons, windows, and controls.
- **Brushed Metal**: Textured metallic surfaces (especially for toolbars and window frames) with subtle horizontal grain.
- **Color Palette**: Bright, optimistic, and saturated. Signature colors include:
  - Apple Blue (#007AFF and variants)
  - Gel green, cyan, purple, and vibrant accents
  - Clean white and light gray backgrounds
- **Typography:** Clean, friendly sans-serif (primarily Lucida Grande). Text often has subtle drop shadows to maintain legibility against translucent backgrounds.
- **Icons**: Highly detailed, colorful, and skeuomorphic — icons look like real objects with shine and dimension (Finder icon, Trash can, etc.).

- **Overall Atmosphere**: Playful, premium, optimistic, fresh, and delightful. The interface feels wet, glossy, and full of life — the visual embodiment of Apple’s “Think Different” era.

### Strictly Prohibited (To Keep Authentic Aqua Feel)
- Flat design or zero shadows (no iOS 7+ flat style).
- Harsh sharp edges or minimal rounded corners.
- Muted, dark, or low-saturation palettes.
- Heavy grunge, noise, or distressed textures.
- Modern heavy blur glassmorphism without the classic glossy gel highlight.
- Any element that feels cold, minimal, or overly serious.

### Recommended Modern Implementation (To Simulate Authentic Aqua)
- Use multiple layered gradients for the classic gel button effect (white highlight at top + color base).
- Add strong specular highlights using pseudo-elements or additional gradients.
- For brushed metal: Use subtle horizontal noise or gradient stripes.
- Buttons: Heavy `border-radius`, inner/outer shadows, and a bright top highlight.
- Backgrounds: Light gradients or subtle linen/paper textures with translucency.
- Icons: Use detailed PNGs or CSS to recreate 3D glossy icons.

### Example Code Snippet (Classic Aqua Glossy Button & Window)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Mac OS X Aqua Example</title>
  <style>
    body {
      background: linear-gradient(#e0f0ff, #c0d8ff);
      font-family: 'Helvetica', system-ui, sans-serif;
      padding: 60px;
    }
    .window {
      background: rgba(255,255,255,0.92);
      border: 1px solid rgba(100,180,255,0.6);
      border-radius: 12px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.25);
      max-width: 520px;
      margin: 0 auto;
      overflow: hidden;
    }
    .titlebar {
      background: linear-gradient(to right, #4a90ff, #007aff);
      color: white;
      padding: 10px 16px;
      font-weight: bold;
      text-align: center;
      border-bottom: 1px solid rgba(255,255,255,0.3);
    }
    button {
      background: linear-gradient(to bottom, #ffffff, #4ade80 30%, #22c55e);
      border: 2px solid #0066cc;
      border-radius: 9999px;
      padding: 12px 36px;
      font-size: 17px;
      font-weight: bold;
      color: #003366;
      box-shadow: 
        0 4px 0 #006633,
        inset 0 8px 12px rgba(255,255,255,0.9),
        inset 0 -4px 6px rgba(0,0,0,0.2);
      cursor: pointer;
      transition: all 0.15s;
    }
    button:active {
      transform: translateY(3px);
      box-shadow: 
        0 1px 0 #006633,
        inset 0 8px 12px rgba(255,255,255,0.7);
    }
  </style>
</head>
<body>
  <div class="window">
    <div class="titlebar">Mac OS X — Aqua Style</div>
    <div style="padding:40px; text-align:center;">
      <h1 style="color:#003366;">Hello, Beautiful.</h1>
      <button>Click Me — I’m Glossy!</button>
    </div>
  </div>
</body>
</html>