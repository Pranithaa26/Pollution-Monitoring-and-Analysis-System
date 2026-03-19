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

The main feature of this system is:

Water Quality Index (WQI) Visualization

The system:

1. Processes environmental parameters
2. Computes WQI values
3. Classifies river segments
4. Displays color-coded pollution levels on map

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

