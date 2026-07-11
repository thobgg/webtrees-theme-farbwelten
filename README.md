# Farbwelten – a webtrees theme with four palettes

*Deutsche Version: [README.de.md](README.de.md)*

**Farbwelten** ("colour worlds") is a custom theme for [webtrees](https://webtrees.net) 2.2.
It is **one** theme module containing **four** colour palettes, switchable directly
from the header menu – modelled on the core "colors" theme:

| Palette | Character |
|---|---|
| **Hell** (light) | Navy & gold on warm paper – the lead palette |
| **Dunkel** (dark) | Dark mode: deep navy background, amber accents |
| **Sepia** | Warm book-print look, ideal for printed family books (includes a print stylesheet) |
| **Bordeaux** | Deep wine red & gold on cream – leather-bound album feel |

All palettes share one structural stylesheet and differ only in colour
variables, so they feel like one family. Text contrast meets WCAG AA
(≥ 4.5:1) throughout; body text typically reaches 10:1 or better.

## Features

- **Palette picker in the header menu** – each user keeps their own choice;
  an administrator's choice becomes the site default for visitors.
- **Serif typography** (Georgia) for headings, tuned tables, fact sheets,
  forms, tabs, dropdowns and chart boxes.
- **Line-style menu icons** as masked SVGs – they automatically recolour
  to match the active palette.
- **Print stylesheet** in the Sepia palette (hides navigation, switches to
  black on white) – useful as a preview for printed family book pages.
- **Responsive** – based on webtrees' minimal theme (Bootstrap 5), with
  additional small-screen refinements.
- **Update check** – webtrees' control panel will tell you when a new
  version is available.

## Requirements

- webtrees **2.2.x**
- PHP 8.2+

## Installation

1. Download the [latest release](https://github.com/thobgg/webtrees-theme-farbwelten/releases).
2. Unpack it into `modules_v4/theme-farbwelten/` inside your webtrees installation.
3. In the control panel, make sure the module is enabled
   (*Control panel → Modules → All modules → Farbwelten*).
4. Select **Farbwelten** as a theme (theme menu in the header, or
   *Control panel → Website preferences → Default theme* to make it the
   site default).
5. Pick a palette from the new **Palette** menu in the header.

## Adding your own palette

The structure is defined once in `resources/css/base.css`, which only
consumes CSS custom properties (`--fa-*`). A palette is a single CSS file
defining those variables. To add one:

1. Copy `resources/css/palette-hell.css` to `resources/css/palette-<name>.css`
   and adjust the values (the required variables are documented in
   [PALETTEN-KONTRAKT.md](PALETTEN-KONTRAKT.md)).
2. Add the palette to the `palettes()` method in `module.php`.

## Notes

- The menu icon set includes icons for the `menu-sammlungen` and
  `menu-ortsregister` classes used by the author's
  [Sammlungen](https://github.com/thobgg/webtrees-sammlungen) and
  [Ortsregister](https://github.com/thobgg/webtrees-ortsregister) modules.
  Without those modules the selectors simply never match – no side effects.

## License

GPL-3.0 – see [LICENSE](LICENSE). Derived from webtrees theme code
© webtrees development team.
