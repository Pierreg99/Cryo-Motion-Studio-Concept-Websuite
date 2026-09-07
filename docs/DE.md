# MOTION — Technische Dokumentation (DE)

## 1. Zweck

MOTION ist ein fiktives Premium-Digitalstudio als statischer Website-Prototyp. Die aktuelle Ausbaustufe legt den Schwerpunkt auf eine art-directed Premium-Oberfläche mit Brand Experience, Web Experience, Motion Design und abstrakter SVG-Visualisierung.

## 2. Technischer Ansatz

Die Anwendung verwendet keine Frontend-Frameworks, keine Build-Tools und keine externen UI-Bibliotheken. Das Frontend basiert auf statischem HTML, modularen CSS-Dateien, lokalen SVG-Assets und einem kleinen Vanilla-JavaScript-Layer.

**Kerntechnologien:**

- HTML5
- CSS3 Custom Properties
- Grid und Flexbox
- Gradients, Blur und Glassmorphism
- Inline-/Standalone-SVG
- Vanilla JavaScript
- IntersectionObserver
- native Anchor-Navigation
- CSS `prefers-reduced-motion`

## 3. Art Direction

Die visuelle Sprache wurde auf eine hochwertige Digital-Studio-Präsentation ausgerichtet: sehr dunkle Grundfläche, transluzente Panels, feine Konturen, große Editorial-Typografie und kontrollierte Electric-Blue/Violet/Pink/Lime-Akzente.

Die Hero-Szene kombiniert ein interaktives Browser-/Dashboard-Interface mit einer lokalen SVG-Illustration. Die Projektkarten verwenden separate SVG-Kompositionen, damit die Cases wie eigenständige Artboards wirken.

## 4. Seitenaufbau

### Navigation

Sticky Navigation mit MOTION Wortmarke, lokalen Ankerzielen und primärem CTA.

### Hero

Große Headline, Studio-Eyebrow, Beschreibung, zwei CTAs und ein interaktives Dashboard. Das Dashboard nutzt einen Desktop-Pointer-Parallax-Effekt und eine lokale `hero-visual.svg`.

### Leistungen

Drei Kernbereiche:

- Brand Experience
- Web Experiences
- Motion Systems

Die Karten besitzen Glasflächen, Farbnummern und dezente, lokalisierte Glows.

### Projekte

NOVA und AURA werden als visuelle Case Studies mit eigenständigen SVG-Artboards und animierter Präsentation dargestellt.

### Kontakt

Der finale CTA öffnet `mailto:hello@motion.studio`.

## 5. Assets

Alle visuellen Hauptassets liegen lokal in `assets/`:

- `logo.svg`
- `hero-visual.svg`
- `nova-visual.svg`
- `aura-visual.svg`

Dadurch funktionieren Preview und lokale Nutzung ohne externe Bilder oder Asset-CDNs.

## 6. Motion-System

- Ambient Orbs schweben langsam.
- Das Hero-Dashboard reagiert auf Pointer-Bewegung.
- Dashboard-Ring und Diagrammbalken animieren sich kontinuierlich.
- Projektvisuals verändern Form und Rotation.
- Reveal-Elemente erscheinen über `IntersectionObserver`.

## 7. Accessibility

Native Links, semantische Sections, Skip-Link und sichtbare `:focus-visible`-Zustände sind Bestandteil des Interfaces. `prefers-reduced-motion: reduce` deaktiviert relevante Animationen praktisch und zeigt Reveal-Elemente sofort.

## 8. Responsive Verhalten

Unterhalb der Desktop-Breakpoints wird das Layout auf eine Spalte reduziert. Navigation wird vereinfacht, das Hero-Visual wandert unter die Copy, Service Cards und Case Studies stapeln sich und der Footer bricht kontrolliert um.

## 9. Performance

Keine externen Fonts, CDNs, Frameworks oder Stockbilder. Lokale SVGs und überwiegend GPU-freundliche `transform`-/`opacity`-Animationen halten die Ausführung schlank.

## 10. Deployment

Das Repository ist für statisches Hosting und GitHub Pages geeignet. `.nojekyll` bleibt als statischer Hosting-Hinweis erhalten.

## 11. QA

Die Design- und Prüfregeln sind in [`DESIGN_SYSTEM.md`](DESIGN_SYSTEM.md) und [`VISUAL_QA.md`](VISUAL_QA.md) dokumentiert.
