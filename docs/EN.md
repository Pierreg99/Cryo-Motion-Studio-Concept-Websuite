# MOTION — Technical Documentation (EN)

## 1. Purpose

MOTION is a fictional premium digital studio website presented as a static, art-directed showcase. The current iteration emphasizes a premium visual system combining Brand Experience, Web Experience, Motion Design and abstract SVG artwork.

## 2. Technical Approach

The site intentionally avoids frontend frameworks, build tools and external UI libraries. It uses static HTML, modular CSS, local SVG assets and a compact vanilla-JavaScript interaction layer.

**Core technologies:**

- HTML5
- CSS Custom Properties
- CSS Grid and Flexbox
- Gradients, blur and glass surfaces
- Standalone SVG assets
- Vanilla JavaScript
- IntersectionObserver
- Native anchor navigation
- `prefers-reduced-motion`

## 3. Art Direction

The visual language is designed as a high-end digital-studio presentation: dark foundation, translucent surfaces, precise borders, large editorial typography and controlled Electric Blue/Violet/Pink/Lime accents.

The hero combines an interactive browser/dashboard interface with local SVG artwork. Project cards use dedicated SVG compositions so each case reads as a distinct visual artboard.

## 4. Page Architecture

### Navigation

Sticky navigation with MOTION wordmark, internal anchors and primary project CTA.

### Hero

Large headline, studio eyebrow, supporting copy, two CTAs and an interactive dashboard. The dashboard uses a desktop pointer-parallax effect and local `hero-visual.svg` artwork.

### Services

Three core disciplines:

- Brand Experience
- Web Experiences
- Motion Systems

The cards combine glass surfaces, color-coded numbering and localized glows.

### Projects

NOVA and AURA are presented as visual case studies using dedicated SVG artboards and restrained motion.

### Contact

The closing CTA links to `mailto:hello@motion.studio`.

## 5. Assets

Primary visual assets are stored locally in `assets/`:

- `logo.svg`
- `hero-visual.svg`
- `nova-visual.svg`
- `aura-visual.svg`

This keeps the presentation usable offline without remote images or asset CDNs.

## 6. Motion System

- Ambient orbs float slowly.
- The hero dashboard reacts to pointer movement.
- The dashboard ring and bars animate continuously.
- Project artwork uses controlled morphing and rotation.
- Reveal elements enter through `IntersectionObserver`.

## 7. Accessibility

Native links, semantic sections, a skip link and visible `:focus-visible` states are included. `prefers-reduced-motion: reduce` practically disables meaningful animation and shows reveal elements immediately.

## 8. Responsive Behavior

Below desktop breakpoints the layout becomes progressively single-column. Navigation simplifies, the hero visual moves below the copy, service cards and case studies stack, and footer content wraps cleanly.

## 9. Performance

No external fonts, CDNs, frameworks or stock imagery are loaded. Local SVGs and predominantly transform/opacity-based motion keep the implementation lightweight.

## 10. Deployment

The repository is suitable for static hosting and GitHub Pages. `.nojekyll` remains included for static delivery.

## 11. QA

Design and validation rules are documented in [`DESIGN_SYSTEM.md`](DESIGN_SYSTEM.md) and [`VISUAL_QA.md`](VISUAL_QA.md).
