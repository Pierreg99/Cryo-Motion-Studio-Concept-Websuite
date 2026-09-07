# MOTION

> Premium Digital Design Studio — art-directed static showcase for Brand, Digital and Motion.

![Hero visual](assets/hero-visual.svg)

## Positionierung

MOTION ist eine fiktive Premium-Digitalstudio-Website mit einer bewusst art-directed, editorialen Oberfläche. Die aktuelle Version verbindet eine dunkle visuelle Basis, Glasflächen, leuchtende Farbverläufe, abstrakte SVG-Visuals und zurückhaltende Motion-Interaktionen.

## Highlights

- Hochwertige Hero-Komposition mit interaktivem Dashboard
- Standalone SVG-Artwork für Hero, NOVA, AURA und Logo
- Responsive Single-Page-Architektur
- Sticky Glass-Navigation und native Anchor-Navigation
- Brand Experience, Web Experiences und Motion Systems als Kernleistungen
- Zwei visuelle Case Studies: NOVA und AURA
- Pointer-Parallax auf Desktop
- IntersectionObserver Reveal-System
- `prefers-reduced-motion`-Unterstützung
- Tastatur-Fokuszustände für zentrale Interaktionen
- Keine Frameworks, keine Build-Tools, keine externen Bild-/Font-CDNs
- Direkt lokal und GitHub-Pages-kompatibel

## Architektur

```text
motion-studio/
├── index.html
├── script.js
├── .nojekyll
├── README.md
├── assets/
│   ├── logo.svg
│   ├── hero-visual.svg
│   ├── nova-visual.svg
│   └── aura-visual.svg
├── docs/
│   ├── ACCESSIBILITY.md
│   ├── ASSETS.md
│   ├── DE.md
│   ├── EN.md
│   ├── DESIGN_SYSTEM.md
│   └── VISUAL_QA.md
└── styles/
    ├── tokens.css
    ├── base.css
    ├── components-1.css
    ├── components-2.css
    ├── components-3.css
    ├── components-4.css
    └── animations.css
```

## Assets

Die Visuals werden als lokale SVG-Dateien versioniert. Dadurch bleiben die Grafiken skalierbar, editierbar und offline verfügbar.

- `assets/logo.svg` — MOTION Markenmarke
- `assets/hero-visual.svg` — abstrakte Hero-Komposition
- `assets/nova-visual.svg` — NOVA Case Study
- `assets/aura-visual.svg` — AURA Case Study

Weitere Informationen: [`docs/ASSETS.md`](docs/ASSETS.md) und [`docs/DESIGN_SYSTEM.md`](docs/DESIGN_SYSTEM.md).

## Dokumentation

- [Deutsch — technische Dokumentation](docs/DE.md)
- [English — technical documentation](docs/EN.md)
- [Design System](docs/DESIGN_SYSTEM.md)
- [Accessibility](docs/ACCESSIBILITY.md)
- [Asset Guide](docs/ASSETS.md)
- [Visual QA](docs/VISUAL_QA.md)

## Technik

HTML5, CSS Custom Properties, Grid, Flexbox, gradients, blur, inline SVG und Vanilla JavaScript. Das Projekt verwendet keine Laufzeitabhängigkeiten außerhalb des Browsers.

## Motion-System

Ambient Orbs und Case-Study-Visuals bewegen sich langsam. Das Hero-Dashboard reagiert auf Pointer-Bewegung, während Inhalte beim Eintritt in den Viewport per `IntersectionObserver` eingeblendet werden. Bei aktivierter Systemoption `prefers-reduced-motion` werden die relevanten Bewegungen praktisch deaktiviert.

## Lokale Nutzung

```bash
git clone https://github.com/Pierreg99/motion-studio.git
cd motion-studio
```

Danach `index.html` direkt öffnen oder einen beliebigen statischen HTTP-Server verwenden.

## Deployment

Das Projekt ist für statisches Hosting geeignet. `.nojekyll` ist Bestandteil des Repositories. Für GitHub Pages kann der `main`-Branch als Quelle für statische Dateien verwendet werden.

## Qualitätsziel

Die aktuelle Ausbaustufe priorisiert Art Direction, klare visuelle Hierarchie, leichte Interaktion, Offline-Nutzung und wartbare modulare CSS-Strukturen. Weitere Ausbaustufen können vollständige Case-Study-Seiten, zusätzliche Accessibility-Prüfungen und automatisierte Browser-/Visual-Regression-Tests ergänzen.
