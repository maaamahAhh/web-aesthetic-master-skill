---
style_name: Glassmorphism
aliases: Glass Morphism, Frosted Glass UI, Translucent Glass Effect, Neo Glassmorphism (when more liquid/advanced)
description: A popular modern UI design style that mimics the appearance of frosted or translucent glass. It creates depth and visual hierarchy through semi-transparent panels with background blur, subtle borders, and soft lighting, allowing colorful or vibrant backgrounds to softly show through while maintaining readability and elegance.
---

### Style Definition
Glassmorphism is a visual design trend that simulates frosted glass panels layered over a background. It adds a sense of depth and sophistication without heavy 3D effects by combining transparency, backdrop blur, and delicate borders. Popularized by operating systems like macOS Big Sur / Windows 11 and widely used in 2025–2026 web and app design, it creates a light, airy, premium feel. It is often paired with vibrant backgrounds to make the "glass" effect stand out while keeping the interface modern and approachable.

Core spirit: **Frosted glass layered over vibrant depth.** Translucent elements float above the background, creating elegant separation and hierarchy with softness and light.

### Core Visual Characteristics (Must Strictly Follow)
- **Semi-Transparency**: Background with low opacity (typically rgba with 0.1–0.25 alpha) so the underlying content softly shows through.
- **Backdrop Blur**: The defining feature — `backdrop-filter: blur(10px–20px)` (or `-webkit-backdrop-filter`) to create the frosted glass effect by blurring what is behind the element.
- **Subtle Border**: Thin, semi-transparent white or light border (1px, opacity 0.1–0.3) to define the glass edge and enhance the glass-like quality.
- **Soft Shadows / Depth**: Very light drop shadow or inner glow for subtle elevation and realism (e.g., `box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37)`).
- **Rounded Corners**: Generous border-radius (12px–24px or higher) for a soft, modern card-like appearance.
- **Vibrant Backgrounds**: Best used over colorful, gradient, or image-rich backgrounds so the blur and transparency create beautiful diffusion.
- **High Readability**: Sufficient contrast for text and icons on the translucent panel. Often paired with dark or light text depending on the background.

- **Overall Atmosphere**: Elegant, modern, light, premium, and layered. Elements appear to float or hover with a sophisticated, almost magical frosted glass quality.

### Strictly Prohibited (To Keep Authentic Glassmorphism Feel)
- Heavy opacity (making it look like a solid card instead of glass).
- No or insufficient backdrop blur — the frosted effect is essential.
- Harsh, thick borders or heavy shadows that destroy the delicate glass illusion.
- Poor contrast or low readability on the translucent layer (especially accessibility issues).
- Overuse on every element, which can cause visual fatigue or performance problems.
- Combining with heavy skeuomorphism or strong 3D effects that clash with the soft translucent look.

### Recommended Modern Implementation (To Simulate Authentic Glassmorphism)
- Set a vibrant or gradient background on the parent/container.
- For the glass element: Use `background: rgba(255, 255, 255, 0.1–0.25)` (or dark variant for dark mode).
- Apply `backdrop-filter: blur(12px–20px)` and `-webkit-backdrop-filter` for compatibility.
- Add a subtle border: `border: 1px solid rgba(255, 255, 255, 0.2)`.
- Include a soft shadow for depth.
- Ensure text has good contrast; test on different backgrounds.
- For performance: Use sparingly on performance-critical pages and test on real devices.

### Example Code Snippet (Classic Glassmorphism Card)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Glassmorphism Example</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #667eea, #764ba2);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: system-ui, sans-serif;
    }
    .glass-card {
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border-radius: 20px;
      border: 1px solid rgba(255, 255, 255, 0.25);
      box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37);
      padding: 40px 50px;
      width: 360px;
      text-align: center;
      color: white;
    }
    h1 {
      font-size: 32px;
      margin-bottom: 16px;
    }
  </style>
</head>
<body>
  <div class="glass-card">
    <h1>Glassmorphism</h1>
    <p>Frosted elegance layered over vibrant depth.</p>
  </div>
</body>
</html>