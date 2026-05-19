# Mammal Diversity Database (MDD) — Web Map & API

![MDD web map — type localities coloured by IUCN status](../../assets/images/mdd-map-screenshot.png)

## Overview

An **interactive web map and REST API** built on the [Mammal Diversity Database v2.4](https://www.mammaldiversity.org/) — 6,871 mammal species with nomenclatural synonyms, type localities, and optional GBIF occurrence overlays. DuckDB is the analysis backbone; a React + MapLibre frontend and FastAPI backend are packaged in a single Docker image for deployment.

**Data:** MDD v2.4 (Zenodo) + GBIF Occurrence API  
**Role:** Solo project  
**Status:** Active — live on Render  
**Live demo:** [mdd-map.onrender.com](https://mdd-map.onrender.com)
**Repository:** [github.com/ulfboge/MDD](https://github.com/ulfboge/MDD)

---

## What it does

| Component | Description |
|-----------|-------------|
| **Taxonomy DB** | DuckDB built from five MDD CSV files — species, ~100k synonyms, type specimen metadata, version diff |
| **Harmonization** | Resolve any reported name (GBIF, field CSV, literature) to the current MDD accepted name via the synonyms table |
| **Type localities** | ~1,941 geocoded holotype collection sites, coloured by IUCN status on the map |
| **GBIF pipeline** | `gbif_import.py` fetches occurrences, harmonizes names, and stores them in DuckDB + GeoParquet |
| **Web map** | Species / genus / family search, museum & country coverage filters, CSV export for missing coordinates, IUCN popups |
| **API** | FastAPI — species lookup, type-localities GeoJSON, occurrences per species, health check |
| **Deploy** | Single-container Docker (nginx + uvicorn + baked DuckDB); `render.yaml` for Render |

---

## Methods & Tools

| Layer | Technology |
|-------|------------|
| Database | DuckDB (spatial extension, GeoParquet export) |
| Backend | Python 3.11, FastAPI, uvicorn |
| Frontend | React, TypeScript, Vite, MapLibre GL JS |
| Data ingest | SQL scripts + `setup_database.py`, `gbif_import.py`, `harmonize_names.py` |
| GIS export | GeoParquet for QGIS; PostgreSQL/PostGIS migration scripts |
| Container | Docker, nginx reverse proxy |
| Hosting | Render Blueprint (`render.yaml`) |

**Design principle:** MDD is the taxonomy backbone — external datasets (GBIF, IUCN, field CSVs) are harmonized *to* MDD via `species_id` and the synonyms table, not the other way around. Coordinates in MDD are **type specimen localities** (where the holotype was collected), not species range centroids.

---

## Key features

- Global map of ~1,941 geocoded type localities with IUCN colour symbology
- Species autocomplete across 6,871 accepted names
- Per-species type locality highlight and optional “show all” layer
- GBIF occurrence layer (populated locally via import pipeline; not at container startup on free tier)
- Reproducible build: `setup_database.py` regenerates the full DuckDB from raw CSVs
- QGIS-ready GeoParquet exports and documented PostGIS migration path

---

## Links

[Live Demo](https://mdd-map.onrender.com){ .md-button .md-button--primary }
[View Code on GitHub](https://github.com/ulfboge/MDD){ .md-button }
[MDD data source](https://www.mammaldiversity.org/){ .md-button }

---

## Citation

```
Mammal Diversity Database. (2026). Mammal Diversity Database (Version 2.4) [Data set].
Zenodo. https://doi.org/10.5281/zenodo.18135819
```
