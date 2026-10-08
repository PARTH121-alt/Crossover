# Crossover

Crossover is a next-generation AI weather intelligence dashboard — live forecasting across every Indian state and UT, radar maps, environmental highlights, 7-day planning and a conversational weather assistant.

## Run it

No build step. Open the entry file directly:

```bash
open index.html
```

Or serve it:

```bash
python3 -m http.server 8080   # → http://localhost:8080
```

## What's inside

- **Dashboard** — live hero conditions, animated weather scene, 6 highlight cards (wind, UV, sun arc, humidity, visibility, feels-like), 7-day forecast with List/Bars modes, tomorrow deep-dive, US-style weather map repurposed over India, and pinned locations.
- **Weather Map** — full-size interactive map: 4 layers (Precipitation / Temperature / Clouds / Wind), radar sweep, zoom & pan, city markers.
- **Locations** — every Indian state & Union Territory with live temperature, condition and rain probability, sortable by clicking any card.
- **Radar** — precipitation-radar map with a 24h rain-bar breakdown.
- **Calendar** — 16-day planner plus tomorrow's hourly strip.
- **Alerts** — thunderstorm / heavy-rain / heat / wind advisories derived from live model output.
- **Settings** — °C/°F scope, automatic quick-check refresh interval, data-source toggle.

## Live data

Telemetry is pulled at runtime from the free [Open-Meteo](https://open-meteo.com) API — no key required. `assets/js/live.js` fetches the selected city's current conditions, hourly series and 16-day forecast, plus the per-state snapshot shown in Locations/Map, and republishes everything through `CXData`. The status pill in the sidebar shows whether the session is online (`LIVE`) or running on cached values (`OFFLINE`).

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `/` or `⌘K` | Open city search |
| `a` | Open the AI assistant |
| `u` | Toggle °C / °F |
| `Esc` | Close overlays |

## Layout

```
assets/css/   tokens · base · layout · components · animations
assets/js/    icons · data · live · weather-icons · charts · hero-scene ·
              highlights · forecast · map · locations · pages · search · ai · app
```
