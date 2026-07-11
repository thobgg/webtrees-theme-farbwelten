# Farbwelten – ein webtrees-Theme mit vier Paletten

*English version: [README.md](README.md)*

**Farbwelten** ist ein Custom-Theme für [webtrees](https://webtrees.net) 2.2:
**ein** Theme-Modul mit **vier** Farbpaletten, direkt im Kopfmenü umschaltbar –
gebaut nach dem Muster des Core-Themes „colors":

| Palette | Charakter |
|---|---|
| **Hell** | Navy & Gold auf warmem Papierton – die Leit-Palette |
| **Dunkel** | Dark Mode: dunkler Navy-Grund, Amber-Akzente |
| **Sepia** | Warme Buchdruck-Anmutung, ideal für Ortsfamilienbücher (inkl. Druck-Stylesheet) |
| **Bordeaux** | Tiefes Weinrot & Gold auf Creme – Leder-Einband-Gefühl |

Alle Paletten teilen sich ein Struktur-Stylesheet und unterscheiden sich
nur in Farbvariablen – sie wirken wie eine Familie. Die Textkontraste
erfüllen durchgängig WCAG AA (≥ 4,5:1), Fließtext meist 10:1 und besser.

## Funktionen

- **Paletten-Menü im Kopfbereich** – jeder Benutzer behält seine eigene Wahl;
  die Wahl eines Administrators wird Site-Standard für Besucher.
- **Serifen-Typografie** (Georgia) für Überschriften, abgestimmte Tabellen,
  Faktenblätter, Formulare, Tabs, Dropdowns und Diagramm-Boxen.
- **Linien-Menü-Icons** als SVG-Masken – sie färben sich automatisch
  passend zur aktiven Palette.
- **Druck-Stylesheet** in der Sepia-Palette (blendet Navigation aus,
  schaltet auf Schwarz/Weiß) – nützlich als Vorstufe für OFB-Seiten.
- **Responsive** – basiert auf dem Minimal-Theme (Bootstrap 5), mit
  zusätzlichem Feinschliff für kleine Bildschirme.
- **Update-Prüfung** – das Kontrollpanel meldet neue Versionen.

## Voraussetzungen

- webtrees **2.2.x**
- PHP 8.2+

## Installation

1. [Aktuelles Release](https://github.com/thobgg/webtrees-theme-farbwelten/releases) herunterladen.
2. Nach `modules_v4/theme-farbwelten/` der webtrees-Installation entpacken.
3. Im Kontrollpanel prüfen, dass das Modul aktiv ist
   (*Kontrollpanel → Module → Alle Module → Farbwelten*).
4. **Farbwelten** als Theme wählen (Theme-Menü im Kopfbereich oder
   *Kontrollpanel → Website-Einstellungen → Standard-Theme* für alle).
5. Im neuen **Palette**-Menü im Kopfbereich eine Palette wählen.

## Eigene Palette ergänzen

Die Struktur steht einmalig in `resources/css/base.css` und verwendet
ausschließlich CSS-Variablen (`--fa-*`). Eine Palette ist eine einzelne
CSS-Datei, die diese Variablen belegt:

1. `resources/css/palette-hell.css` nach `palette-<name>.css` kopieren und
   Werte anpassen (Pflicht-Variablen: [PALETTEN-KONTRAKT.md](PALETTEN-KONTRAKT.md)).
2. Palette in der Methode `palettes()` in `module.php` eintragen.

## Hinweise

- Der Icon-Satz enthält auch Icons für die Menü-Klassen `menu-sammlungen`
  und `menu-ortsregister` der Module
  [Sammlungen](https://github.com/thobgg/webtrees-sammlungen) und
  [Ortsregister](https://github.com/thobgg/webtrees-ortsregister).
  Ohne diese Module greifen die Selektoren einfach nie – keine Nebenwirkungen.

## Lizenz

GPL-3.0 – siehe [LICENSE](LICENSE). Abgeleitet von webtrees-Theme-Code
© webtrees development team.
