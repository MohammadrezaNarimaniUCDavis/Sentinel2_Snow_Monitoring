# Sentinel2_Snow_Monitoring

A reproducible workflow and toolkit for **interactive snow monitoring and Sentinel-2 data download** using Python, Google Earth Engine, and open-source geospatial libraries.

---

## ✨ Features

- **Interactive ROI selection:** Click on a Sentinel-2 image map to create square sampling windows (512×512 pixels).
- **Auto-save ROIs:** Each region is saved with center coordinates, acquisition date, and geometry as a shapefile.
- **Batch Sentinel-2 download:** Automatically downloads the first 12 bands (B1–B12, excluding B10) for each ROI and date, clipped to each drawn square.
- **Visualization:** Display your exported TIFFs and ROI boundaries on an interactive map inside your notebook.
- **Handles cloud, snow, and image date selection transparently.**

---

## 🛰️ Use Cases

- Monitoring snow cover over Lake Tahoe or other regions
- Time series analysis of Sentinel-2 surface reflectance
- Remote sensing for hydrology, climate, or agriculture

---

## 🚀 Quick Start

1. **Clone the repo:**
    ```bash
    git clone https://github.com/MohammadrezaNarimaniUCDavis/Sentinel2_Snow_Monitoring.git
    cd Sentinel2_Snow_Monitoring
    ```

2. **Set up your environment:**  
   (Recommended: use Anaconda/Miniconda)
    ```bash
    conda env create -f environment.yml
    conda activate gee
    ```

    Or manually install dependencies:
    ```
    conda install -c conda-forge geemap geopandas rasterio gdal pyproj shapely fiona localtileserver
    pip install earthengine-api
    ```

3. **Run the main Jupyter notebook:**  
   The workflow will prompt you for project paths and walk you through:
   - Authenticating Google Earth Engine
   - Drawing ROIs on a Sentinel-2 map
   - Exporting ROI shapefiles
   - Downloading Sentinel-2 imagery for each region/date
   - Visualizing results

---

## 📁 Folder Structure

- `Python_Code/S2_Download/` – Main Python and notebook files for the workflow
- `SHP/` – (Auto-created) ROI shapefiles
- `Sentinel2_Square_Exports/` – (Auto-created) Downloaded Sentinel-2 TIFF files
- `README.md` – This file

---

## 📝 Notes

- Only valid Sentinel-2 bands are downloaded (no B10).
- All tools run cross-platform (Linux/Mac/Windows), but full compatibility is ensured in Conda environments.
- If you encounter PROJ/GDAL/rasterio errors, update all geospatial dependencies with conda-forge.

---

## 📚 References

- [Sentinel-2 Data Documentation](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR_HARMONIZED)
- [Google Earth Engine Python API](https://developers.google.com/earth-engine/python_install)
- [geemap documentation](https://geemap.org/)

---

## 👤 Author

- **Mohammadreza Narimani, UC Davis**

---

*Pull requests and improvements welcome!*
