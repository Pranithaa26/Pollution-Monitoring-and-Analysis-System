Pollution Monitoring and Analysis System

(Narmada Basin GIS Web Application)

---

1. Project Structure

The project is organized as follows:

project/
│
├── app.py                  # Main Flask backend server
├── interpolation.py       # Raster interpolation (IDW)
├── raster_clip.py         # Raster clipping logic
├── perdistrict.py         # District-wise statistics
│
├── template/              # Frontend (HTML + JS)
│   ├── index.html
│   ├── index1.html
│   ├── rivers.html
│   ├── district_climate.html
│   └── rivers.js
│
├── data/
│   ├── csv/               # Input CSV data
│   ├── geojson/           # GeoJSON layers
│   ├── shp/               # Shapefiles
│   └── raster/            # Raster files (.tif)
│
└── __pycache__/           # Auto-generated (ignore)

---

2. Software Requirements

---

2.1 Install Python

- Python 3.8 or above
- Download: https://www.python.org

---

2.2 Install Required Libraries

Run:

pip install flask pandas geopandas numpy rasterio shapely scipy tqdm openpyxl

---

2.3 Recommended GIS Support

pip install geopandas[all]

---

2.4 Browser

- Google Chrome (Recommended)

---

2.5 Internet

Required for:

- Leaflet.js
- GeoRaster visualization

---

3.  Running the Project

---

Step 1: Open Terminal

Navigate to project folder:

cd project

---

Step 2: Run Backend

python app.py

---

Step 3: Open Website

Go to:

http://127.0.0.1:5000

---

4. 🌐 Website Features

---

4.1 GIS Map Visualization

The system displays:

- State boundary
- District boundaries
- Narmada basin
- River network
- Centerline
- Towns and HQ

Users can:

- Zoom / Pan
- Click features to view details

---

4.2 Layer Control

Users can:

- Enable/disable layers
- Overlay multiple GIS layers
- Customize map view

---

4.3  Raster Processing

---

▶ Clip Raster

Steps:

1. Click “Clip Raster” button
2. Backend processes raster using:
   - "raster_clip.py"
3. Clipped raster ("precip_clipped.tif") is generated
4. Raster is displayed on map

---

4.4 Toggle Raster Visibility

- Checkbox: Show Layer

✔ Checked → Raster visible
❌ Unchecked → Raster hidden

---

4.5 District Climate Analysis

From "district_climate.html"

Users can view:

- Mean precipitation
- Mean temperature
- District-wise climate data

---

4.6  Rivers per District

From "rivers.html"

Steps:

1. Open menu (☰)
2. Click River Tributaries per District

Displays:

- District name
- River count
- River names

---

5.  Backend Modules

---

🔹 app.py

- Main Flask server
- Handles API requests
- Connects frontend and backend

---

🔹 raster_clip.py

- Clips raster using basin boundary
- Generates "precip_clipped.tif"

---

🔹 interpolation.py

- Performs IDW interpolation
- Creates raster surfaces

---

🔹 perdistrict.py

- Calculates district-wise statistics
- River counts and climate values

---

6.  Data Files

---

data/csv/

- Input environmental data

---

data/geojson/

- GIS layers used in map

---

data/shp/

- Shapefiles for spatial analysis

---

data/raster/

Contains:

- "2011_2023_Precipitation.tif"
- "2011_2023_Mean_Temperature.tif"
- "precip_clipped.tif"

---

7.  Important Notes

---

Processing Time

- Raster clipping and analysis may take time
- Depends on:
  - Data size
  - System performance

⚠ Do NOT refresh during processing

---

8. Troubleshooting

---

Website not opening

✔ Ensure Flask server is running

---

Raster not showing

✔ Click “Clip Raster” first
✔ Wait for processing

---

Map not loading

✔ Check internet connection

---

9. User Capabilities

Users can:

- View GIS layers
- Toggle layers
- Generate raster outputs
- Analyze pollution using WQI
- View district climate data
- View rivers per district

---

10. Team Members

- Ansh Jain
- Komma Pranitha
- Deshagani Chennakeshava
- Nitin
- Lakhani Prayag

—
