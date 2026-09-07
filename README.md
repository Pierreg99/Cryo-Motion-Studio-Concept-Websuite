# MOTION

> Premium Digital Design Studio — modulare, statische Showcase-Website für Brand Experience, Web und Motion.

## Visual Direction

MOTION kombiniert die zuletzt definierte helle Premium-Art-Direction mit transluzenten UI-Flächen, kühlen Blau-/Violett-/Pink-Verläufen, organischen Formen und einer präzisen Motion-Ebene. Das Hero-Visual ist als eigenständige SVG-Komposition angelegt und ergänzt das CSS-basierte Dashboard.

## Features

- Responsive Single-Page-Website
- Semantische HTML5-Struktur
- Sticky Navigation mit internen Anchor-Links
- Hero mit interaktivem 3D-Parallax-Dashboard
- Eigenständige SVG-Visuals für Hero, NOVA und AURA
- CSS-basierte Glow-, Blob-, Ring- und Chart-Animationen
- IntersectionObserver Fade-Up Reveal
- `prefers-reduced-motion` Unterstützung
- Kontakt über `mailto:hello@motion.studio`
- Keine Frameworks, keine Build-Tools, keine CDNs
- GitHub-Pages-kompatibel über `.nojekyll`

## Structure

```text
motion-studio/
├── index.html              # kanonischer Einstieg
├── script.js               # Vanilla JS interactions
├── .nojekyll
├── README.md
├── assets/
│   ├── logo.svg            # Brand Mark
│   ├── hero-visual.svg     # Hero / Monitor composition
│   ├── nova-visual.svg     # NOVA artwork
│   └── aura-visual.svg     # AURA artwork
├── docs/
│   ├── DE.md               # technische Dokumentation Deutsch
│   ├── EN.md               # technische Dokumentation Englisch
│   ├── ASSETS.md           # SVG / Visual asset guide
│   └── DEPLOYMENT.md       # statisches Deployment
└── styles/
    ├── tokens.css
    ├── base.css
    ├── components-1.css
    ├── components-2.css
    ├── components-3.css
    ├── components-4.css
    └── animations.css
```

## Architecture

`index.html` ist der einzige kanonische HTML-Einstieg und bindet die modularen CSS-Dateien sowie `script.js` ein.

`styles/` trennt Design-Tokens, globale Regeln, Hero/Services/Projects-Komponenten, Responsive-Regeln und Motion-Keyframes.

`assets/` enthält versionierbare SVG-Grafiken. Sie können offline geladen werden und benötigen keinen Bildserver.

`docs/` beschreibt technische Architektur, Assets, Accessibility und Deployment in Deutsch und Englisch.

## Interaction & Motion

Der Hero reagiert auf Pointer-Bewegungen mit einem dezenten `perspective(1300px)`-Parallax-Effekt. Section-Reveals verwenden `IntersectionObserver`. Hintergrund-Orbs, Ring, Chart-Balken und organische Shapes werden ausschließlich per CSS animiert.

Bei `prefers-reduced-motion: reduce` werden zeitbasierte Bewegungen und Transitionen praktisch deaktiviert; der Parallax-Layer wird nicht aktiviert.

## Local / Offline

```bash
git clone https://github.com/Pierreg99/motion-studio.git
cd motion-studio
```

Danach `index.html` direkt im Browser öffnen oder einen beliebigen statischen Server verwenden.

## GitHub Pages

Branch `main` plus Root als Veröffentlichungsquelle verwenden. `.nojekyll` bleibt im Repository-Root erhalten.

## Documentation

- [Deutsch](docs/DE.md)
- [English](docs/EN.md)
- [Assets](docs/ASSETS.md)
- [Deployment](docs/DEPLOYMENT.md)
- [Accessibility](docs/ACCESSIBILITY.md)

## Status

Premium statischer Frontend-Prototyp mit modularer CSS-Architektur, Vanilla-JavaScript und eigenständigem SVG-Visual-System.
