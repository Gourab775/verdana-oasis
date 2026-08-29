# Verdana -- Digital Oasis | Interactive 3D Grass Experience

Immersive WebGL experience featuring procedural grass, scroll-driven camera, and depth-of-field. A performant showcase for nature-driven brand storytelling and interactive landing pages.

Live Demo: `https://3d-grass.vercel.app` | Category: Interactive Website / WebGL | Stack: HTML5, CSS, JavaScript (WebGL / Shaders)

---

## Overview

Verdana renders a lush, interactive grass field with realistic wind, lighting, and depth-of-field. The camera responds to scroll and pointer input, creating a calm, editorial atmosphere ideal for sustainability brands, wellness, and environmental campaigns.

Built with modular architecture for maintainability and performance.

## Features

- **Procedural grass** -- GPU-driven blades with wind animation, variation, and LOD
- **Cinematic camera** -- Scroll-linked movement with smooth lerp and depth-of-field
- **Lighting & atmosphere** -- Soft shadows, fog, and color-graded palette (`#e8ece4` on `#000`)
- **Modular architecture** -- Separated CSS and JS for maintainability, no bundler required
- **Responsive** -- Fluid layout, viewport-fit, mobile gesture support

## Tech Stack

- **Rendering:** WebGL, custom GLSL shaders, Canvas
- **Frontend:** HTML5, CSS3 (Inter + Playfair Display), Vanilla JavaScript
- **Fonts:** Google Fonts (Inter 300-600, Playfair Display)
- **Deployment:** Static -- any host (GitHub Pages, Vercel, Netlify)

## Project Structure

`
.
|-- index.html          # Markup + importmap + layout
|-- css/
|   -- styles.css        # Design system, layout, grass styling
|-- js/
|   -- app.js            # WebGL scene, shaders, animation loop, interactions
-- .gitignore
`

## Getting Started

Open `index.html` directly, or serve:

``bash
# Python
python -m http.server 8000

# Node
npx serve .
``

Then open `http://localhost:8000`.

## Deployment

Static site -- deploy repository root:

- **GitHub Pages:** Settings -> Pages -> Deploy from `master` / root
- **Vercel / Netlify:** Import repo, no build command, output `.`

No environment variables required.

## Customization

- **Palette:** Tweak CSS variables in `css/styles.css` and WebGL clear color in `js/app.js` shader uniforms
- **Typography:** Swap `Inter` / `Playfair Display` imports in `index.html` head
- **Grass density / wind:** Adjust shader uniforms and constants at top of `js/app.js`
- **Branding:** Update `<title>Verdana -- Digital Oasis</title>` and hero copy in `index.html`

## Performance Notes

- Modular CSS/JS enables caching and minification for production
- Shader complexity scales with blade count -- reduce density for low-end devices
- Compress textures and minify `css/styles.css` / `js/app.js` for LCP gains

## License

MIT -- free for personal and commercial use.
