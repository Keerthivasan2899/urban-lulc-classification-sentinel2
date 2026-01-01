# Urban Land Use / Land Cover Classification using Sentinel-2 and Random Forest

## 📌 Project Summary
This project implements an end-to-end **urban Land Use / Land Cover (LULC) classification workflow** using **Sentinel-2 multispectral satellite imagery** and a **Random Forest supervised machine learning classifier**.

The objective is to accurately classify major urban land cover categories to support **urban planning, environmental monitoring, and geospatial analysis**.

The workflow integrates:
- GIS-based preprocessing (QGIS)
- Pixel-level spectral feature extraction
- Supervised machine learning using Python

---

## 🗺️ Study Area
**Tiruchirappalli (Trichy), Tamil Nadu, India**  
Coordinate Reference System (CRS): **EPSG:32644 (WGS 84 / UTM Zone 44N)**

---

## 📊 Final LULC Classification Output
![LULC Classification Map](outputs/lulc_rf_trichy_2025.png)

---

## 🛰️ Data Used

- **Satellite:** Sentinel-2 MSI Level-2A (Surface Reflectance)
- **Data Source:** ESA Copernicus
- **Acquisition Date:** March 13, 2025
- **Spatial Resolution:** 10 m
- **Spectral Bands Used:**
  - B02 (Blue)
  - B03 (Green)
  - B04 (Red)
  - B08 (Near Infrared)

> Raw Sentinel-2 data is not included in this repository due to file size constraints.  
> The repository focuses on workflow reproducibility and analytical outputs.

---

## ⚙️ Methodology

1. Sentinel-2 imagery was mosaicked, reprojected, and clipped to the study area using **QGIS (LTR)**.
2. Training polygons representing major LULC classes were manually digitized.
3. Pixel-level spectral features were extracted from the multispectral bands.
4. A **Random Forest classifier** was trained using Python (`scikit-learn`).
5. The trained model was applied to classify the full raster dataset.
6. Final classified maps were styled and exported using **QGIS Print Layout**.

This workflow follows standard practices for regional-scale urban LULC classification using satellite data.

---

## 🧰 Tools & Technologies

- **GIS:** QGIS (Long Term Release)
- **Programming Language:** Python 3.x
- **Machine Learning:** Random Forest (scikit-learn)
- **Geospatial Libraries:** rasterio, geopandas, numpy, pandas
- **Visualization & Mapping:** QGIS Print Layout
- **Version Control:** GitHub

---

## 📈 Results & Interpretation

- **Overall classification accuracy:** ~83%
- Vegetation and water classes achieved high accuracy due to strong spectral separability.
- Some confusion was observed between built-up and barren land classes, which is expected at 10 m spatial resolution in urban environments.
- The final classified output is suitable for **urban analysis, land monitoring, and planning-oriented GIS workflows**.

---

## 🎯 Skills Demonstrated

- Urban Land Use / Land Cover classification
- Sentinel-2 multispectral data processing
- Supervised machine learning for geospatial analysis
- Training data preparation and feature extraction
- Accuracy assessment and result interpretation
- Professional cartographic map production
- Reproducible and well-structured GIS project documentation
