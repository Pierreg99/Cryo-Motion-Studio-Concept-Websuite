# MOTION — 3D Art Direction 2.0

## Ziel

Die 3D-Art-Direction erweitert die visuelle Identität von MOTION ohne WebGL, Three.js oder externe Rendering-Libraries. Die Illusion von Tiefe entsteht aus SVG-Layern, Gradients, Glow-Feldern, Glasflächen, perspektivischen Transformationen und langsamen Motion-Loops.

## Visuelle Bausteine

### Hero

`assets/hero-visual.svg` kombiniert eine transparente Monitorfläche, ein volumetrisches Ribbon, orbitale Kreise, ein schwebendes Interface-Panel und ein geometrisches Glasobjekt.

### NOVA

`assets/nova-visual.svg` nutzt ein cyan-violettes Motion-Sculpture-System, ein perspektivisches Glasprisma und konzentrische Orbitalringe. Das Artwork ist für die dunkle NOVA Case Study ausgelegt.

### AURA

`assets/aura-visual.svg` nutzt eine weichere pink-violette Formensprache, Sensor-/Orbit-Elemente und ein transluzentes geometrisches Panel für einen ruhigeren Wellness-Tech-Charakter.

## Motion Layer

Die Website kombiniert mehrere unabhängige Ebenen:

- langsames Ambient-Floating
- SVG-Artwork-Float
- Morphing der CSS-Container
- Hover-Depth für Project Cards
- Pointer-basierte Dashboard-Perspektive auf Desktop
- Reveal-on-scroll über IntersectionObserver
- reduzierte Bewegung über `prefers-reduced-motion`

## Performance

Die SVGs sind textbasierte, lokale Assets. Keine externen Bilder oder Runtime-3D-Engines werden geladen. Bewegungen verwenden überwiegend `transform`, `opacity` und GPU-freundliche Eigenschaften.

## Art-Direction-Prinzip

Die Visuals sollen wie gerenderte 3D-Objekte wirken, bleiben aber absichtlich als skalierbare Vektorgrafik und CSS komponiert. Damit bleibt die Website schnell, offline-fähig und versionierbar.

## Erweiterung

Weitere Szenen können aus denselben primitives aufgebaut werden: Rings, ribbons, planes, glass cards, orbital grids, soft glow fields und perspective layers. Die Farbwelt bleibt auf Electric Blue, Violet, Pink, Lime und tiefe Navy-Töne begrenzt.