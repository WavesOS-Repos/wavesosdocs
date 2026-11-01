# EWW ↔ Matugen

Matugen templates write colour tokens used by `colors.scss` / EWW includes. After wallpaper change:

1. Matugen runs (Wallfliper hook or `matugen-from-wall.sh`)  
2. Colour files update  
3. `eww reload` (or watchdog/open cycle) picks up new variables  

Widgets should **only** consume Matugen variables for accents/backgrounds so light/dark toolkit switches do not invent a second palette for EWW.
