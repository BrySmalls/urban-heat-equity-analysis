# Urban Heat Island & Equity Analysis

## Project Overview
This project identifies neighborhoods most vulnerable to extreme urban heat using geospatial analysis, demographic data, and environmental variables.

## Objectives
- Identify high-risk neighborhoods
- Analyze environmental equity
- Support urban planning decisions

## Tech Stack
- ArcGIS Pro
- PostgreSQL/PostGIS
- Python
- ArcGIS Dashboards
- Git/GitHub

## Workflow
Data → ETL → PostGIS → Spatial Analysis → Dashboard

## Datasets
### USGS Landsat 8-9 Collection 2 Level-2
- Source: U.S. Geological Survey
- Geography: Washington, DC scene coverage
- Fields: surface temperature, surface reflectance, cloud mask, and related thermal bands
- Used for: urban heat exposure layer and land surface temperature analysis

### U.S. Census Bureau ACS 5-year estimates
- Source: U.S. Census Bureau
- Geography: Census tracts in Washington, DC
- Fields: median income, poverty rate, age 65+, population density
- Used for: socioeconomic vulnerability layer

### USGS NLCD Fractional Impervious Surface
- Source: U.S. Geological Survey.
- Geography: Washington, DC land cover coverage.
- Fields: impervious surface percentage and built-environment context.
- Used for: built environment and heat retention analysis.

## 📡 Data Acquisition Status
### Landsat Surface Temperature
- Scene: `LC09_L2SP_015033_20260503_20260504_02_T1` (Landsat 9 C2 L2)
- Location: Path 15 / Row 33 (Washington, DC)
- Acquisition: May 3, 2026
- Files: Level-2 Surface Reflectance (13 files) + Surface Temperature (14 files)
- Key layer: `ST_B10.TIF` (30m surface temperature, Kelvin)
- Source: [USGS EarthExplorer](https://earthexplorer.usgs.gov/)
- Storage: `data/raw/temperature/` *(local, excluded from Git)*
- Quick stats: Resolution 30m, UTM Zone 18N, cloud cover <10%


## Results
(Add screenshots later)

## Future Improvements
- Real-time weather integration
- Predictive heat modeling
