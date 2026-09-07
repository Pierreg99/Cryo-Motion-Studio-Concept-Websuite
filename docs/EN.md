# MOTION — Technical Documentation (EN)

## 1. Purpose

MOTION is a fictional premium digital studio presented as a static showcase site. It combines brand experience, web experience, motion design and abstract visual storytelling.

## 2. Technical Approach

The project deliberately avoids frontend frameworks, build tools and external UI libraries. It uses static HTML, modular CSS and a small vanilla-JavaScript interaction layer.

**Core technologies:** HTML5, CSS Custom Properties, Grid, Flexbox, gradients, blur, vanilla JavaScript, IntersectionObserver and `prefers-reduced-motion`.

## 3. Entry Point and Structure

`index.html` is the single canonical HTML entry point.

`script.js` owns scroll reveal, smooth internal navigation and the desktop hero-dashboard parallax effect.

`styles/` separates tokens, base rules, components, responsive rules and animations.

`assets/` contains standalone SVG visuals for the logo, hero, NOVA and AURA.

`docs/` contains technical, visual, accessibility and deployment documentation.

## 4. Visual System

The site uses a light editorial premium surface with translucent panels, thin contours, blue-violet-pink gradients, organic shapes and an abstract monitor/browser motif. The SVG artwork is original and offline-friendly.

## 5. Motion System

Ambient lights float slowly. The hero dashboard reacts to pointer movement in a `perspective(1300px)` scene. The ring, chart bars and project blobs are CSS-driven. Section content reveals through `IntersectionObserver` fade-up transitions.

## 6. Accessibility

Navigation and primary actions use native links. Section targets use stable IDs. With `prefers-reduced-motion: reduce`, movement and transitions are effectively disabled and the pointer parallax layer is not activated. See [`ACCESSIBILITY.md`](ACCESSIBILITY.md).

## 7. Responsive Behavior

Desktop uses multi-column hero and project compositions. At tablet and mobile widths the visual moves below the copy, services and projects stack vertically, and the navigation is simplified.

## 8. Performance

No external images, Google Fonts, CDNs, framework runtimes or build steps are required. SVG assets are text-based, and animations rely primarily on transform and opacity.

## 9. Deployment

The project can be opened locally or served as a static GitHub Pages site. `.nojekyll` supports direct static delivery.

See [`DEPLOYMENT.md`](DEPLOYMENT.md).
