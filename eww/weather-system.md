# Weather scripts (EWW)

Shell helpers under `~/.config/eww/scripts/` fetch and format weather for widgets (temperature, humidity, wind, icon line). Prefer **long-term reliable** HTTP APIs (e.g. Open-Meteo) over brittle scrapers.

Defpoll in yuck calls these scripts on an interval. Failures should degrade to a placeholder string, not crash EWW.
