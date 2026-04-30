# Madagascar Lemur SDM

![Madagascar Lemur SDM](../../assets/images/placeholder-project.png)

## Overview

**Species Distribution Modeling (SDM)** for five lemur species in Madagascar, combining cutting-edge **AlphaEarth satellite embeddings** with traditional bioclimatic predictors. The project evaluates habitat suitability across Madagascar-wide extents and within two protected areas: the Mandena Conservation Zone and Sahamalaza-Iles Radama National Park.

**Study Area:** Madagascar (island-wide) · Mandena Conservation Zone (~2×2 km) · Sahamalaza-Iles Radama NP  
**Species:** *Hapalemur meridionalis*, *Cheirogaleus medius*, *Lepilemur sahamalaza*, *Microcebus sambiranensis*, *Mirza zaza*  
**Role:** Solo project  
**Status:** Analysis complete  
**Repository:** [github.com/ulfboge/movement_ecology](https://github.com/ulfboge/movement_ecology)

---

## Methods & Tools

**Data Sources**

- AlphaEarth Embeddings (A00–A63, 2017–2024, 10–100 m) — satellite-derived feature embeddings
- SRTM — elevation, slope, aspect
- WorldClim BIO (bio01–bio19) — bioclimatic variables
- GBIF / field occurrence records — species presence points

**Processing Steps**

1. Compile species occurrence records with spatial filtering
2. Extract predictor values at occurrence and background points
3. Run ensemble SDM with LASSO regularization and Random Forest
4. Compare performance: traditional bioclimatic vs. AlphaEarth embeddings
5. Project habitat suitability maps for both study areas

**Tools Used**

| Tool | Purpose |
|------|---------|
| R — biomod2 | Ensemble SDM modeling |
| R — sf, terra | Spatial data handling |
| Python | AlphaEarth data preprocessing |
| QGIS | Map production and validation |

---

## Key Findings

- Evaluated the contribution of all 64 AlphaEarth embedding dimensions as predictors
- AlphaEarth embeddings improved model performance compared to bioclimate-only baselines
- Produced habitat suitability maps for both species and study areas
- Comparative analysis across Mandena and Sahamalaza datasets

---

## Links

[View Code on GitHub](https://github.com/ulfboge/movement_ecology){ .md-button }
