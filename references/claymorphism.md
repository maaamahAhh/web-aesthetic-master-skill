---
style_name: Claymorphism
aliases: Claymorphism, Clay UI, Soft Clay 3D, Puffy Clay Aesthetic, Clay-Like Soft UI
description: A soft, tactile, and playful 3D-like UI design style that mimics the appearance of clay or soft plastic material. It creates a puffy, inflated, chunky depth using multiple layered shadows (outer shadow for separation + double inner shadows for volume), large rounded corners (often squircle-like), and vibrant or pastel colors, giving elements a friendly, touchable, and organic feel.
---

### Style Definition
Claymorphism is a UI trend that gives digital elements a soft, chunky, 3D clay-like appearance. It builds on Neumorphism but allows more vibrant colors and independent backgrounds because it uses a combination of outer shadow (for floating/separation) and dual inner shadows (for volume and softness). The style feels playful, friendly, and tangible — like physical clay or soft modeling material — making interfaces more approachable and emotionally engaging. It gained popularity around 2021–2022 and remains a favorite for adding warmth and depth to modern designs.

Core spirit: **Soft, puffy, and touchable 3D without heavy realism.** Elements look inflated and organic, blending minimalism with gentle depth and playfulness.

### Core Visual Characteristics (Must Strictly Follow)
- **Large Rounded Corners / Squircle**: Very generous border-radius (often 30–50% or squircle smoothing) to create the soft, blob-like clay shape.
- **Multi-Layered Shadows**:
  - Outer shadow (usually darker, offset) for separation and floating effect.
  - Double inner shadows: one lighter (top-left) and one darker (bottom-right) to simulate volume and thickness.
- **Vibrant or Pastel Colors**: Bright, friendly, or soft pastel backgrounds (e.g., soft greens, yellows, pinks, blues). The clay effect works well with colorful bases.
- **Subtle Depth & Volume**: Elements appear "puffy" or inflated with soft 3D illusion. Avoid flat or overly sharp looks.
- **Clean & Friendly Typography**: Legible sans-serif fonts with good hierarchy. The soft clay elements make the overall interface feel warm and approachable.
- **Minimal Additional Effects**: Focus on the clay shadows and rounding. Avoid heavy gloss, neon, or complex textures that fight the soft clay material.

- **Overall Atmosphere**: Playful, friendly, warm, tactile, and approachable. The design feels soft, chunky, and inviting — like interacting with physical modeling clay or soft toys.

### Strictly Prohibited (To Keep Authentic Claymorphism Feel)
- Sharp edges or small border-radius (destroys the puffy clay look).
- Heavy gloss, metallic effects, or strong skeuomorphism that clashes with the soft clay material.
- Dark, muted, or low-saturation palettes that make shadows ineffective (claymorphism shines with brighter/pastel bases).
- Flat design without the characteristic multi-layered shadows.
- Overly complex or busy compositions that hide the clay effect.
- Poor accessibility — ensure sufficient contrast for text on clay-colored elements.

### Recommended Modern Implementation (To Simulate Authentic Claymorphism)
- Base color: Soft pastel or vibrant background for the element.
- Key effect: Multiple `box-shadow` declarations:
  - Outer shadow for floating.
  - Two inner shadows (lighter top-left + darker bottom-right) for volume.
- Large `border-radius` (or use squircle techniques for even softer shapes).
- Example CSS structure:
  ```css
  .clay {
    background: #ffeb3b; /* vibrant clay color */
    border-radius: 40px;
    box-shadow: 
      34px 34px 68px rgba(0,0,0,0.25),           /* outer shadow */
      inset -8px -8px 16px rgba(0,0,0,0.3),      /* dark inner */
      inset 8px 8px 16px rgba(255,255,255,0.8);  /* light inner */
  }
  ```
- Combine with subtle hover effects (e.g., slight scale or shadow change) for interactivity.

### Example Code Snippet (Classic Claymorphism Card)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Claymorphism Example</title>
  <style>
    body {
      background: #f0f0f0;
      font-family: system-ui, sans-serif;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      margin: 0;
    }
    .clay-card {
      background: #ffcc80;
      border-radius: 40px;
      padding: 40px 50px;
      width: 320px;
      text-align: center;
      box-shadow: 
        30px 30px 60px rgba(0,0,0,0.25),
        inset -10px -10px 20px rgba(0,0,0,0.3),
        inset 10px 10px 20px rgba(255,255,255,0.8);
      color: #333;
    }
    h1 {
      font-size: 28px;
      margin-bottom: 12px;
    }
  </style>
</head>
<body>
  <div class="clay-card">
    <h1>Claymorphism</h1>
    <p>Soft, puffy, and touchable — like real clay.</p>
  </div>
</body>
</html>