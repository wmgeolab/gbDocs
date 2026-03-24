# Digitizing

**Digitizing** is the process of converting features from an image into digital vector data (a polygon).

If an acceptable licensed shapefile is not found, follow these steps:

## Digitizing Steps

**Finding an Image to Georeference**  
To start digitizing, find an image with the boundary you need. Common options:

- **Wikimedia** – check the license.  
- **Google Images** – ensure the source license is acceptable.  

**Georeferencing the Image**

1. Open **ArcGIS Pro** or **QGIS**, create a **Blank Map**.  
2. Name the project the respective countries' ISO code and ADM level, `ISO_ADM#`.  
3. Add the image:
   - Click **Add Data → Data** (or open the **Map** tab).  
   - Navigate to the folder with the image and select it.  
   - The image may appear in the middle of the ocean — this is normal.  
4. Go to **Imagery → Georeference**. Tools to use: **Fit to Display**, **Move**, **Scale**, **Rotate**.

**Adding Control Points**

- Click **Add Control Points** in the Georeference tab.  
- Click a point on the image and align it with the basemap.  
- Repeat along the border.  
- Tip: Make the image **partially transparent** to align more easily.  
- After adding points: **Transformation → Adjust → Save → Close Georeference**.

**Digitizing the Boundary**

- Open **Catalog Pane → Folders** dropdown.  
- Right-click your project folder → **New → Shapefile**.  
  - Feature Class Name  
  - Geometry Type (Polygon / Polyline)  
  - Coordinate System: `WGS 1984`  
- Edit tab → **Create → select feature → trace along boundary**.  
- Double-click to close polygon.  
- For neighboring polygons → use **Trace Tool**.

**Saving Your Work**

- Click **Save** in Edit tab.  

---
