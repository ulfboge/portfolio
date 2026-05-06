# Skogsmonitor – GEE App Demo

![Skogsmonitor GEE Demo](../../assets/images/skogsmonitor-gee-demo.png)

## Overview

A **Google Earth Engine (GEE) App** demonstrating how satellite data can be used to monitor forest change over time in Sweden. Designed for environmental NGOs and non-profit use, the app makes NDVI-based change detection transparent and pedagogically accessible without requiring technical GIS skills.

**Study Area:** Sweden (administrative boundaries or user-drawn polygons)  
**Role:** Solo project  
**Status:** Live demo  
**Repository:** [github.com/ulfboge/skogsmonitor-gee-demo](https://github.com/ulfboge/skogsmonitor-gee-demo)

---

## Methods & Tools

**How It Works**

Users select an area (administrative boundary or drawn polygon) and choose two time periods (A and B) to explore:

- NDVI for period A and period B
- ΔNDVI — change between periods
- A change mask — areas below a configurable detection threshold
- Affected area in hectares
- Click-to-inspect: NDVI A, NDVI B, and ΔNDVI values at any map location

**Data Sources**

- Sentinel-2 MSI — multispectral imagery (10–20 m resolution)
- Swedish administrative boundaries (SCB/Lantmäteriet)

**Tools Used**

| Tool | Purpose |
|------|---------|
| Google Earth Engine | Image compositing, NDVI calculation, UI |
| JavaScript (GEE API) | App logic and interactive interface |

---

## Key Features

- No GIS skills required — designed for NGO non-technical users
- Configurable NDVI change threshold
- Area statistics in hectares
- Click-to-inspect values at any point

---

## Links

[View Code on GitHub](https://github.com/ulfboge/skogsmonitor-gee-demo){ .md-button }
