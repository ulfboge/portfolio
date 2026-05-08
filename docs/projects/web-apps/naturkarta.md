# Naturkarta — Skyddad natur och skog

![Naturkarta – Skyddad natur och skog](../../assets/images/naturkarta-screenshot.png)

## Overview

An **interactive web GIS application** visualizing Swedish nature conservation data — nature reserves, national parks, Natura 2000 habitats, and logging notifications — built on **Origo Map**, the open-source framework used by Swedish municipalities and county administrative boards (*länsstyrelser*). The application mimics a realistic Swedish municipal nature conservation GIS portal.

**Study Area:** Sweden (national WMS layers); Stockholm County (clickable GeoJSON detail)  
**Role:** Solo project  
**Status:** Active — Phase 2 complete  
**Repository:** [github.com/ulfboge/svensk-naturkarta-origo-demo](https://github.com/ulfboge/svensk-naturkarta-origo-demo)

---

## Layers & Data

| Layer | Source | Type |
|-------|--------|------|
| Naturreservat (hela Sverige) | Naturvårdsverket | WMS |
| Naturreservat — klickbar popup, Stockholms Län | Naturvårdsverket (CC0) | Local GeoJSON |
| Nationalparker | Naturvårdsverket | WMS |
| Natura 2000 | Naturvårdsverket INSPIRE | WMS |
| Avverkningsanmälningar | Skogsstyrelsen | WMS |
| Bakgrundskarta | OpenStreetMap / OpenTopoMap | Tile |

Click any nature reserve in the Stockholm area to see a popup with name, protection type, IUCN category, area (ha), designation date, county, municipality, and managing authority. 383 reserves are available as local GeoJSON to avoid CORS issues and enable offline use.

---

## Features

- **Clickable popups** with full attribute data — name, IUCN category, area, designation date, county, municipality, manager
- **WMS layers** from Naturvårdsverket and Skogsstyrelsen for national-scale coverage
- **Background layer switcher** — OpenStreetMap / OpenTopoMap
- **Coordinate display** in SWEREF99 TM and WGS84 simultaneously
- **Measure tool**, scale bar, and map title overlay
- **Green forest theme** — custom CSS overrides matching the nature domain

---

## Methods & Tools

**Architecture decision:** No npm, no bundler, no backend. Origo is served as a pre-built UMD browser bundle — mirroring how Swedish municipalities deploy GIS applications in production. All configuration lives in a single `origo.json` file.

| Component | Technology |
|-----------|-----------|
| Map framework | Origo Map v2.10 |
| Rendering engine | OpenLayers 9 (bundled inside Origo) |
| Configuration | JSON (`public/config/origo.json`) |
| Local data | GeoJSON — 383 Stockholms Län nature reserves |
| Projections | EPSG:3857 display + SWEREF99 TM / WGS84 readout |
| Dev server | `python -m http.server` |

**Data sources (all CC0 / open):**

- Naturvårdsverket — nature reserves, national parks, Natura 2000
- Skogsstyrelsen — logging notifications (Avverkningsanmälningar)
- OpenStreetMap — background tiles (ODbL)
- GeoJSON pre-fetched via WFS to handle CORS constraints

---

## Links

[View Code on GitHub](https://github.com/ulfboge/svensk-naturkarta-origo-demo){ .md-button }
[Live Demo](https://ulfboge.github.io/svensk-naturkarta-origo-demo){ .md-button .md-button--primary }
