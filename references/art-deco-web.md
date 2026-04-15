---
style_name: Art Deco Web
aliases: Art Deco Design, Neo Deco Web, Geometric Deco Aesthetic, 1920s-1930s Web Revival, Luxe Geometric UI
description: A glamorous, geometric, and luxurious web design style inspired by the 1920s–1930s Art Deco movement. It features bold symmetry, sharp lines, sunbursts, chevrons, zigzags, metallic accents (especially gold and chrome), rich jewel tones, and streamlined elegance to create sophisticated, high-impact, and timeless digital experiences.
---

### Style Definition
Art Deco Web adapts the iconic Art Deco architectural and decorative style — born from the 1925 Paris Exposition — to modern digital interfaces. It combines modernist geometry with luxurious ornamentation, celebrating progress, glamour, and machine-age optimism while maintaining refined elegance.

In 2026, Art Deco (often called Neo Deco) is experiencing a strong revival as a counter to minimalism and brutalism. It appears in luxury fashion sites, hospitality brands, creative agencies, and high-end portfolios seeking to convey sophistication, heritage, and bold visual drama.

**Core spirit:** **Glamorous geometry meets digital luxury.** Use symmetry, sharp lines, and metallic finishes to make interfaces feel like stepping into a 1930s skyscraper lobby or a Jazz Age gala — elegant, bold, and unforgettable.

### Core Visual Characteristics (Must Strictly Follow)
- **Bold Geometric Patterns**: Sunbursts, chevrons, zigzags, stepped ziggurat forms, fan motifs, and repeating symmetrical shapes.
- **Symmetry & Streamlined Forms**: Balanced compositions, clean straight lines with occasional elegant curves, and strong vertical/horizontal emphasis.
- **Luxurious Metallic Accents**: Gold, chrome, silver, and brass effects achieved through gradients, glows, and reflective highlights.
- **Rich Color Palettes**: Deep jewel tones (emerald, sapphire, burgundy, black) contrasted with gold, cream, or vibrant accents. High contrast with black outlines.
- **Elegant Typography**: Bold, geometric sans-serifs or stylized serif fonts with strong contrast in stroke weight. Heavy tracking, uppercase headlines, and art deco-inspired letterforms.
- **Layered & Ornamental Details**: Subtle borders, frames, and decorative lines that enhance without overwhelming content.
- **Overall Atmosphere**: Glamorous, sophisticated, bold yet refined, timeless, and luxurious. The interface should feel opulent and celebratory.

### Strictly Prohibited (To Keep Authentic Art Deco Web Feel)
- Soft organic curves, florals, or Art Nouveau-style fluidity that contradict the geometric precision.
- Muted or overly minimalist palettes without metallic shine or jewel-tone contrast.
- Asymmetrical chaos or heavy randomness that breaks the symmetrical elegance.
- Poor contrast or illegible text over busy patterns.
- Excessive modern effects (heavy glassmorphism, brutalist rawness) that dilute the 1920s–1930s glamour.
- Ignoring performance or accessibility — decorative elements must not harm loading speed or readability.
- Using the style purely as decoration; geometric motifs must support hierarchy and brand storytelling.

### Recommended Modern Implementation (To Simulate Authentic Art Deco Web)
- **CSS Core**: Use CSS Grid with symmetrical columns. Create geometric patterns via repeating-linear-gradient or SVG backgrounds. Apply metallic effects with multi-layer `text-shadow` and `box-shadow` in gold/chrome tones.
- **Patterns & Motifs**: Implement sunbursts or chevrons with SVG or CSS clip-path. Add subtle borders and frames using pseudo-elements.
- **Typography**: Choose bold geometric fonts (e.g., with strong vertical emphasis). Use generous letter-spacing and uppercase for headlines. Apply gold gradients via `background-clip: text`.
- **Depth & Glow**: Add soft cinematic shadows and gentle hover glows. Use radial gradients for spotlight-like highlights.
- **Performance Optimization**: Prefer vector SVG for patterns and icons. Compress high-quality images. Lazy-load decorative elements and respect `prefers-reduced-motion`.
- **Accessibility First**: Ensure strong contrast ratios (especially gold on black). Use semantic HTML and clear focus states. Test with screen readers and keyboard navigation.
- **Tools**: Figma for mood boards and geometric layouts, CSS/SVG for implementation, GSAP for elegant micro-animations, and inspiration from Chrysler Building details or classic Art Deco posters.

### Example Code Snippet (Art Deco Web Hero Section)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Art Deco Web Example</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: #1a0f08; /* deep luxe brown-black */
      color: #f5e8c7;
      font-family: system-ui, sans-serif;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      position: relative;
    }

    .artdeco-hero {
      text-align: center;
      padding: 60px 80px;
      border: 4px solid #d4af37; /* gold border */
      background: rgba(26, 15, 8, 0.85);
      box-shadow: 
        0 0 40px rgba(212, 175, 55, 0.4),
        inset 0 0 30px rgba(255,255,255,0.1);
      position: relative;
    }

    h1 {
      font-size: 4.8rem;
      font-weight: 700;
      letter-spacing: 12px;
      text-transform: uppercase;
      color: #d4af37;
      text-shadow: 
        0 0 10px #d4af37,
        4px 4px 0 #1a0f08;
      margin: 0 0 24px 0;
    }

    .subtitle {
      font-size: 1.6rem;
      letter-spacing: 6px;
      opacity: 0.9;
      margin: 0;
    }

    /* Subtle sunburst decorative lines */
    .artdeco-hero::before {
      content: "";
      position: absolute;
      inset: -20px;
      border: 2px solid rgba(212, 175, 55, 0.3);
      clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
      pointer-events: none;
    }
  </style>
</head>
<body>
  <div class="artdeco-hero">
    <h1>ÉLÉGANCE</h1>
    <p class="subtitle">1925 • TIMELESS • LUXE</p>
  </div>
</body>
</html>