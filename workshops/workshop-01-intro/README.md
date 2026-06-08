---
title: INTRODUCTION TO QGIS WORKSHOP
nav_order: 1
parent: Workshops
---

# 1. INTRODUCTION TO QGIS WORKSHOP
## Guide to Nigeria Dam Overflow Example

This step-by-step guide for the hands-on project in Nigeria, part of the **Introduction to QGIS** workshop, offers a practical introduction to using QGIS for mapping and basic spatial analysis.

- [Full Abstract](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/Full%20Abstract%2010435437034480e9848afec63609e328.md)
- 😆 [Slides](https://docs.google.com/presentation/d/1753YZm_CWNk98tHKFKMmfDZaHaSLa1Af/edit?usp=drive_link&ouid=116103803223383670483&rtpof=true&sd=true)

---

## Before You Begin

Please complete the following before starting the workshop:

### 1. Install QGIS  
Follow the instructions in  
👉 [Downloading QGIS](https://app.notion.com/p/Downloading-installing-and-exploring-QGIS-interface-11a35437034480789ee4e4cc5c98131d?pvs=21)

![QGIS Interface](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image.png)

### 2. Download the Workshop Data  
💾 [Workshop DATA](https://drive.google.com/drive/folders/1Q037BIwtwuU3UU6mOhzNsvBzdSeWbzo0?usp=drive_link)

### 3. Keep the Server Link Open  
🔧 [Server Link](https://docs.google.com/document/d/18JXyJn1bmmtg2ynu70LxOIWgZ6D5ucMEX1is0lC_M9k/pub)

---

# STEP-BY-STEP GUIDE

---

## Step 2: Understanding the QGIS Interface

### a. Launch QGIS  
Open the QGIS application on your computer.

### b. Explore the Interface  
Key components:

- **Menu Bar** – access tools and functions  
- **Toolbars** – shortcuts to common tools  
- **Layers Panel** – manage data layers  
- **Map View** – main visualization area  
- **Status Bar** – CRS and map info  

![QGIS Interface](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/1_NewProject_Anno-2862822255.jpg)

### c. Add the Processing Toolbox  
- `View` → `Panels` → enable **Processing Tools**  
- Shortcut: **Ctrl + Alt + T** (Windows) / **Cmd + Alt + T** (macOS)

![Processing Toolbox](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%201.png)

---

## Step 3: Vector Data Display

### a. Download Vector Data  
For this workshop, download the pre‑selected shapefiles, unzip them, and save them in a reliable folder.

### b. Load Vector Data  
- `Layer` → `Add Layer` → `Add Vector Layer`  
- Browse to the `.shp` files  
- Load **political boundaries** and **rivers**

### c. Basic Display Controls  
- Toggle layer visibility  
- Pan and zoom  
- Rename layers  
- Change symbology  

![Zoom Tools](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%202.png)

Workshop task:  
- Political boundaries → white fill + black border  
- Rivers → blue  

---

## Step 4: Map Server Visualization

### a. Add XYZ Tiles  
- `Layer` → `Data Source Manager` → `XYZ Tiles`  
- Click **New**

![XYZ Tiles](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%203.png)

### b. Add Server URLs  
Examples:

| Product | URL |
|--------|-----|
| Google Maps | https://mt1.google.com/vt/lyrs=r&x={x}&y={y}&z={z} |
| Google Satellite | https://www.google.cn/maps/vt?lyrs=s@189&gl=cn&x={x}&y={y}&z={z} |
| Google Hybrid | https://mt1.google.com/vt/lyrs=y&x={x}&y={y}&z={z} |
| Google Terrain | https://mt1.google.com/vt/lyrs=t&x={x}&y={y}&z={z} |
| Google Roads | https://mt1.google.com/vt/lyrs=h&x={x}&y={y}&z={z} |
| OpenStreetMap | https://tile.openstreetmap.org/{z}/{x}/{y}.png |

Drag the tile layer into the map canvas.

---

## Step 5: Population Data (Raster)

Dataset:  
**GHS_BUILT_S_NRES_E2030_GLOBE_R2023A_54009_100_V1_0_R8_C20**

Meaning:

- Built‑up areas  
- Non‑residential estimates for 2030  
- Global coverage  
- Mollweide projection (EPSG:54009)  
- 100m resolution  

### a. Import Raster  
- `Layer` → `Add Raster Layer`  
- Load the dataset  
- Confirm CRS = **EPSG:54009**

Workshop task:  
- Use **Palette/Unique values**  
- Classify  
- Exclude 0  

![Raster Display](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%204.png)

---

## Step 6: Analyze Data

### a. Filter a Vector Layer  
- Duplicate the layer  
- Right‑click → **Filter**  
- Build SQL expression

Workshop task:  
- Filter **Nigeria** from political boundaries  

![Query Example](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%206.png)

### b. Select Feature by Value  
Workshop task:  
- Search for **ALAU** dam  

![Select Feature](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%207.png)

### c. Identify Location with OSM Search Plugin  
- Install **OSM Search** plugin  
- Search: *Maiduguri*, *Konduga*, *Alau Dam*

![OSM Search](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%209.png)

### d. Create a Shapefile  
- `Layer` → `Create Layer` → `New Shapefile Layer`  
- Geometry: point/line/polygon  
- CRS: **WGS 84**  
- Add attribute fields  

Workshop task:  
- Create shapefile **Alau Dam**

![New Shapefile](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%2010.png)

### e. Edit the Shapefile  
- Toggle Editing  
- Add features  
- Save edits  
- Style with star symbol + label  

![Label Example](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%2011.png)

![Satellite View](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%2012.png)

### f. Create a Buffer  
- Processing Toolbox → **Buffer**  
- Input: Dam shapefile  
- Distance: **25 km**  
- Dissolve: Yes  

![Buffer Tool](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%2013.png)

---

## Step 7: Create a Map

### a. Sketch Your Idea  
![Sketch](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%2014.png)

### b. Print Layout  
- Create new layout  
- Set paper  
- Add map  
- Lock layers  
- Add scale bar, north arrow, title, legend  

![Layout](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/image%2015.png)

---

## Step 8: Export Your Map

- `Layout` → Export as **Image**, **PDF**, or **SVG**  
- Choose resolution and save  
- Save the layout for future edits  

---

## Data Sources  
[Data sources](INTRODUCTION%20TO%20Q%20GIS%20WORKSHOP/Data%20sources%20e7c4a266321148f88d674bd84888412e.md)

