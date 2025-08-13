# Let's create the updated README.md file with the provided content

readme_content = """# Sentinel2_Snow_Monitoring 🌨️

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
