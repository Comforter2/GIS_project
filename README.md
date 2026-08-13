# GIS_project
# Assessing Spatial Variability of Soil Nutrients and Topographic Influences for Variable-Rate Fertilization in an Irrigated Corn Field

## Overview
This project evaluates whether a Variable Rate Application (VRA) fertilizer program is agronomically and economically justified for a 50-acre irrigated corn field in Georgia. Using ArcGIS Pro, soil chemistry, soil physical properties (electrical conductivity), and field topography were analyzed to determine the drivers of spatial yield variability and to generate site-specific management recommendations.

Course project completed for GEOG 6370 (University of Georgia).

## Objectives
1. Map soil chemical (pH, phosphorus, potassium) and corn yield variability using Inverse Distance Weighting (IDW) interpolation
2. Apply UGA fertilizer recommendation guidelines to classify soil chemistry into sub-optimal, optimal, and above-optimal zones
3. Identify "prescription polygons" where soil nutrient deficiencies overlap with below-average yield
4. Use 3D terrain visualization to assess whether micro-topography drives yield variability
5. Deliver a spatial management plan outlining targeted fertilizer and structural remediation zones

## Methods
- **Data processing:** Coordinate system standardization (NAD 1983 UTM Zone 16N), conversion of GeoJSON yield/ECa/elevation data to point features
- **Interpolation:** IDW interpolation (5m x 5m resolution) for soil pH, phosphorus, potassium, yield, elevation, and ECa
- **Smoothing:** Focal Statistics (7x7 window) to reduce noise in yield, elevation, and ECa surfaces
- **Reclassification:** UGA soil test sufficiency guidelines applied to define chemical management zones
- **Vector analysis:** Raster-to-polygon conversion, clipping, and intersect overlays to identify VRA target zones
- **3D visualization:** Yield polygons draped over a digital elevation model to assess topographic influence

## Key Findings
- Soil pH and phosphorus were non-limiting across nearly the entire field — no variable-rate lime or phosphorus application is agronomically justified
- A localized zone of medium potassium levels overlapping with below-average yield was identified as a targeted, cost-effective candidate for variable-rate potassium application
- The dominant driver of the yield gap was not nutrient deficiency but topography and soil texture: a central sandy ridge (low ECa, high elevation) corresponded closely with below-average yield due to poor water retention
- Recommended management strategy: targeted variable-rate potassium in deficient zones, combined with variable-rate irrigation and drainage improvements in the topographically limited areas, rather than a uniform fertilizer program

## Tools
ArcGIS Pro (Spatial Analyst, Interpolation, Reclassify, Overlay, 3D Scene tools)

## Data
Field data (soil grid samples, yield monitor records, ECa, elevation) was provided as part of coursework at the University of Georgia and is not included in this repository. Only the analysis workflow, code/documentation, and exported map outputs are shared here.

