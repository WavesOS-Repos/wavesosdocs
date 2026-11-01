# Wallfliper Architecture

**Repository:** WavesHyprland  
**Branch:** main (WavesOS current)
**Version:** 0.1.0

---


## Layers

- main.py — CLI and application bootstrap
- core/ — library scanning, backends, thumbnails, previews, colors, cache GC, single instance, state, integrations, deps
- ui/ — Qt bridge, model, QML, shaders

## Backends

- Images: swww or awww
- Video: mpvpaper

## Config

config.json including color_hook (currently hardcoded path — see audits)
