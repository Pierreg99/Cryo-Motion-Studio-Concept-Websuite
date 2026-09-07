# MOTION — Technische Dokumentation (DE)

## 1. Zweck

MOTION ist ein fiktives Premium-Digitalstudio als statischer Website-Prototyp. Die Seite demonstriert eine hochwertige Kombination aus Brand Experience, Web Experience, Motion Design und abstrakter visueller Gestaltung.

## 2. Technischer Ansatz

Die Anwendung verwendet keine Frontend-Frameworks, keine Build-Tools und keine externen UI-Bibliotheken. Das Frontend basiert auf statischem HTML, modularen CSS-Dateien und einem kleinen Vanilla-JavaScript-Layer.

**Kerntechnologien:**

- HTML5
- CSS3 mit Custom Properties, Grid, Flexbox, Gradients und Blur
- Vanilla JavaScript
- IntersectionObserver
- native Anchor-Navigation
- CSS `prefers-reduced-motion`

## 3. Seitenaufbau

### Navigation

Die fixe Glass-Navigation enthält die MOTION-Wortmarke, interne Anchor-Links und den primären Projekt-CTA.

### Hero

Der Hero kombiniert eine große Editorial-Headline mit einem abstrahierten Browser-/Dashboard-Visual. Das Visual wird ausschließlich aus HTML und CSS aufgebaut und simuliert eine hochwertige digitale Markenwelt.

### Leistungen

Drei gleichgewichtete Service Cards bilden die Kernkompetenzen ab:

- Brand Experience
- Web Experiences
- Motion Systems

### Projekte

Die Case Studies NOVA und AURA verwenden unterschiedliche helle Farbwelten und organische CSS-Shapes. Die Shapes werden per `border-radius`-Morphing und Rotation animiert.

### Kontakt

Der Abschluss der Seite führt über einen zentralen CTA direkt zu `mailto:hello@motion.studio`.

## 4. Motion-System

Die Animationen sind bewusst langsam und subtil:

- Ambient Lights bewegen sich in weiten Bahnen.
- Gradient-Elemente und organische Shapes verändern ihre Form.
- Hero-Visuals reagieren auf Pointer-Bewegungen.
- Inhalte erscheinen beim Erreichen des Viewports per Fade-Up.

Der Reveal-Mechanismus verwendet `IntersectionObserver`, um nicht sichtbare Inhalte zunächst mit reduzierter Opazität und vertikaler Verschiebung darzustellen.

## 5. Accessibility

Die Navigation besteht aus nativen Links. Abschnittsziele verwenden IDs und `scroll-margin-top`, damit die fixe Kopfzeile den Inhalt beim Scrollen nicht verdeckt.

Bei aktivierter Systemeinstellung `prefers-reduced-motion: reduce` werden Animationen und Übergänge praktisch deaktiviert und Reveal-Elemente unmittelbar sichtbar gemacht. Der Pointer-basierte 3D-Effekt wird bei reduzierter Bewegung nicht aktiviert.

## 6. Responsive Verhalten

Desktop verwendet mehrspaltige Kompositionen. Ab kleineren Breakpoints wird das Layout stufenweise auf eine Spalte reduziert:

- Navigation wird vereinfacht.
- Hero-Visual wandert unter den Text.
- Service Cards stapeln sich.
- Case Studies werden vertikal angeordnet.
- Footer-Inhalte umbrechen.

## 7. Performance-Prinzipien

Es werden keine externen Bilder, Google Fonts, CDNs oder großen JavaScript-Frameworks geladen. Die visuellen Elemente bestehen aus CSS, HTML und Inline-SVG. Animationen arbeiten überwiegend mit transform- und opacity-basierten Eigenschaften.

## 8. Repository-Modularität

Die aktuelle Codebasis trennt Design Tokens, Basiselemente, Komponenten und Animationen in mehrere CSS-Dateien. `index.html` ist der primäre Einstiegspunkt; `script.js` kapselt die interaktiven Funktionen.

## 9. Bekannter Wartungspunkt

`motion.html` und `index.html` enthalten derzeit denselben HTML-Stand. Für ein produktives Repository sollte nur ein kanonischer Einstieg verwendet werden, sofern keine bewusst getrennten Entry Points benötigt werden.

## 10. Deployment

Das Projekt ist als statische Website für GitHub Pages geeignet. Die Datei `.nojekyll` verhindert die Verarbeitung durch Jekyll und unterstützt die direkte Auslieferung der statischen Projektdateien.

## 11. Weiterentwicklung

Der nächste sinnvolle Ausbau umfasst eine einheitliche Entry-Point-Strategie, vollständig ausgearbeitete Projektseiten, zusätzliche semantische Accessibility-Prüfungen sowie automatisierte Browser-/Visual-Regression-Tests.
