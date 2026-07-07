# Vestige — web

The public map front-end for **Vestige**, a historical atlas of extreme natural-hazard events.
An interactive dark map (MapLibre GL) that reads events from the Vestige API and renders each one
with its source trail and honest precision / impact labels.

## Status
Early walking skeleton — a single static `index.html` rendering USGS earthquakes + IBTrACS cyclone
tracks over a dark basemap, with a click-through dossier. A React / MapLibre app replaces this next.

## Run locally
1. Start the Vestige API so `http://localhost:8000` is serving events.
2. Serve this folder statically, e.g. `python3 -m http.server 5173`
3. Open http://localhost:5173

Point the front-end at another API by editing `API_BASE` at the top of the script in `index.html`.

## Tech
MapLibre GL JS + a free/open dark basemap — no Google/Mapbox keys, no tile server. The production
map hot-path is static vector tiles (PMTiles) on a CDN.
