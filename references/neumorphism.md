---
style_name: Neumorphism
aliases: Neumorphism, Soft UI, Soft Neumorphic Design, Extruded Soft UI, New Skeuomorphism
description: A soft, tactile UI design style that creates the illusion of extruded or inset 3D-like elements using subtle inner and outer shadows on a matching background color. It blends minimalism with gentle depth, giving buttons, cards, and controls a soft, embossed, or pressed-in appearance while maintaining a clean and calm aesthetic.
---

### Style Definition
Neumorphism (a blend of “new” and “skeuomorphism”) emerged around 2019–2020 as a middle ground between strict flat design and heavy skeuomorphism. It uses the same base color for the element and its parent background, then creates depth solely through carefully balanced light and dark shadows. This produces a soft, extruded (raised) or inset (pressed) effect that feels tactile and premium without realistic textures or heavy 3D rendering. It is often called “Soft UI” because of its gentle, approachable look and is best suited for light-mode interfaces with muted palettes.

Core spirit: **Soft tactile depth through shadow and light.** Elements appear gently extruded from or pressed into the surface, combining the cleanliness of minimalism with subtle physicality.

### Core Visual Characteristics (Must Strictly Follow)
- **Monochromatic / Matching Background**: The element’s background color is nearly identical to its parent container. Depth comes purely from shadows, not color contrast.
- **Dual Shadow Technique**:
  - Light shadow (usually top-left) to simulate highlight.
  - Dark shadow (usually bottom-right) to simulate depth/shadow.
  - For raised/extruded look: outer shadows.
  - For pressed/inset look: inset shadows.
- **Soft Rounded Corners**: Generous but soft border-radius (typically 12–24px) to enhance the gentle, pill-like feel.
- **Subtle Highlights**: Very light, almost white highlight on the raised edge to mimic light reflection.
- **Restrained Color Palette**: Soft pastels, warm grays, off-whites, or muted tones. Avoid high saturation or bright accents that break the soft effect.
- **Minimal Decoration**: Clean surfaces with very little additional ornamentation. Focus remains on the soft extruded depth.

- **Overall Atmosphere**: Soft, calm, tactile, friendly, and premium. Elements feel gently touchable, like high-quality soft material or embossed surfaces.

### Strictly Prohibited (To Keep Authentic Neumorphism Feel)
- Strong color contrast between element and background (destroys the seamless extruded illusion).
- Heavy or harsh shadows (makes it look like regular drop-shadow design).
- Sharp edges or minimal border-radius.
- Bright, neon, or highly saturated colors.
- Heavy textures, gradients, or additional skeuomorphic details.
- Overuse on every element — neumorphism works best selectively for key interactive components (buttons, cards, toggles).

### Recommended Modern Implementation (To Simulate Authentic Neumorphism)
- Use the same background color for the element and its container.
- Create the effect with two opposing shadows:
  - Light shadow: `box-shadow: 8px 8px 16px #d1d1d1;` (light mode raised)
  - Dark inset shadow: `box-shadow: inset 8px 8px 16px #bebebe;` (pressed)
- For dark mode: Invert shadow colors using darker grays.
- Apply generous but soft border-radius.
- Ensure accessibility: Add sufficient contrast for text and focus states (neumorphism’s low contrast is a known weakness — compensate with careful typography and focus indicators).

### Example Code Snippet (Classic Neumorphism Button & Card)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Neumorphism Example</title>
  <style>
    body {
      background: #e0e0e0;
      font-family: system-ui, sans-serif;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      margin: 0;
    }
    .neumorph-card {
      background: #e0e0e0;
      border-radius: 24px;
      padding: 40px;
      width: 320px;
      box-shadow: 
        12px 12px 24px #bebebe,
        -12px -12px 24px #ffffff;
    }
    button {
      background: #e0e0e0;
      border: none;
      padding: 16px 40px;
      border-radius: 50px;
      font-size: 17px;
      font-weight: 600;
      cursor: pointer;
      box-shadow: 
        6px 6px 12px #bebebe,
        -6px -6px 12px #ffffff;
      transition: all 0.2s ease;
    }
    button:active {
      box-shadow: 
        inset 4px 4px 8px #bebebe,
        inset -4px -4px 8px #ffffff;
    }
  </style>
</head>
<body>
  <div class="neumorph-card">
    <h2 style="margin-bottom:24px; text-align:center;">Neumorphism</h2>
    <button>Press Me — I Feel Soft</button>
  </div>
</body>
</html>