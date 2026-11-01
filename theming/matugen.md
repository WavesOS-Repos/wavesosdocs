# Matugen

**Config:** `~/.config/matugen/config.toml`  
**Templates:** `~/.config/matugen/templates/`  
**Hook script:** `~/.config/hypr/scripts/matugen-from-wall.sh`

---

## Significance

Matugen is the **single palette engine** for WavesOS dynamic chrome: Hyprland borders (`matugen-colors.lua`), Waybar, Rofi, Kitty, EWW. Wallpaper changes should not require hand-editing colours.

---

## How we built it

1. Templates export Lua table for Hyprland and CSS/Rasi/SCSS for other apps.  
2. Wallfliper / wallpaper scripts call Matugen with a fixed mode (e.g. dark + vibrant/tonal scheme) and **non-interactive** source colour index so automation never blocks on prompts.  
3. `colors.lua` loads `matugen-colors.lua` with **fallback** colours if the file is missing (prevents Hyprland crash on first boot).  
4. Kitty must **not** use `dark-theme.auto.conf` that overrides Matugen opacity/colours.

---

## How to use

```bash
# From current wallpaper (scripted)
~/.config/hypr/scripts/matugen-from-wall.sh

# Manual example
matugen image /path/to/wall.png --mode dark --type scheme-vibrant --source-color-index 0
hyprctl reload
# reload waybar / eww as needed
```

Seed `matugen-colors.lua` exists before first Hyprland start if Matugen has never run.
