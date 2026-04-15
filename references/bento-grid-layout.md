---
style_name: Bento Grid Layout
aliases: Bento Grid, Bento Box Layout, Bento UI, Modular Bento Grid, Compartmentalized Grid
description: A modern, modular grid-based layout style inspired by Japanese bento lunch boxes. It organizes content into visually distinct rectangular or square "compartments" (cards/blocks) of varying sizes within a structured grid, creating balanced, scannable, and aesthetically pleasing compositions that feel organized yet dynamic.
---

### Style Definition
Bento Grid Layout is a popular contemporary web design trend that divides the page into multiple self-contained content blocks (cards or tiles) of different sizes, arranged in a grid-like structure. Inspired by the compartmentalized Japanese bento box, each "compartment" holds a specific piece of content (text, image, video, stats, etc.). The varying block sizes create natural visual hierarchy and rhythm while maintaining overall balance and order. It is widely used in feature sections, dashboards, portfolios, and landing pages for its clean, modern, and highly scannable appearance.

Core spirit: **Organized variety within structure.** Different content types are neatly compartmentalized yet visually harmonious, making complex information easy to scan and engaging to view.

### Core Visual Characteristics (Must Strictly Follow)
- **Modular Grid Structure**: Content is arranged in a CSS Grid with varying column and row spans (e.g., 1x1, 2x1, 2x2, 1x2 blocks). Blocks align to an underlying grid but have different sizes for visual interest.
- **Varying Block Sizes**: Mix of small and large cards to create hierarchy — larger blocks for important content, smaller ones for supporting details.
- **Rounded Corners**: Soft, consistent border-radius on all blocks (typically 12–24px) to give a friendly, modern card-like feel.
- **Consistent Spacing (Gutters)**: Uniform gaps between blocks (usually 16–24px) for clean separation and breathing room.
- **Clean, Card-Based Design**: Each block is a self-contained unit with its own background, subtle elevation (light shadow or flat), and focused content (title + short description + visual).
- **Visual Balance**: Asymmetrical yet harmonious arrangement. The layout feels dynamic but not chaotic.
- **Color & Imagery**: Often paired with vibrant accents inside blocks or clean backgrounds. High-quality images or icons inside compartments.

- **Overall Atmosphere**: Modern, organized, scannable, balanced, and visually engaging. The design feels premium, structured, and delightful — like neatly arranged gourmet dishes in a bento box.

### Strictly Prohibited (To Keep Authentic Bento Grid Feel)
- Uniform same-sized cards (that becomes a regular grid, not bento).
- Chaotic or overlapping elements without grid alignment.
- Inconsistent spacing or gutters between blocks.
- Heavy shadows, gloss, or skeuomorphic effects on blocks (keep cards relatively flat or subtly elevated).
- Poor hierarchy — all blocks looking equally important.
- Cluttered content inside individual blocks.

### Recommended Modern Implementation (To Simulate Authentic Bento Grid)
- Use CSS Grid with `grid-template-columns` and `grid-auto-rows`.
- Span blocks using `col-span-*` and `row-span-*` (especially in Tailwind CSS).
- Maintain consistent gap (`gap-6` or `gap-8`).
- Make it responsive: Stack vertically on mobile while preserving the visual rhythm on larger screens.
- Add subtle hover effects or micro-interactions for polish.

### Example Code Snippet (Classic Bento Grid with Tailwind)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Bento Grid Example</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    .bento-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 24px;
    }
  </style>
</head>
<body class="bg-zinc-950 text-white p-8">
  <div class="max-w-6xl mx-auto">
    <h1 class="text-5xl font-bold mb-12 text-center">Bento Grid Layout</h1>
    
    <div class="bento-grid">
      <!-- Large block -->
      <div class="col-span-2 row-span-2 bg-zinc-900 rounded-3xl p-10 flex flex-col justify-end">
        <h2 class="text-4xl font-semibold">Main Feature</h2>
        <p class="mt-4 text-zinc-400">The hero content goes here with more space.</p>
      </div>
      
      <!-- Small blocks -->
      <div class="bg-zinc-900 rounded-3xl p-8">Quick Stat 1</div>
      <div class="bg-zinc-900 rounded-3xl p-8">Quick Stat 2</div>
      <div class="bg-zinc-900 rounded-3xl p-8">Image Block</div>
      <div class="col-span-2 bg-zinc-900 rounded-3xl p-8">Wide Supporting Content</div>
    </div>
  </div>
</body>
</html>