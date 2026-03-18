Narmada Basin Pollution Monitoring and Analysis System

---

Project Overview

This project is a Geospatial Web-Based Pollution Monitoring System developed for the Narmada River Basin.

Core Objective

To analyze water quality and generate color-coded pollution maps using the Water Quality Index (WQI).

The system integrates:

- GIS visualization
- Raster data processing
- Climate & streamflow analysis
- Web-based interactive mapping

---

Core Feature: WQI-Based Pollution Analysis

The main feature of this system is:

Water Quality Index (WQI) Visualization

The system:

1. Processes environmental parameters
2. Computes WQI values
3. Classifies river segments
4. Displays color-coded pollution levels on map

WQI Classification

WQI Range| Category| Color
0–25| Excellent| 🟢 Green
26–50| Good| 🟡 Yellow
51–75| Poor| 🟠 Orange
76–100| Very Poor| 🔴 Red

Final output: Interactive pollution map showing river health

---

System Design Summary

🔹 Use Case

- User Authentication
- View GIS layers
- Generate rasters
- Pollution analysis (WQI)
- District statistics

🔹 Key Modules

- User (Admin / Contributor / Viewer)
- Raster Processing
- Spatial Layer Management
- WQI Prediction Module
- District Statistics Module

🔹 Workflow

1. Upload spatial & parameter data
2. Generate raster layers
3. Compute WQI
4. Classify pollution
5. Visualize results on map

---

🌐 Website Features

GIS Visualization

- State & district boundaries
- Narmada basin polygon
- River network & centerline
- HQ locations & towns
- Interactive popups

---

Raster Processing

- Clip raster (backend)
- Load GeoTIFF on map
- Toggle raster visibility

---

Pollution Analysis

- WQI calculation
- Color-coded river segments
- Identification of polluted areas

---

District Analysis

- Rivers per district
- Climate statistics (temperature & precipitation)

---

Technologies Used

🔹 Frontend

- HTML, CSS, JavaScript
- Leaflet.js
- GeoRaster

🔹 Backend

- Flask (Python)
- GeoPandas
- Rasterio
- Shapely

🔹 Data Processing

- Pandas
- NumPy
- SciPy

---

📁 Project Structure

project/
│
├── index.html
├── rivers.html
├── app.py
├── raster_clip.py
│
├── geojson/
│   ├── state_boundary.geojson
│   ├── district_boundary.geojson
│   ├── narmada.geojson
│   ├── narmada_named_network.geojson
│   ├── narmada_centerline.geojson
│
├── rasters/
│   ├── precip_clipped.tif
│   ├── temperature.tif
│
├── scripts/
│   ├── create_streamflow_monthly.py
│   ├── streamflow_monthly_rasters.py
│
├── docs/
│   ├── Pollution Monitoring and Analysis.pdf
│
├── requirements.txt
└── README.md

---

⚙️ Requirements

Create a file named requirements.txt with:

flask
pandas
geopandas
numpy
rasterio
shapely
scipy
tqdm
openpyxl

---

Installation

🔹 Step 1: Install Python

Install Python 3.8 or higher

---

🔹 Step 2: Install Dependencies

pip install -r requirements.txt

---

🔹 Optional (Full GIS Support)

pip install geopandas[all]

---

How to Run the Project

🔹 Step 1: Download Project

- Clone repository OR download ZIP
- Extract files

---

🔹 Step 2: Open Terminal

cd software_project

---

🔹 Step 3: Start Backend Server

python app.py

Expected output:

Running on http://127.0.0.1:5000

---

🔹 Step 4: Open Website

Open browser:

http://127.0.0.1:5000

---

🌐 How to Use the Website

🔹 1. Load Map

- Opens Narmada basin map
- Default layers visible

---

🔹 2. Toggle Layers

- Use layer control
- Enable/disable GIS layers

---

🔹 3. View Attributes

- Click on map features
- Popups display details

---

🔹 4. Clip Raster

Steps:

1. Click "Clip Raster"
2. Backend processes raster
3. Raster appears on map

---

🔹 5. Show / Hide Raster

- Use checkbox "Show Layer"

---

🔹 6. Rivers per District

- Open menu → rivers page
- View river counts

---

🔹 7. Climate Analysis

- Backend computes:
  - Mean temperature
  - Mean precipitation

---

GIS Details

- CRS: EPSG:4326 (Web)
- Raster CRS: EPSG:32644
- Pixel Size: 30m
- Method: IDW + Raster Clipping

---

⚠️ Important Notes

- Backend must be running
- File paths must be correct
- Large rasters may take time
- Internet required for map libraries

---

 Future Enhancements

- User authentication system
- PostGIS database integration
- Real-time data updates
- Advanced WQI prediction models

---

Team Members

- Ansh Jain
- Komma Pranitha
- Deshagani Chennakeshava
- Nitin
- Lakhani Prayag

---

Conclusion

This project provides a complete GIS-based pollution monitoring system, focused on:

 Water Quality Index (WQI) based pollution analysis

It enables:

- Identification of polluted river segments
- Spatial visualization of pollution
- Data-driven environmental decision making

The final output is an interactive color-coded pollution map of the Narmada basin.

—
