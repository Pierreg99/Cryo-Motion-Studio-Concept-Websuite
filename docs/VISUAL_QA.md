# MOTION — Visual QA Checklist

## Desktop

- Hero reads in a clear left-copy / right-visual hierarchy.
- Dashboard keeps a stable 3D composition while responding softly to pointer movement.
- Hero SVG remains subordinate to the typography and UI chrome.
- Service cards form a balanced three-column rhythm.
- NOVA and AURA artwork supports, rather than obscures, copy and CTA controls.
- Gradient, blur, border and shadow values stay restrained.

## Tablet

- Hero converts to a stacked composition without hiding the main CTA.
- Navigation progressively simplifies.
- Case-study artwork remains clipped inside its card.

## Mobile

- Main navigation keeps brand and project CTA visible.
- Hero visual moves below the copy.
- Service and project cards stack to one column.
- Large typography uses responsive clamps and does not create horizontal overflow.
- SVG artwork remains crisp without external image requests.

## Motion

- Ambient orbs float slowly.
- Hero dashboard parallax is disabled on small screens.
- Scroll reveal uses IntersectionObserver.
- `prefers-reduced-motion: reduce` removes practical animation and transition effects.

## Offline

No external font, image, CDN, framework or build dependency is required by the site. SVG artwork is stored inside `assets/` and linked locally.
