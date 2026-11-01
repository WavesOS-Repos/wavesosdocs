# Wallfliper Troubleshooting

**Repository:** WavesHyprland  
**Branch:** main (WavesOS current)
**Version:** 0.1.0

---


## Symptoms and Checks

| Symptom | Check |
|---------|-------|
| GUI does not start | python main.py --check; PySide6; layer-shell-qt |
| Images do not apply | swww query; swww-daemon running |
| Videos do not apply | mpvpaper installed; ffmpeg present |
| No color update | color_hook path valid and executable |
| Restore fails at login | delay in autostart; path to main.py |
