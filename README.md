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
- USGS Landsat
- U.S. Census ACS
- NLCD Land Cover

## 📡 Data Acquisition Status

### ✅ Task 4 Complete: Landsat Surface Temperature
**Scene**: `LC09_L2SP_015033_20260503_20260504_02_T1` (Landsat 9 C2 L2)
**Location**: Path 15 / Row 33 (Washington, DC)
**Acquisition**: May 3, 2026 (early summer baseline)
**Files**: Level-2 Surface Reflectance (13 files) + Surface Temperature (14 files)
**Key Layer**: `ST_B10.TIF` (30m surface temperature, Kelvin)
**Source**: [USGS EarthExplorer](https://earthexplorer.usgs.gov)
**Storage**: `data/raw/temperature/` *(local - excluded from Git)*

**Quick Stats**:
Resolution: 30m (UTM Zone 18N)
Size: ~1GB
Cloud Cover: <10%
Temp Range: 290-320K (17-47°C urban heat)

## Results
(Add screenshots later)

## Future Improvements
- Real-time weather integration
- Predictive heat modeling
