# Miljögifter i svenska sjöar

![Miljögifter i svenska sjöar](../../assets/images/placeholder-project.png)

## Overview

An **interactive web map** visualizing the presence of environmental toxins in Swedish lakes. The map makes it easy to see which lakes are affected by substances such as PFAS, mercury (kvicksilver), PCB, and cadmium — and to what degree. Designed for use by the general public, journalists, and decision-makers.

**Study Area:** Sweden (national lake dataset)  
**Role:** Solo project  
**Status:** Live  
**Repository:** [github.com/ulfboge/miljogifter-500](https://github.com/ulfboge/miljogifter-500)

---

## Features

- **Clickable lake markers** — popup with lake name, county, contamination level, measured substances, and latest sampling date
- **Color-coded contamination levels** — green (low) / yellow (moderate) / red (high)
- **Substance filter** — select one or more substances (PFAS, Hg, PCB, Cd) with AND logic

---

## Methods & Tools

**Data Sources**

- Swedish environmental monitoring data — lake toxin measurements (PFAS, Hg, PCB, Cd)
- SLU/SMHI lake coordinate data

**Tools Used**

| Tool | Purpose |
|------|---------|
| Leaflet.js | Interactive map |
| JavaScript | Filter logic, popup rendering |
| HTML / CSS | Layout and styling |
| Python | Data preparation and GeoJSON export |

---

## Links

[View Code on GitHub](https://github.com/ulfboge/miljogifter-500){ .md-button }
