# Theme Switching (dark / light)

**Script:** `~/.config/hypr/scripts/theme-switch.sh`

---

## Significance

Separates **toolkit theme** (GTK Relax light/dark, Kvantum, icons, gsettings color-scheme) from **Matugen dynamic colours**. Switching to light mode should not destroy Kitty/Matugen terminal colours.

---

## How we built it

1. Toggle or force paths refined during install (running the script twice can force “end on dark” when args were unreliable).  
2. Applies Relax GTK + Kvantum light/dark variants and icon packs.  
3. Users must avoid leaving Kitty `dark-theme.auto.conf` in place.  
4. File manager (Thunar) follows GTK; Qt apps follow Kvantum/qt6ct.

---

## How to use

```bash
~/.config/hypr/scripts/theme-switch.sh
```

Bind to a key if desired. Installer post-step typically ends on a dark desktop for first impression.
