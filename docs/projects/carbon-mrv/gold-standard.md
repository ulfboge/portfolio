# Gold Standard MRV Pipeline

![Gold Standard MRV](../../assets/images/gold-standard-cover.png)

## Overview

A prototype MRV pipeline for projects seeking certification under the **Gold Standard for the Global Goals (GS4GG)**, with an initial focus on **Afforestation/Reforestation (A/R)** activities. The pipeline integrates field data collection via Mergin Maps with automated validation, spatial enrichment, and evidence reporting.

**Standard:** Gold Standard for the Global Goals (GS4GG) — A/R  
**Role:** Solo project  
**Status:** Prototype / In progress  
**Repository:** [github.com/ulfboge/gold-standard](https://github.com/ulfboge/gold-standard)

---

## Methods & Tools

**Pipeline Components**

**Field Data Pipeline (`field_pipeline/`)**

- Ingest incoming field GeoPackages and attachments from Mergin Maps into timestamped run folders
- Validate schema, geometry, and basic data-quality rules
- Enrich observations with context layers (admin boundaries, protected areas, land cover)
- Export to CSV/GeoJSON and generate Markdown reports for internal and external use

**MRV Validation (`mrv_validation/`)**

- Schema and rule set for validating MRV GeoPackages against a structured specification
- Automated checks aligned with GS4GG A/R MRV requirements

**Tools Used**

| Tool | Purpose |
|------|---------|
| Python / GeoPandas | Data ingestion, validation, spatial enrichment |
| QGIS | Map production and visual QA |
| Mergin Maps | Field data collection |
| GitHub Actions | Automated pipeline runs |

---

## Key Features

- End-to-end traceability from field observation to evidence report
- Timestamped run folders for full audit trail
- Configurable validation rules aligned with GS4GG requirements
- Automated Markdown reports suitable for project documentation

---

## Links

[View Code on GitHub](https://github.com/ulfboge/gold-standard){ .md-button }
