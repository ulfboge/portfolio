# Geodata Pipeline Demo

![Geodata Pipeline Demo](../../assets/images/placeholder-project.png)

## Overview

An **automated geodata workflow** built with Python and GitHub Actions, demonstrating how to operationalize routine GIS processing tasks in a CI/CD pipeline. The pipeline reads geodata from a GeoPackage, calculates area in hectares, filters features by a configurable minimum area threshold, saves results to a new GeoPackage, and logs each run.

**Role:** Solo project  
**Status:** Live  
**Repository:** [github.com/ulfboge/geodata-pipeline-demo](https://github.com/ulfboge/geodata-pipeline-demo)

---

## What It Does

1. Reads feature data from a GeoPackage input
2. Calculates area in hectares for each feature
3. Filters features by a configurable minimum area threshold
4. Saves filtered results to a new GeoPackage
5. Logs each pipeline run (timestamp, feature count, filtered count)
6. Runs automatically on push via GitHub Actions

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Python / GeoPandas | Geodata reading, area calculation, filtering |
| GitHub Actions | Automated CI/CD pipeline trigger |
| GeoPackage (GPKG) | Input/output data format |

---

## Key Features

- Demonstrates geodata automation with open-source Python tools
- Configurable area threshold via environment variable
- Full run log for auditability
- GitHub Actions badge showing live pipeline status

---

## Links

[View Code on GitHub](https://github.com/ulfboge/geodata-pipeline-demo){ .md-button }
