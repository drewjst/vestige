# Data sources

Vestige is built entirely on free, public, authoritative data. Every event links back to its
origin — nothing is modeled or summed across sources.

## Live feeds (v1)

| Source | Hazards | Spatial extent | Record floor | Geometry | Impact data |
|---|---|---|---|---|---|
| [USGS](https://earthquake.usgs.gov/) | Earthquakes | Global | 1900 | Observed point | None in feed |
| [IBTrACS](https://www.ncei.noaa.gov/products/international-best-track-archive) / [NHC](https://www.nhc.noaa.gov/) | Tropical cyclones | Global | 1842 | Track line | None in feed |
| [NOAA Storm Events](https://www.ncei.noaa.gov/products/storm-events-database) | Severe weather (US) — tornadoes, floods, heat, winter storms, **wildfires**, wind, and more | United States | 1996 | Observed point **or** county-attributed (zone-collected rows) | Deaths / damage itemized per event |

### What Storm Events does differently

Storm Events is the **only** v1 feed that carries ground impact. It is also the most
heterogeneous:

- **County-collected** rows (e.g. many tornadoes, flash floods) include begin/end coordinates →
  rendered as observed points.
- **Zone-collected** rows (heat, many floods/winter/wildfire/hurricane entries) have **no
  coordinates** — only an NWS forecast zone. Vestige attaches these at **county** level via the
  public zone→county correlation and labels them honestly (`geom_precision=county`). A zone name
  is never drawn as a pinpoint.

## Reference data (not event feeds)

| Data | Role |
|---|---|
| [Census TIGER/Line](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html) | County polygons (`places`) |
| [NWS zone–county correlation](https://www.weather.gov/gis/ZoneCounty) | Zone-collected Storm Events → county attachment |

## Provenance

Every event carries a `source_url` linking to the authoritative record — the USGS event page, an
NHC Tropical Cyclone Report, or the NCEI Storm Events event detail page (Event ID).

Live row counts and temporal floors are exposed at `GET /api/coverage` — every number is a real
count over the loaded database, never an estimate.

## Planned (not loaded)

**FEMA OpenFEMA** disaster declarations are the planned “add-a-feed” test — county FIPS only, no
hazard geometry. Not in the atlas today.

Each source records different things at different geographic precision. Vestige keeps those
differences visible — see [The honesty model](honesty-model.md).
