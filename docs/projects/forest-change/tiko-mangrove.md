# Tiko Mangrove Threat Mapping

![Tiko Mangrove Threat Mapping](../../assets/images/tiko-mangrove-loss-by-year.png)

## Overview

Mapping and quantifying mangrove deforestation in the **Tiko area of Cameroon** using Hansen Global Forest Change (GFC) loss data constrained to the **Global Mangrove Watch v3 (GMW v3)** extent. The analysis quantifies yearly mangrove loss from 2001 to 2024, summarized by administrative units, and supports conservation planning with printable A3/A4 maps.

**Study Area:** Tiko area, Cameroon (AOI from project asset)  
**Duration:** 2001–2024 time series  
**Role:** Lead analyst  
**Status:** Completed  
**Repository:** [github.com/ulfboge/Tiko_Mangrove_Threat_Mapping](https://github.com/ulfboge/Tiko_Mangrove_Threat_Mapping)

---

## Methods & Tools

**Data Sources**

- Hansen GFC (lossyear) — annual tree cover loss raster
- Global Mangrove Watch v3 (GMW v3) — mangrove extent mask
- geoBoundaries ADM2 — administrative unit boundaries
- Project AOI (provided asset)

**Processing Steps**

1. Constrain Hansen GFC loss data to GMW v3 mangrove extent
2. Clip to project AOI
3. Calculate yearly mangrove loss area (2001–2024)
4. Summarize loss by administrative unit (ADM2)
5. Produce A3/A4 maps and technical summary tables

**Tools Used**

| Tool | Purpose |
|------|---------|
| Google Earth Engine | Forest loss extraction within mangrove mask |
| Python | Area statistics and tabular output |
| QGIS | Cartographic map production |

---

## Key Findings

- Quantified annual mangrove loss 2001–2024 within GMW v3 extent and project AOI
- Produced loss summaries by administrative zone for targeted conservation planning
- Delivered printable maps and technical notes suitable for client reporting

---

## Links

[View Code on GitHub](https://github.com/ulfboge/Tiko_Mangrove_Threat_Mapping){ .md-button }
