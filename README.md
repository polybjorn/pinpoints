# <img src="favicon.svg" width="28" alt="Pinpoints icon"> Pinpoints

Interactive map for plotting and browsing travel destinations.

## Features

- Index view with places grouped by category
- Interactive map with all pins, marker clustering for dense areas
- Category-based color coding with toggleable legend
- Visited / want-to-visit status filtering
- Click a place card to focus it on the map
- Dark theme, responsive design

## File structure

```
places.json         # array of places (name, lat, lon, category, visited, note)
index.html          # the app
favicon.svg         # map pin icon
```

## Adding a place

Edit `places.json` and add an entry:

```json
{
  "name": "Place Name",
  "lat": 41.89,
  "lon": 12.49,
  "category": "landmark",
  "visited": false,
  "note": "Optional description",
  "sources": ["https://example.com/place"]
}
```

Categories are free-form strings. Colors are auto-assigned from a fixed palette. Sources are optional and can contain multiple URLs — shown as clickable domain names in map popups.

## Setup

Static site. No build step, no dependencies.

```sh
python3 -m http.server 8080
```

## Stack and attribution

- [Leaflet](https://leafletjs.com/) (BSD-2-Clause)
- [Leaflet.markercluster](https://github.com/Leaflet/Leaflet.markercluster) (MIT)

Tile providers:
- [OpenTopoMap](https://opentopomap.org) - CC-BY-SA
- [CyclOSM](https://www.cyclosm.org) - ODbL (OpenStreetMap)
- [Esri World Imagery](https://www.esri.com) - Esri
- [CARTO](https://carto.com) - CC-BY 3.0
- [OpenStreetMap](https://www.openstreetmap.org) - ODbL

## Place data

`places.json` is excluded from this repository. To use this app, create your own `places.json` with an array of place objects (see "Adding a place" above).
