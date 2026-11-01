# Wallfliper Overview

**App path:** `~/.config/wallfliper` (deployed from `apps/wallfliper`)  
**Run:** `python main.py` from that directory (or your wrapper)

---

## Significance

Wallfliper is the **wallpaper picker** for WavesOS: browse library, set static or video wallpapers, restore on login, and trigger Matugen so the whole rice recolors.

---

## How we built / integrated it

1. Shipped as an app tree (Python + UI), not only a shell script.  
2. Session autostart restores the last wallpaper.  
3. Colour hook calls Matugen (config must use **your** `$HOME`, not a hardcoded foreign path).  
4. Works with swww/awww/mpvpaper-style backends depending on build.

---

## How to use

```bash
cd ~/.config/wallfliper
python main.py
```

After install, fix any hardcoded paths in `config.json` hooks. Pair with `matugen-from-wall.sh` if the hook is not enough.
