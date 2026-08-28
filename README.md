# Verdana — Digital Oasis | Interactive 3D Grass Experience

Immersive WebGL experience featuring procedural grass, scroll-driven camera, and depth-of-field. A performant showcase for nature-driven brand storytelling and interactive landing pages.

Live Demo: `https://gourab775.github.io/3d-grass` · Category: Interactive Website / WebGL · Stack: HTML5, CSS, JavaScript (WebGL / Shaders)

---

## Overview

Verdana renders a lush, interactive grass field with realistic wind, lighting, and depth-of-field. The camera responds to scroll and pointer input, creating a calm, editorial atmosphere ideal for sustainability brands, wellness, and environmental campaigns.

Built as a single-file, dependency-free experience for maximum portability and load speed.

## Features

- **Procedural grass** — GPU-driven blades with wind animation, variation, and LOD
- **Cinematic camera** — Scroll-linked movement with smooth lerp and depth-of-field
- **Lighting & atmosphere** — Soft shadows, fog, and color-graded palette (`#e8ece4` on `#000`)
- **Zero-dependency** — Pure HTML/CSS/JS, no bundler, instant deploy
- **Responsive** — Fluid layout, viewport-fit, mobile gesture support

## Tech Stack

- **Rendering:** WebGL, custom GLSL shaders, Canvas
- **Frontend:** HTML5, CSS3 (Inter + Playfair Display), Vanilla JavaScript
- **Fonts:** Google Fonts (Inter 300-600, Playfair Display)
- **Deployment:** Static — any host (GitHub Pages, Vercel, Netlify)

## Project Structure

```
.
├─ index.html    # Markup + styles + WebGL + shaders + logic (self-contained)
└─ .gitignore
```

All styles and scripts are inline in `index.html` for a single-request demo. Split into `css/` + `js/` for larger builds if needed.

## Getting Started

Open `index.html` directly, or serve:

```bash
# Python
python -m http.server 8000

# Node
npx serve .
```

Then open `http://localhost:8000`.

## Deployment

Upload `index.html` as-is to any static host. No build, no env vars.

- **GitHub Pages:** Settings → Pages → Deploy from `master` / root
- **Vercel / Netlify:** Import repo, no build command, output `.`

## Customization

- **Palette:** Tweak CSS variables and WebGL clear color in `index.html` `<style>` and shader uniforms
- **Typography:** Swap `Inter` / `Playfair Display` imports in `<head>`
- **Grass density / wind:** Adjust shader uniforms and JS constants near top of `<script>` in `index.html`
- **Branding:** Update `<title>Verdana — Digital Oasis</title>` and hero copy

## Performance Notes

- Single HTML file ≈100 KB — ideal for LCP; inline critical CSS/JS
- For production, extract CSS/JS, minify, and compress textures
- Shader complexity scales with blade count — reduce density for low-end devices

## License

MIT — free for personal and commercial use.
