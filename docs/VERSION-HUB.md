# CRYO MOTION — Version Hub

`versions/hub.html` ist die zentrale Navigation der Concept Websuite.

## Kategorien

- **Products:** `variants/motion-flow.html`, `variants/motion-os.html`
- **Case Studies:** `projects/nova.html`, `projects/aura.html`
- **Concepts:** `concepts/motion-cinema.html`
- **Labs:** `labs/motion-editorial.html`, `experiments/motion-lab.html`
- **3D Showcases:** `showcase/motion-flow-3d.html`, `showcase/motion-os-3d.html`, `showcase/motion-cinema-3d.html`
- **Suite:** `index.html`

## Live-Demo-Navigation

Der Hub verwendet ausschließlich relative Links. Dadurch bleiben die Navigationen lokal, auf GitHub Pages und auf jedem beliebigen statischen Server identisch.

Jede Product-/Concept-Karte kann zwischen **Original Experience** und einer veredelten **3D Demo** unterscheiden. Die Demo-Seiten sind eigenständige HTML-Dateien und benötigen keine Runtime-Bibliothek.

Die Filter sind clientseitig mit Vanilla JavaScript umgesetzt. `aria-pressed` wird für den aktiven Filter gepflegt und die Cards können ohne Seitenwechsel ein-/ausgeblendet werden.

## 3D-Polish

Die neue `showcase/`-Ebene konzentriert sich auf die stärksten visuellen Richtungen:

- **MOTION FLOW:** volumetrischer Core, doppelte Orbit-Ringe, Glasprisma und Floating Signals
- **MOTION OS:** 3D-Device-Stage, Glasrahmen, Creative Kernel und KPI-Layer
- **MOTION CINEMA:** filmische Bühne, Lichtlauf, Morph-Core und mehrschichtige Orbit-Geometrie

## Ziel

Der Hub dient als Launchpad für alle visuellen Versionen. Neue Experimente können als eigenständige HTML-Datei in einem bestehenden oder neuen Verzeichnis ergänzt und anschließend als Karte im Hub registriert werden.
