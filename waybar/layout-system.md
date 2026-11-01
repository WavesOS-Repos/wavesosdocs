# Waybar Layout System

**Layouts:** `~/.config/waybar/configs/*`  
**Styles:** `~/.config/waybar/style/*.css`  
**Active links:** `config` → chosen layout, `style.css` → chosen CSS  
**Switcher:** `~/.config/hypr/scripts/waybar-layout.sh`  
**Reload:** `~/.config/hypr/scripts/waybar-reload.sh`  
**Colours:** Matugen → `wall-theme.css` / theme include

---

## Significance

Users can change the **shape** of the bar (top full width, left vertical, skew, dual-tone, etc.) without losing wallpaper-driven colours.

---

## How we built it

1. Multiple layout JSON/JSONC files and matching CSS files.  
2. Switcher updates symlinks `config` and `style.css`, then restarts Waybar cleanly (kill old instance first to avoid stacked bars).  
3. All layouts consume **shared Matugen colour variables** (not hard-coded hex), after an initial pass where only some CSS files were wired.  
4. Modules live under `modules/*.jsonc` and are included per layout.

---

## How to use

```bash
~/.config/hypr/scripts/waybar-layout.sh
# pick layout — e.g. full-top, bar-left, skew-left
~/.config/hypr/scripts/waybar-reload.sh --reload
```

Typical keybind: Super+Ctrl+W for layout switch, Ctrl+Esc for reload (see your `keybinds.lua`).
