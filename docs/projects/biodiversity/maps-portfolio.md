# Maps Portfolio

![Maps Portfolio](../../assets/images/placeholder-project.png)

## Overview

A curated collection of biodiversity maps visualizing species distribution data for two iconic taxa: **galagos in Tanzania** and **lemurs in Madagascar**. Maps are produced in QGIS from GBIF occurrence data and published as both static print-quality outputs and interactive web maps via GitHub Pages.

**Study Areas:** Tanzania (galagos) · Madagascar (lemurs)  
**Role:** Solo project  
**Status:** Live  
**Live site:** [ulfboge.github.io/maps-portfolio](https://ulfboge.github.io/maps-portfolio)  
**Repository:** [github.com/ulfboge/maps-portfolio](https://github.com/ulfboge/maps-portfolio)

---

## Methods & Tools

**Data Sources**

- GBIF — species occurrence records (galagos, lemurs)
- Natural Earth — country boundaries and physical features
- SRTM — elevation for background shading

**Processing Steps**

1. Download and clean occurrence records from GBIF
2. Spatial filtering: remove records without coordinates or outside plausible range
3. Produce print-quality maps in QGIS (A4/A3 layouts)
4. Export interactive maps via Leaflet.js for web publication

**Tools Used**

| Tool | Purpose |
|------|---------|
| QGIS | Map design and layout |
| Python / pandas | GBIF data cleaning |
| Leaflet.js | Interactive web map |

---

## Links

[View Live Maps](https://ulfboge.github.io/maps-portfolio){ .md-button .md-button--primary }
[View Code on GitHub](https://github.com/ulfboge/maps-portfolio){ .md-button }
