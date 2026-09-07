# MOTION — Technische Dokumentation (DE)

## 1. Zweck

MOTION ist ein fiktives Premium-Digitalstudio als statischer Website-Prototyp. Die Seite verbindet Brand Experience, Web Experience, Motion Design und abstrakte visuelle Gestaltung.

## 2. Technischer Ansatz

Die Anwendung verwendet keine Frontend-Frameworks, keine Build-Tools und keine externen UI-Bibliotheken. Die Basis ist statisches HTML, modularer CSS und ein kleiner Vanilla-JavaScript-Layer.

**Kerntechnologien:** HTML5, CSS3 Custom Properties, Grid, Flexbox, Gradients, Blur, Vanilla JavaScript, IntersectionObserver und `prefers-reduced-motion`.

## 3. Einstieg und Struktur

`index.html` ist der einzige kanonische HTML-Einstiegspunkt.

`script.js` übernimmt Scroll-Reveal, Smooth-Scrolling und den Desktop-Parallax-Effekt des Hero-Dashboards.

`styles/` trennt Tokens, Basiselemente, Komponenten, Responsive Regeln und Animationen.

`assets/` enthält eigenständige SVG-Visuals für Logo, Hero, NOVA und AURA.

`docs/` enthält technische, visuelle, Accessibility- und Deployment-Dokumentation.

## 4. Visual System

Die Website nutzt eine helle, galerieartige Premium-Oberfläche mit transluzenten Panels, feinen Konturen, Blau-/Violett-/Pink-Verläufen, organischen Formen und einem abstrakten Monitor-/Browser-Motiv. Die SVGs sind original und offline-fähig.

## 5. Motion System

Ambient Lights schweben langsam. Das Hero-Dashboard reagiert auf Pointer-Bewegung in einer `perspective(1300px)`-Szene. Ring, Chart-Balken und Case-Study-Blobs animieren sich ausschließlich per CSS. Inhalte werden über `IntersectionObserver` als Fade-Up eingeblendet.

## 6. Accessibility

Die Navigation und primären Aktionen sind native Links. Abschnittsziele verwenden eindeutige IDs. Bei `prefers-reduced-motion: reduce` werden Bewegungen und Übergänge praktisch deaktiviert und der Pointer-Parallax-Layer nicht aktiviert. Weitere Hinweise stehen in [`ACCESSIBILITY.md`](ACCESSIBILITY.md).

## 7. Responsive Verhalten

Desktop verwendet eine mehrspaltige Hero- und Projektkomposition. Auf Tablet und Mobile wandert das Visual unter den Hero-Text, Service Cards und Projekte werden einspaltig, und die Navigation wird reduziert.

## 8. Performance

Keine externen Bilder, Google Fonts, CDNs, Framework-Runtimes oder Build-Schritte. SVGs sind textbasierte Dateien; Animationen setzen vorwiegend auf `transform` und `opacity`.

## 9. Deployment

Das Projekt kann direkt lokal geöffnet oder über statisches Hosting wie GitHub Pages ausgeliefert werden. `.nojekyll` unterstützt die unveränderte statische Auslieferung.

Siehe [`DEPLOYMENT.md`](DEPLOYMENT.md).
