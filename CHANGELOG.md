# Changelog

## v1.0.0 – 2026-07-11

Erstes Release / initial release.

- Ein Theme-Modul mit vier Paletten: Hell, Dunkel, Sepia, Bordeaux
  (Muster: Core-Theme „colors" – Paletten-Menü, Benutzer-Präferenz,
  Admin-Wahl wird Site-Standard).
- Gemeinsame Struktur in `base.css` (Bootstrap-Mapping, Header mit
  Wortmarke, Tabellen, Faktenblätter, Formulare, Tabs, Dropdowns,
  Diagramm-Boxen, Footer, Fokus-Ringe, Mobil-Anpassungen).
- Paletten ausschließlich als CSS-Variablen-Sätze (`--fa-*`),
  dokumentiert in `PALETTEN-KONTRAKT.md`; Kontraste WCAG AA geprüft.
- Linien-Menü-Icons als SVG-Masken, palettenabhängig eingefärbt.
- Sepia mit Druck-Stylesheet (OFB-Vorstufe), Dunkel mit
  Dark-Mode-Sonderbehandlung für Formulare/Modale/Dropdowns.
- i18n: Englisch (Quellsprache) und Deutsch.
