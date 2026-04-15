---
style_name: Neo Glassmorphism
aliases: Neo-Glassmorphism, Liquid Glass, Advanced Glassmorphism, Dynamic Glass UI, Fluid Glass Aesthetic
description: An evolved, more dynamic and expressive evolution of classic Glassmorphism. Neo Glassmorphism (also called Liquid Glass) features higher fluidity, real-time light refraction, adaptive translucency, dynamic specular highlights, and more organic, responsive behavior. It creates a premium, almost physical "liquid glass" material that reacts to content, movement, and interaction while maintaining excellent readability and depth.
---

### Style Definition
Neo Glassmorphism (often referred to as Liquid Glass, especially after Apple's 2025 introduction) takes traditional Glassmorphism further by adding fluidity, motion responsiveness, and more advanced optical qualities. While classic Glassmorphism relies on static backdrop blur and semi-transparency, Neo/Liquid Glass behaves like a living digital material — refracting light, adapting color based on surroundings, showing dynamic specular highlights, and subtly transforming with user interaction or content. It creates a more immersive, premium, and "alive" layered effect while remaining elegant and functional.

Core spirit: **Fluid, responsive, and optically rich glass.** Elements feel like real liquid glass that dynamically interacts with light, content, and user input, adding vitality and depth without sacrificing clarity.

### Core Visual Characteristics (Must Strictly Follow)
- **Advanced Translucency & Adaptive Opacity**: Variable semi-transparency (typically 10–30% base) that intelligently adapts to background content and lighting conditions.
- **Dynamic Backdrop Blur + Refraction**: Strong backdrop blur combined with light refraction and lensing effects. The blur is not static — it can subtly shift with movement or context.
- **Specular Highlights & Dynamic Shine**: Realistic, moving specular highlights and reflections that react to user gestures, scroll, or content changes, giving a "wet" or liquid quality.
- **Fluid & Organic Shapes**: Softer, more rounded or slightly irregular borders and forms compared to rigid classic glassmorphism. Elements can feel more "liquid" or responsive.
- **Layered Depth with Motion**: Multiple translucent layers with subtle parallax or responsive movement. Depth is expressed through adaptive blur, highlights, and color bleeding from the background.
- **Vibrant yet Readable Backgrounds**: Best paired with colorful gradients, images, or dynamic backgrounds so the glass "reacts" beautifully while maintaining high text/icon readability.
- **Subtle Borders & Edges**: Thin, luminous or adaptive borders that enhance the glass illusion without overpowering the effect.

- **Overall Atmosphere**: Elegant, dynamic, premium, immersive, and alive. The interface feels like high-quality physical glass or liquid material — sophisticated, responsive, and full of subtle vitality.

### Strictly Prohibited (To Keep Authentic Neo Glassmorphism Feel)
- Static, low-quality blur without dynamic highlights or refraction (falls back to basic Glassmorphism).
- Heavy opacity that blocks the background completely or makes panels look solid.
- Harsh, thick borders or excessive shadows that destroy the delicate, liquid quality.
- Poor contrast or low readability on translucent layers (especially important for accessibility).
- Overuse on every element, which can cause visual fatigue or performance issues.
- Combining with heavy skeuomorphism or chaotic effects that clash with the refined glass material.

### Recommended Modern Implementation (To Simulate Authentic Neo Glassmorphism)
- Base: `background: rgba(255,255,255,0.1–0.25)` (adjust for dark/light mode).
- Core effect: `backdrop-filter: blur(16px–24px)` + `-webkit-backdrop-filter`.
- Add dynamic shine: Use pseudo-elements with moving gradients or CSS animations for specular highlights.
- For more "liquid" feel: Combine with slight `transform` on hover/scroll or adaptive color based on background.
- Ensure performance: Use sparingly on critical elements; test on real devices (backdrop-filter can be expensive).
- Accessibility: Maintain high contrast ratios; provide fallback for browsers that don't support advanced filters.

### Example Code Snippet (Neo / Liquid Glass Card)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Neo Glassmorphism Example</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: system-ui, sans-serif;
      color: white;
    }
    .neo-glass {
      background: rgba(255, 255, 255, 0.12);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border-radius: 24px;
      border: 1px solid rgba(255, 255, 255, 0.25);
      box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37);
      padding: 48px 56px;
      width: 380px;
      text-align: center;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }
    .neo-glass:hover {
      transform: translateY(-4px) scale(1.02);
      box-shadow: 0 20px 50px rgba(31, 38, 135, 0.5);
    }
    h1 {
      font-size: 32px;
      margin-bottom: 12px;
    }
  </style>
</head>
<body>
  <div class="neo-glass">
    <h1>Neo Glassmorphism</h1>
    <p>Liquid, responsive, and full of light. The glass reacts — just like reality.</p>
  </div>
</body>
</html>