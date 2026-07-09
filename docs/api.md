# API

A small read-only API serves event detail behind the map. (The map's own tiles are static — the API
is never in the tile hot path.)

## Endpoints
| Method | Path | Returns |
|---|---|---|
| `GET` | `/api/events` | All events as a GeoJSON `FeatureCollection` |
| `GET` | `/api/event/{event_id}` | One event as a GeoJSON `Feature` |

Interactive OpenAPI docs are served at `/api/docs` when the API is running.

## Honesty fields
Every feature's `properties` carry the honesty facts:

| Field | Meaning |
|---|---|
| `geom_precision` | `observed_point` · `track_line` · `county` · … |
| `impact_source_present` | whether this source recorded impact (else absence is data) |
| `narrative_is_generated` | whether the summary was templated from fields |
| `source_url` | link to the authoritative record |
| `links` | detail path only — curated Related reading (`url`, `title`, `kind`, `matched_by`, `published_at`); never mixed into impact |

```json
{
  "type": "Feature",
  "geometry": { "type": "LineString", "coordinates": [ "..." ] },
  "properties": {
    "event_id": "ibtracs:2024268N17278",
    "hazard_type": "tropical_cyclone",
    "intensity_value": 120,
    "intensity_unit": "kt",
    "geom_precision": "track_line",
    "impact_source_present": false,
    "source_url": "https://www.nhc.noaa.gov/data/tcr/AL092024_Helene.pdf",
    "links": [
      {
        "url": "https://en.wikipedia.org/wiki/Hurricane_Helene",
        "title": "Hurricane Helene",
        "kind": "wikipedia",
        "matched_by": "manual",
        "published_at": null
      }
    ]
  }
}
```
