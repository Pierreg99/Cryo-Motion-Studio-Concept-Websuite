# MOTION Accessibility

## Semantics

The site uses native HTML landmarks including `header`, `nav`, `main`, `section`, `article`, and `footer`. Internal destinations use stable IDs.

## Keyboard

Primary navigation and actions are native links, so keyboard users can activate them without a custom interaction layer.

## Reduced Motion

`prefers-reduced-motion: reduce` minimizes CSS animation and transition timing. The pointer-based 3D dashboard effect is not enabled when reduced motion is requested.

## Decorative Artwork

The standalone SVGs are treated as visual assets. Informational imagery receives an accessible `alt` description; decorative CSS shapes are hidden from assistive technology.

## Production QA

Before launch, run keyboard-only navigation, screen-reader checks, Axe/Lighthouse audits, and responsive visual regression tests across current desktop, tablet, and mobile browsers.
