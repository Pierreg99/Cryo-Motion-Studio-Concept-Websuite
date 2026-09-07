# MOTION

> Premium Digital Design Studio — statische, modulare Showcase-Website mit Motion- und Brand-Experience-Fokus.

## Überblick

MOTION ist eine fiktive Premium-Digitalstudio-Website für Brand Experience, Web Experiences und Motion Systems. Die aktuelle Implementierung ist bewusst als statische Frontend-Anwendung ohne Framework aufgebaut.

Die visuelle Richtung verbindet eine helle, galerieartige Editorial-Oberfläche mit transluzenten UI-Flächen, sanften Blau-/Violett-/Pink-Verläufen und abstrakten CSS-Visuals. Die Hero-Szene simuliert ein hochwertiges Browser-/Monitor-Interface und reagiert auf Mausbewegungen mit einem dezenten 3D-Parallax-Effekt.

## Aktueller Funktionsumfang

- Responsive Single-Page-Website
- Semantische HTML-Struktur
- Sticky Glass-Navigation
- Anchor-Navigation für Leistungen, Projekte und Kontakt
- Hero mit interaktivem Browser-/Dashboard-Visual
- CSS-basierte abstrakte 3D-Formen und Licht-/Glow-Effekte
- Service-Karten für Brand Experience, Web Experiences und Motion Systems
- Zwei Case Studies: NOVA und AURA
- Kontakt-CTA mit `mailto:hello@motion.studio`
- IntersectionObserver-basierte Reveal-Animationen
- `prefers-reduced-motion`-Unterstützung
- Keine Bilder oder externen Asset-CDNs erforderlich
- GitHub-Pages-kompatible statische Struktur mit `.nojekyll`

## Projektstruktur

```text
motion-studio/
├── index.html
├── motion.html
├── script.js
├── .nojekyll
├── README.md
└── styles/
    ├── tokens.css
    ├── base.css
    ├── components-1.css
    ├── components-2.css
    ├── components-3.css
    ├── components-4.css
    └── animations.css
```

## Architektur

### `index.html`

Primärer Einstiegspunkt der Website. Das Dokument enthält Navigation, Hero, Services, Projects, Contact und Footer und bindet die modularen CSS-Dateien ein.

### `motion.html`

Aktuell ein zweiter statischer HTML-Einstieg mit identischem Inhalt zum vorhandenen `index.html`. Er kann für einen separaten Showcase-Einstieg genutzt oder später entfernt werden, falls nur ein einziger Einstiegspunkt gewünscht ist.

### `script.js`

Enthält das Vanilla-JavaScript für:

1. Scroll-Reveal mit `IntersectionObserver`
2. Mausgesteuerten 3D-Parallax-Effekt des Hero-Dashboards auf Desktop
3. Smooth Scrolling für interne Anchor-Links
4. Berücksichtigung von `prefers-reduced-motion`

### `styles/`

Die Styles sind nach Verantwortungsbereich getrennt. `tokens.css` enthält Design-Tokens, `base.css` globale Layout-/Grundregeln, `components-*.css` Komponenten und `animations.css` Bewegungs- und Übergangslogik.

## Designsystem

Die visuelle Sprache basiert auf:

- Hintergrund: sehr helles, neutrales Interface-Grau
- Primärfarben: Electric Blue, Violet, Pink, Lime
- Oberflächen: weiße/transluzente Cards mit Blur
- Konturen: sehr feine, kühle Linien
- Typografie: große, enge Editorial-Überschriften
- Formen: abgerundete Flächen, weiche Orbs und organische Blobs
- Motion: langsam, präzise und unterstützend statt dekorativ überladen

## Responsivität

Die Layouts wechseln bei kleineren Breakpoints von mehrspaltigen Bereichen zu einspaltigen Strukturen. Navigationselemente werden auf schmalen Displays reduziert, das Hero-Visual wird unterhalb des Textes angeordnet und Case Studies werden untereinander dargestellt.

## Accessibility & Motion

Die Anwendung setzt auf semantische Links und native Browser-Interaktionen. Bewegungsintensive Effekte werden über `prefers-reduced-motion: reduce` praktisch deaktiviert. Der interaktive Parallax-Effekt ist auf Desktop beschränkt.

## Offline / Deployment

Die Website benötigt für die vorhandene Implementierung keine Build-Pipeline und keine Laufzeit-Abhängigkeit. Bei einer lokalen Nutzung können die Dateien direkt aus dem Projektverzeichnis geöffnet werden. Für GitHub Pages dient `.nojekyll` dazu, dass das Projekt als statischer Inhalt ausgeliefert werden kann.

## Lokale Nutzung

```bash
git clone https://github.com/Pierreg99/motion-studio.git
cd motion-studio
```

Anschließend `index.html` im Browser öffnen oder den Ordner über einen beliebigen statischen HTTP-Server bereitstellen.

## Erweiterungspunkte

- Reduktion auf einen einzigen HTML-Einstiegspunkt
- Ausbau der Case Studies zu vollständigen Projektseiten
- Erweiterte mobile Navigation
- Kontaktformular mit externem Backend bei Bedarf
- zusätzliche Motion-/3D-Komponenten ohne externe Bibliotheken
- automatisierte visuelle/regressive Tests

## Status

Aktiver statischer Showcase-Prototyp mit modularer CSS-Struktur und Vanilla-JavaScript-Interaktionen.

---

## English

MOTION is a fictional premium digital studio website focused on brand experience, web experiences, motion systems and interactive visual storytelling.

The repository is intentionally framework-free and uses static HTML, modular CSS and small vanilla-JavaScript interactions. The interface is responsive, GitHub-Pages-friendly and designed to remain lightweight while preserving a premium visual character.

For the detailed English technical documentation, see [`docs/EN.md`](docs/EN.md).

For the detailed German technical documentation, see [`docs/DE.md`](docs/DE.md).
