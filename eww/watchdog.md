# EWW Watchdog

**Script:** `~/.config/hypr/scripts/eww-watchdog.sh`  
**State:** `~/.config/eww/active-widget` (or path used by your switcher)

---

## Significance

Wallpaper engines restart or flash the desktop; without a watchdog, widgets die or the session falls back to a default widget. The watchdog keeps the **user’s chosen** widget alive.

---

## How we built it

1. Merged with **eww-widget.sh** responsibilities so switcher and watchdog do not fight.  
2. Reads **active-widget** and runs `eww open` on that name.  
3. `--ensure` / repair mode reopens the preferred widget without forcing Antares.  
4. Started from **autostart** after EWW daemon is available.

---

## How to use

Autostart:

```lua
hl.exec_cmd("~/.config/hypr/scripts/eww-watchdog.sh")
```

Change widget via switcher; watchdog will keep that choice across wallpaper updates.
