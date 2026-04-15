---
style_name: Early Web 1.0 / Geocities Style
aliases: Geocities Style, Old Web, Web 1.0, 1990s Personal Homepage, Early Internet Aesthetic, 90s Amateur Web
description: The chaotic, colorful, amateur, and highly personal homepage aesthetic from the mid-to-late 1990s (1995–1999), typical of GeoCities, Angelfire, and Tripod users. Raw, unpolished, maximalist, and full of enthusiasm — the true "vernacular web" before professional web design took over.
---

### Style Definition
Early Web 1.0 / Geocities Style represents the golden age of personal homepages when anyone with basic HTML knowledge could publish their own site. Pages were created by ordinary people (often teenagers or hobbyists), not professional designers. The result is loud, personal, imperfect, and full of joy — a celebration of individual expression over polished usability.

Core spirit: **Personal expression first, technical perfection second.** Pages feel like someone's digital bedroom or scrapbook.

### Core Visual Characteristics (Must Strictly Follow)
- **Backgrounds**: Strongly prefer repeating tiled background images (background-repeat). Common examples:
  - Starfields, space/nebula patterns
  - Marble, flames, water droplets, clouds, geometric patterns
  - Bright solid colors (electric blue, purple, hot pink, lime green) or simple gradients
  - Legibility often sacrificed for visual impact

- **Color Palette**: High-contrast, bright, and saturated. Heavy use of hot pink (#FF00FF / #FF1493), lime green (#00FF00 / #39FF14), cyan, yellow, and red text on dark or busy backgrounds. Avoid modern muted, elegant, or low-saturation palettes.

- **Typography**:
  - Default system fonts only: Times New Roman, Arial, Comic Sans MS, Courier New, Verdana.
  - Heavy use of `<font face="" color="" size="">` to randomly change font, color, and size.
  - Titles often large, centered, colored, bold, underlined, or in multiple fonts.
  - Hyperlinks are classic underlined blue or bright colors.

- **Layout**:
  - Primary layout method: HTML `<table>` (often heavily nested tables).
  - Centered or left-aligned linear content.
  - Typical structure: Header with big welcome/title + animated GIF, main content area, sidebar with links, footer with counter/guestbook.
  - Fixed width (optimized for 800x600 resolution). No responsive design.

- **Signature Elements** (Use abundantly — these are essential):
  - **Animated GIFs everywhere**: Spinning globes, dancing babies, flaming text, construction workers, blinking "New!", email icons, dividers, "Under Construction" banners, glitter graphics.
  - **<marquee>**: Scrolling text for announcements or welcome messages.
  - **Blinking text** (via `<blink>` or animated GIFs).
  - **Hit Counter**: Visitor counter GIF or image.
  - **"Under Construction"**: Almost mandatory banner or text.
  - **Guestbook** and **Web Rings** links.
  - **"Best viewed in Netscape Navigator at 800×600"** warning.
  - **MIDI Background Music**: Auto-playing .mid files (modern fallback: `<audio>` with loop).
  - **88x31 buttons**: Small "friendship" or "award" buttons.
  - Horizontal rules (`<hr>`) and basic clip art.

- **Overall Atmosphere**: Chaotic, noisy, playful, amateur, enthusiastic, and slightly "bad but charming." Many simultaneous animations, clashing colors, and personal touches.

### Strictly Prohibited (To Avoid Modern or "Clean" Feel)
- Any modern CSS techniques (Flexbox, Grid, backdrop-filter, soft shadows, large rounded corners, glassmorphism, smooth gradients).
- Low-saturation, minimalist, elegant, or professional color schemes.
- Clean whitespace, generous spacing, or sophisticated typography (no Space Grotesk, Satoshi, etc.).
- Responsive / mobile-first layouts.
- Modern icon libraries (Font Awesome, SVG icons) — use only old-school GIFs or clipart.
- Any element that looks "designed," "premium," or "user-friendly" by today's standards.

### Recommended Modern Implementation (To Simulate Authentic 1990s)
- Use heavy `<table>` layouts and legacy tags (`<center>`, `<font>`, `<marquee>`).
- CSS (minimal): `background: url('tiled-bg.gif') repeat;` + bright `color` declarations.
- Source low-resolution 256-color GIFs (search Internet Archive Geocities collections or "90s animated gif pack").
- For MIDI: Use `<audio autoplay loop>` with a .mid or converted file.
- Keep file sizes small and loading "feel" slow/authentic if possible.

### Example Code Snippet (Classic Geocities-style Homepage)
```html
<body bgcolor="#000000" text="#00FF00" link="#FF00FF" background="starfield.gif">
<center>
  <img src="welcome.gif" alt="Welcome!!!">
  <h1><font face="Comic Sans MS" color="#FF1493" size="7">My Awesome Homepage!!!</font></h1>
  
  <marquee behavior="scroll" direction="left" bgcolor="#FFFF00">
    Under Construction! Come back soon!!
  </marquee>
  
  <table width="80%" border="3" cellpadding="10" cellspacing="5">
    <tr>
      <td><img src="dancing-baby.gif"><br>My Hobbies</td>
      <td>My Favorite Links</td>
    </tr>
  </table>
  
  <p>This page has been visited <img src="counter.gif"> times!</p>
  <p><a href="guestbook.html">Sign My Guestbook</a> | <a href="links.html">Cool Links</a></p>
</center>
</body>