# Data sources

Vestige is built entirely on free, public, authoritative data. Every event links back to its origin.

| Source | Hazards | What it provides |
|---|---|---|
| [USGS](https://earthquake.usgs.gov/) | Earthquakes | Precise epicenter points + magnitude. No impact data. |
| [IBTrACS](https://www.ncei.noaa.gov/products/international-best-track-archive) / [NHC](https://www.nhc.noaa.gov/) | Tropical cyclones | Best-track lines + intensity; NHC Tropical Cyclone Reports. No ground impact. |
| [NOAA Storm Events](https://www.ncei.noaa.gov/products/storm-events-database) | Severe weather (US) | Floods, tornadoes, heat, winter storms — with recorded deaths/damage (1996–). |

Each source records different things at different geographic precision. Vestige keeps those
differences visible rather than papering over them — see [The honesty model](honesty-model.md).

**Provenance:** every event carries a `source_url` linking to the authoritative record — the USGS
event page, the NHC report, the NCEI Storm Events entry.
