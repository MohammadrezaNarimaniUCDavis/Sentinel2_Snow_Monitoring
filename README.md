# Sentinel2_Snow_Monitoring 🌨️

**A reproducible workflow for interactive snow-cover monitoring using Sentinel-2 imagery, Google Earth Engine, and open-source geospatial tools.**

---

## Poster Showcase 🎯

Click the image below to view the **full high-resolution PDF** of the project poster.

[![Project Poster](https://github.com/MohammadrezaNarimaniUCDavis/Sentinel2_Snow_Monitoring/blob/main/Poster/Showcase_Poster/ESEARCH_Summer_2025.png)](https://github.com/MohammadrezaNarimaniUCDavis/Sentinel2_Snow_Monitoring/blob/main/Poster/Showcase_Poster/ESEARCH_Summer_2025.pdf)

---

## ✨ Features

- **Interactive ROI selection**  
  Draw square sampling windows (512×512 pixels) directly on a Sentinel-2 map notebook.
- **Auto-save ROIs**  
  Each region is saved as a shapefile with center coordinates, acquisition date, and geometry.
- **Batch Sentinel-2 download**  
  Automatically fetches the first 12 bands (B1–B12, excluding B10) for each ROI and acquisition date, clipped to the drawn window.
- **Visualization**  
  Display downloaded TIFFs and ROI boundaries on an interactive map within your notebook.
- **Cloud, snow, and date handling**  
  Seamlessly filters imagery based on cloud and snow coverage, and handles date selection logic.

---

## 🧭 Use Cases

- Snow cover monitoring over Lake Tahoe or similar regions  
- Sentinel-2 time-series analysis of surface reflectance  
- Remote sensing applications in hydrology, climate, agriculture, and environmental studies

---

## 🚀 Quick Start

1. **Clone the repo**  
   ```bash
   git clone https://github.com/MohammadrezaNarimaniUCDavis/Sentinel2_Snow_Monitoring.git
   cd Sentinel2_Snow_Monitoring
   ```

2. **Set up your environment** (recommended: Conda)  
   ```bash
   conda env create -f environment.yml
   conda activate gee
   ```
   Or install manually:  
   ```bash
   conda install -c conda-forge geemap geopandas rasterio gdal pyproj shapely fiona localtileserver
   pip install earthengine-api
   ```

3. **Run the main Jupyter notebook**  
   It guides you through:
   - Authenticating with Google Earth Engine  
   - Drawing ROIs on an interactive Sentinel-2 map  
   - Exporting ROI shapefiles  
   - Downloading Sentinel-2 imagery for selected regions/dates  
   - Visualizing the results

---

## 📁 Folder Structure

```
Sentinel2_Snow_Monitoring/
├── Python_Code/
│   └── S2_Download/             ← Jupyter and Python code for main workflow
├── SHP/                         ← Auto-created folder with ROI shapefiles
├── Sentinel2_Square_Exports/    ← Auto-created TIFF files for downloaded imagery
├── Poster/
│   └── Showcase_Poster/         ← PNG and PDF of the project poster
└── README.md
```

---

## ⚠️ Notes

- Sentinel-2 Band 10 is excluded as per ESA specifications.  
- Compatible across Linux, macOS, and Windows – best results in a Conda-based setup.  
- If you run into errors with PROJ, GDAL, or rasterio, ensure all geospatial dependencies are synced via conda-forge.

---

## 📚 References

- Sentinel-2 Data Documentation  
- Google Earth Engine Python API  
- geemap Python documentation  

---

## 👤 Author & Contribution

Created by **Mohammadreza Narimani**, University of California, Davis, Digital Agriculture Lab.  
Pull requests and feedback are welcome!
