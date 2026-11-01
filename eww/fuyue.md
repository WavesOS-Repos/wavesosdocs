# Fuyue Widget

**Window name:** `fuyue`  
**Files:** `eww.yuck` (defwindow/defwidget), `eww.scss`, `scripts/fuyue-day-svg.sh`, weather scripts

---

## Significance

Fuyue is the **large calendar digit** desktop piece: oversized day-of-month with a vertical fade, weekday, month, clock, and weather. It is one of the signature visuals of the rice.

---

## How we built it

1. **SVG day number** — `fuyue-day-svg.sh` writes an SVG with `linearGradient` and Matugen primary colour; EWW displays it as an image.  
2. Vertical stretch and sizing tuned so the digit matches the original Conky reference screenshots.  
3. Weekday / month / time / weather as separate labels with careful margins (geometry height must be large enough or text clips).  
4. Open with `eww open fuyue` only (do not open Antares at the same time unless you want overlap).

---

## How to use

```bash
eww open fuyue
# switch away
~/.config/hypr/scripts/eww-widget.sh
```

If text is clipped at the bottom, increase the defwindow **height** (and keep position/`y` stable). Colours update when Matugen regenerates `colors.scss` / widget colour includes and EWW reloads.
