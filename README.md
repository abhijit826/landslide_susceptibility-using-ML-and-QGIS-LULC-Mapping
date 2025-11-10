# 🗺️ Nigulsari Landslide Susceptibility Mapping – Himachal Pradesh (QGIS)
![Landlide Whole-](https://github.com/user-attachments/assets/d2ac52b1-83fe-45df-814b-b2640293c5ed)
## 📖 Overview
This repository presents the **Nigulsari Landslide Susceptibility Mapping Project**, conducted in **Kinnaur District, Himachal Pradesh, India**.  
The project integrates **OpenStreetMap (QuickOSM)** data, **QGIS terrain analysis**, and the **Slope-based SZ Plugin** for assessing landslide susceptibility.


The workflow demonstrates how to:
- Define a **study area boundary** using OSM and manual digitization,
- Prepare essential **topographic and environmental layers**, and
- Generate a **Landslide Susceptibility Map** using the **SZ Plugin** in QGIS.

---

## 🌍 Study Area
- **Location:** Nigulsari, Kinnaur District, Himachal Pradesh, India  
- **Coordinates:** ~31.558° N, 77.946° E  
- **Key features:** NH-5 Highway, Satluj River valley, and the 2021 Nigulsari landslide.  
- **Elevation range:** ~1400–2400 m  

The area is characterized by steep terrain, deeply incised valleys, and high precipitation, making it prone to frequent slope failures.

---

## 🧰 Tools & Plugins

| Tool / Plugin | Purpose |
|----------------|----------|
| **QGIS (v3.30+)** | Base GIS environment |
| **QuickOSM** | Extracts roads, rivers, and forest data from OpenStreetMap |
| **QuickMapServices** | Adds satellite or OSM basemaps |
| **SZ Plugin** | Slope Unit–based Landslide Susceptibility Mapping |
| **DEM Data (SRTM / CartoDEM)** | Derivation of slope, aspect, and elevation |
| **Google Earth Pro** | Landslide inventory mapping using time slider |

---

## 📦 Datasets Used

### 1️⃣ Landslide Inventories  
- Digitized from **Google Earth** using **Time Slider** to identify landslide locations.  
- Exported as **KML/KMZ**, then imported to QGIS and saved as a shapefile.

### 2️⃣ Topographic Layers  
Derived from DEM:
- **Elevation**
- **Slope**
- **Aspect**

### 3️⃣ Environmental Layers  
- **Precipitation**
- **NDVI (Normalized Difference Vegetation Index)** – computed from satellite imagery.


---

## 🧭 Workflow / Methodology

### Step 1: Define Study Area
1. Locate **Nigulsari** in QGIS (using Google Satellite basemap).  
2. Create a new polygon shapefile:  
   - Geometry: **Polygon**  
   - CRS: **EPSG:32643 (WGS 84 / UTM Zone 43N)**  
3. Digitize around the landslide slope, NH5, and Satluj River valley.

---


### Step 2: Prepare Intermediate Layers
Using **Raster → Analysis Tools** in QGIS:
- Generate **Slope**, **Aspect**, and **Elevation** maps from DEM.  
- Compute **NDVI** using multispectral imagery (Sentinel-2 or Landsat).  
- Integrate **precipitation raster** (if available).

---

### Step 3: Install and Use SZ Plugin
1. Go to `Plugins → Manage and Install Plugins → Search “SZ”`.  
2. Install the **SZ Plugin** for landslide susceptibility analysis.  
3. Inputs required:
   - Slope Units (derived from DEM)
   - Elevation, Slope, Aspect, NDVI, Precipitation
   - Landslide Inventory (training points)
4. Run the **Landslide Susceptibility Model** → output susceptibility index.

---

## 📊 Outputs
- **Study Area Boundary Map** (from QuickOSM + Manual Polygon)
- **Slope Unit Map**
- **Elevation / Aspect / Slope Maps**
- **NDVI and Rainfall Layers**
- **Final Landslide Susceptibility Map (SZ Plugin Output)**

---



