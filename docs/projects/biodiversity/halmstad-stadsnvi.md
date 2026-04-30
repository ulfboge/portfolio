# Halmstad StadsNVI

![Halmstad StadsNVI](../../assets/images/placeholder-project.png)

## Overview

A **desktop NVI (Naturvärdesinventering)** project for an urban test area in Halmstad, Sweden, using open geodata to identify and prioritize urban nature values. The project demonstrates how reproducible NVI workflows can be applied in municipal and urban planning contexts using only freely available Swedish geodata.

**Study Area:** Halmstad urban test area, Sweden  
**Role:** Solo project  
**Status:** Completed  
**Repository:** [github.com/ulfboge/halmstad-stadsnvi-project](https://github.com/ulfboge/halmstad-stadsnvi-project)

---

## Methods & Tools

**Data Sources**

- NMD (Nationellt Marktäckedata, 2018 base layer) — land cover classification
- Lantmäteriet — topographic data and base maps
- Open Swedish municipal data — green space layers

**Processing Steps**

1. Preprocess NMD and topographic layers for the study area
2. Apply NVI-relevant classification: forest, wetland, semi-natural grassland, urban green
3. Compute nature value indices per land cover type
4. Produce prioritization maps for field survey planning
5. Export PDF/PNG outputs and documented QGIS project

**Tools Used**

| Tool | Purpose |
|------|---------|
| QGIS | Analysis, map production, project documentation |
| NMD 2018 | Land cover baseline |
| Python (scripting) | Data preparation |

---

## Key Features

- Demonstrates NVI methodology in an urban context
- Fully reproducible QGIS project with documented layers and styles
- Print-quality cartographic outputs (PDF/PNG)

---

## Links

[View Code on GitHub](https://github.com/ulfboge/halmstad-stadsnvi-project){ .md-button }
