# MOTION — Technical Documentation (EN)

## 1. Purpose

MOTION is a fictional premium digital studio presented as a static website prototype. It demonstrates a high-end combination of brand experience, web experience, motion design and abstract visual storytelling.

## 2. Technical Approach

The project deliberately avoids frontend frameworks, build tools and external UI libraries. The frontend consists of static HTML, modular CSS and a small vanilla-JavaScript interaction layer.

**Core technologies:**

- HTML5
- CSS3 Custom Properties, Grid, Flexbox, gradients and blur
- Vanilla JavaScript
- IntersectionObserver
- native anchor navigation
- CSS `prefers-reduced-motion`

## 3. Page Architecture

### Navigation

The fixed glass navigation contains the MOTION wordmark, internal anchor links and the primary project CTA.

### Hero

The hero pairs a large editorial headline with an abstract browser/dashboard composition. The visual is constructed from HTML and CSS rather than external imagery.

### Services

Three equal-weight service cards present the core disciplines:

- Brand Experience
- Web Experiences
- Motion Systems

### Projects

The NOVA and AURA case studies use distinct color atmospheres and organic CSS shapes. Their visual forms are animated through changing border radii and rotation.

### Contact

The closing CTA links directly to `mailto:hello@motion.studio`.

## 4. Motion System

Motion is intentionally restrained:

- Ambient lights move slowly across the background.
- Gradient and organic shapes morph over time.
- The hero visual reacts to pointer movement on desktop.
- Content reveals with a fade-up as it enters the viewport.

The reveal system uses `IntersectionObserver` so off-screen elements begin visually subdued and transition into place only when visible.

## 5. Accessibility

Navigation uses native links and section targets use IDs. Sections provide `scroll-margin-top` so fixed navigation does not obscure the destination.

When `prefers-reduced-motion: reduce` is active, animation and transition durations are effectively disabled and reveal elements are shown immediately. The pointer-based 3D effect is not activated in reduced-motion mode.

## 6. Responsive Behavior

The desktop composition uses multiple columns. At smaller breakpoints the layout progressively becomes single-column:

- Navigation is simplified.
- The hero visual moves below the copy.
- Service cards stack vertically.
- Case studies stack vertically.
- Footer content wraps cleanly.

## 7. Performance Principles

The project does not load external images, Google Fonts, CDNs or large JavaScript frameworks. Visual assets are constructed with CSS, HTML and inline SVG. Motion relies primarily on transform- and opacity-based effects.

## 8. Repository Modularity

The stylesheet is split by responsibility: design tokens, base rules, components and animation rules. `index.html` is the primary entry point and `script.js` owns the interactive behavior.

## 9. Known Maintenance Point

`motion.html` and `index.html` currently contain the same HTML snapshot. For production, a single canonical entry point should be preferred unless multiple entry points are intentional.

## 10. Deployment

The repository is suitable for static GitHub Pages hosting. `.nojekyll` is included so the static files can be served directly without Jekyll processing.

## 11. Future Development

Useful next steps include a single-entry strategy, fully developed project pages, deeper semantic accessibility testing and automated browser/visual-regression tests.
