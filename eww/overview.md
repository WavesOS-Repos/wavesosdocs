# EWW Widgets Overview

**Config:** `~/.config/eww/` (`eww.yuck`, `eww.scss`, `colors.scss`)  
**Scripts:** `~/.config/eww/scripts/` and Hypr helpers `eww-widget.sh`, `eww-watchdog.sh`

---

## Significance in WavesOS

EWW provides **desktop widgets** without replacing Hyprland with a full shell (no Quickshell dependency). WavesOS ships three main experiences:

| Widget | Role |
|--------|------|
| **Antares** | System / time / weather style desktop widget |
| **Fuyue** | Large date digit (SVG gradient) + weekday + weather line |
| **Rock** | Compact date/time style widget |

Colours follow **Matugen** so widgets stay in the same palette as Waybar, Rofi, and borders.

---

## How we built it

1. Ported visual ideas from Conky themes (Antares / Fuyue) into **yuck + scss**.  
2. **Fuyue** uses a generated **SVG** for the tall faded day number (CSS alone could not match the gradient look reliably).  
3. Weather via shell scripts (prefer reliable HTTP sources such as Open-Meteo).  
4. **active-widget** state file + **watchdog** so wallpaper changes do not force Antares if the user chose Fuyue/Rock.  
5. **Widget switcher** script to open one widget and close others.

---

## How to use

```bash
eww daemon   # if not running
eww open antares
eww open fuyue
eww open rock
eww close antares   # etc.
eww reload
```

Switcher (Rofi or script):

```bash
~/.config/hypr/scripts/eww-widget.sh
```

Watchdog on autostart:

```bash
~/.config/hypr/scripts/eww-watchdog.sh
```

List windows: `eww list-windows`
