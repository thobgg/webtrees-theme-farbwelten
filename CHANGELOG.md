# Changelog

## v1.0.0 (2026-07-11)

Erstes Release / initial release.

- Ein Theme-Modul mit vier Paletten: Hell, Dunkel, Sepia, Bordeaux.
  Paletten-Menü im Kopfbereich, Benutzer-Präferenz, Admin-Wahl wird
  Site-Standard (Muster: Core-Theme „colors").
- Gemeinsame Struktur in `base.css`: Bootstrap-Mapping, Header mit
  Wortmarke, Tabellen, Faktenblätter, Formulare, Tabs, Dropdowns,
  Diagramm-Boxen, Footer, Fokus-Ringe, Mobil-Anpassungen.
- Paletten als reine CSS-Variablen-Sätze (`--fa-*`), dokumentiert in
  `PALETTEN-KONTRAKT.md`. Kontraste nach WCAG AA geprüft.
- Menü-Icons als SVG-Masken, palettenabhängig eingefärbt.
- Sepia mit Druck-Stylesheet, Dunkel mit angepassten Formularen,
  Modalen und Dropdowns.
- Sprachen: Englisch (Quellsprache) und Deutsch.
