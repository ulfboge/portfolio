# Soil Carbon Modeling

![Soil Carbon Modeling](../../assets/images/soil-carbon-distribution-visual.png)

## Overview

Scripts and notebooks for processing geospatial data required for **soil carbon modeling** in carbon projects. The workflow leverages Google Earth Engine to extract and analyze climate, soil, vegetation, and land cover data for any specified Area of Interest — enabling scalable carbon stock quantification for nature-based solutions projects.

**Application:** Carbon project soil carbon baseline  
**Role:** Solo project  
**Status:** Completed  
**Repository:** [github.com/ulfboge/soil-carbon-modeling](https://github.com/ulfboge/soil-carbon-modeling)

---

## Methods & Tools

**Data Sources**

- GRIDMET — daily climate data (temperature, precipitation, etc.)
- SoilGrids — global soil property maps (SOC, bulk density, clay content)
- MODIS — vegetation indices and land cover time series
- Custom AOI shapefiles

**Processing Steps**

1. Define Area of Interest and export boundary
2. Extract climate variables from GRIDMET within AOI
3. Pull SoilGrids layers (SOC stock, depth profiles)
4. Extract MODIS NDVI and land cover time series
5. Compile multi-source dataset for modeling
6. Visualize and validate in Jupyter notebooks

**Tools Used**

| Tool | Purpose |
|------|---------|
| Google Earth Engine | Large-scale data extraction |
| Python / Pandas / NumPy | Data processing and analysis |
| Jupyter Notebooks | Interactive analysis and visualization |
| QGIS | Spatial validation and map output |

---

## Key Features

- Automated extraction of multiple datasets for any global AOI
- Reproducible pipeline from raw GEE export to analysis-ready tables
- Jupyter notebooks for interactive exploration and quality control
- Documented workflow aligned with carbon project methodologies

---

## Links

[View Code on GitHub](https://github.com/ulfboge/soil-carbon-modeling){ .md-button }
