# Urban Heat Island & Equity Analysis
A geospatial decision-support project that identifies neighborhoods in Washington, DC most vulnerable to extreme urban heat. The workflow integrates satellite-derived land surface temperature, tree canopy, impervious surface, and ACS demographic data to support environmental equity analysis and planning decisions.

## Project Overview
Urban heat affects neighborhoods unevenly. Areas with high impervious surface, low tree canopy, and greater socioeconomic vulnerability often experience stronger heat exposure and fewer adaptive resources [file:1]. This project combines remote sensing, census data, spatial databases, ETL automation, and GIS analysis to build a reproducible heat vulnerability workflow for Washington, DC.

The final deliverable is designed to support city planners, public health officials, emergency management agencies, and environmental equity initiatives.

## Objectives
- Map land surface temperature across Washington, DC, using Landsat data.
- Incorporate census tract-level socioeconomic variables from ACS.
- Use NLCD impervious surface data and tree canopy metrics to represent built-environment and vegetation conditions.
- Build a PostgreSQL/PostGIS database to organize and manage spatial data.
- Automate extraction, transformation, and loading with Python scripts.
- Produce an ArcGIS Dashboard and portfolio-ready documentation.
  
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

## Datasets
### USGS Landsat 8-9 Collection 2 Level-2
- Source: U.S. Geological Survey
- Geography: Washington, DC scene coverage
- Fields: surface temperature, surface reflectance, cloud mask, and related thermal bands.
- Used for: land surface temperature and urban heat exposure analysis.

### U.S. Census Bureau ACS 5-year estimates
- Source: U.S. Census Bureau
- Geography: Census tracts in Washington, DC
- Fields: median income, poverty rate, age 65+, and population density.
- Used for: socioeconomic vulnerability analysis.

### USGS NLCD Fractional Impervious Surface
- Source: U.S. Geological Survey.
- Geography: Washington, DC land cover coverage.
- Fields: impervious surface percentage and built-environment context.
- Used for: built environment and heat retention analysis.

## Risk Modeling Approach

The project creates a vulnerability score by combining standardized variables related to heat exposure and social sensitivity [file:1]. Core inputs include:

- Heat intensity.
- Low tree canopy.
- Population density.
- Income vulnerability.
- Elderly population.

A weighted scoring model is used to produce a final heat vulnerability layer that classifies areas into low, moderate, and high risk [file:1].

## Deliverables

- PostgreSQL/PostGIS spatial database.
- Python ETL workflow.
- ArcGIS Pro spatial analysis outputs.
- ArcGIS Dashboard.
- Professional GitHub repository and README documentation.

## Results

The analysis identifies areas where high surface temperature overlaps with low canopy coverage, high impervious surface, and greater socioeconomic vulnerability [file:1]. These outputs can help prioritize mitigation strategies such as urban tree planting, cooling interventions, and equity-focused resource allocation [file:1].

## Results
(Add screenshots later)

## Future Improvements
- Real-time weather integration
- Predictive heat modeling
