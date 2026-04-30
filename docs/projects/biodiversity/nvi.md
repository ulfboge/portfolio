# NVI – Geodatadriven Naturvärdesinventering

![NVI Pipeline](../../assets/images/placeholder-project.png)

## Overview

A reproducible Python pipeline that combines **Swedish open geodata** (NMD, Lantmäteriet, Skogsstyrelsen) to produce a **prioritized hotspot map** for targeted field NVI (Naturvärdesinventering) surveys. The methodology and results are published as an interactive GitHub Pages site.

**Study Area:** Sweden (configurable AOI)  
**Role:** Solo project  
**Status:** Live  
**Live site:** [ulfboge.github.io/nvi](https://ulfboge.github.io/nvi)  
**Repository:** [github.com/ulfboge/nvi](https://github.com/ulfboge/nvi)

---

## Methods & Tools

**Data Sources**

- NMD (Nationellt Marktäckedata) — national land cover
- Lantmäteriet — topographic data and administrative boundaries
- Skogsstyrelsen — forest stand data
- SLU SOS — species observations (API)
- Swedish Red List (CSV) — threatened species
- Protected areas (Naturvårdsverket WFS)

**Processing Steps**

1. Download and preprocess NMD and Lantmäteriet layers
2. Compute ecological indices (woodland age, wetland, habitat connectivity)
3. Overlay species observations and red-listed species distributions
4. Build prioritized hotspot model combining multiple indices
5. Export hotspot raster and vector layers for field use
6. Generate showcase figures for GitHub Pages

**Tools Used**

| Tool | Purpose |
|------|---------|
| Python / GeoPandas / rasterio | Data processing and index computation |
| PostgreSQL + PostGIS | Spatial data management |
| QGIS | Visual QA and cartographic output |
| GitHub Pages | Results publication |

---

## Key Features

- Fully reproducible: runs from raw open data downloads
- Configurable AOI and index weights
- Integrates species observations and red-listed taxa
- Results published as interactive web page

---

## Links

[View Live Site](https://ulfboge.github.io/nvi){ .md-button .md-button--primary }
[View Code on GitHub](https://github.com/ulfboge/nvi){ .md-button }
