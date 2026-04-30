# VoNat Tiko Mangroves

![VoNat Tiko Mangroves](../../assets/images/placeholder-project.png)

## Overview

Remote sensing analysis of the **Tiko Mangrove ecosystem in Cameroon**, conducted for **VoNat (Voice of Nature)**. The project uses satellite imagery and machine learning to assess mangrove degradation, identify conservation threats, and support conservation planning. The analysis combines multi-sensor data with automated change detection to produce a comprehensive threat assessment report.

**Client:** VoNat (Voice of Nature)  
**Study Area:** Tiko Mangrove, Cameroon  
**Duration:** September–November 2025  
**Role:** Lead Analyst  
**Status:** Report Complete — submitted to client  
**Repository:** [github.com/ulfboge/VoNat-Tiko-Mangroves](https://github.com/ulfboge/VoNat-Tiko-Mangroves)

---

## Methods & Tools

**Data Sources**

- Sentinel-2 multispectral imagery — mangrove extent and health
- Global Mangrove Watch (GMW v3) — mangrove baseline extent
- Hansen GFC — historical forest/mangrove loss
- Planet imagery (where available) — high-resolution change detection

**Processing Steps**

1. Establish baseline mangrove extent using GMW v3
2. Map current mangrove extent from Sentinel-2 classification
3. Identify degradation hotspots using change detection
4. Classify threat types (agriculture, urban expansion, aquaculture, etc.)
5. Produce threat maps and quantitative summary for the conservation report

**Tools Used**

| Tool | Purpose |
|------|---------|
| Google Earth Engine | Image classification and change detection |
| Python | Machine learning classification, area statistics |
| QGIS | Cartographic outputs and map layouts |

---

## Key Findings

- Mapped current mangrove extent and identified degraded zones
- Classified primary threat categories and their spatial distribution
- Delivered final conservation report with maps, ready for client submission

---

## Links

[View Code on GitHub](https://github.com/ulfboge/VoNat-Tiko-Mangroves){ .md-button }
