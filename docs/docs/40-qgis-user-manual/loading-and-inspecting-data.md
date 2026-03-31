# Loading and Inspecting Data

Once the data has been downloaded following the steps in the [Downloading Data page](https://wmgeolab.github.io/gbDocs/30-data-acquisition/downloading-data/), the next step is to load it into QGIS and verify that it is correct.

---

## Loading the Data

1. Open **QGIS**.
2. Drag and drop the GeoJSON file into the QGIS window.

<img width="913" height="348" alt="Drag_Drop" src="https://github.com/user-attachments/assets/6aa740c1-e08d-4c4d-aa35-dc76f491fbaa" />

3. Click **Add Layers** when prompted.

<img width="434" height="267" alt="add_layers" src="https://github.com/user-attachments/assets/67a0d8e8-f976-4a33-bca7-fc3b6005b133" />

4. The selected boundary should now appear in the map window.
   `USA_ADM1` is listed as an example.

<img width="821" height="484" alt="USA_example" src="https://github.com/user-attachments/assets/066c3749-93bc-4773-872f-85550baad40f" />

---

## Inspecting Data

There are two main ways to inspect the dataset:

1. Reviewing the attribute table
2. Inspecting the polygons themselves.

## Attribute Table

To open and review the attribute table:

1. Right-click the layer in the Layers panel.
2. Select **Open Attribute Table**.

<img width="451" height="681" alt="Screenshot 2026-03-30 212425" src="https://github.com/user-attachments/assets/a65ae895-9869-4fb5-9d88-d9bf015b4770" />

3. Verify that all required fields are present.

Required fields are described in the **Checking the Attribute Table** section of the [End-to-End Pipeline](https://wmgeolab.github.io/gbDocs/10-workflow-overview/end-to-end-pipeline/).

---

## Polygons

### Selecting Features

1. Use the **Select Features** tool.
2. Click on a polygon to inspect it.

<img width="566" height="350" alt="image" src="https://github.com/user-attachments/assets/bbc735aa-75ad-4ccf-8749-7f244e518c61" />

---

### Checking the Projection

1. Right-click the layer in the **Layers panel**.
2. Select **Properties**.

<img width="245" height="304" alt="image" src="https://github.com/user-attachments/assets/5ed47d80-5821-4831-9efa-7aa31f64c70b" />

3. Open the **Information** tab. 

<img width="634" height="530" alt="image" src="https://github.com/user-attachments/assets/99a8a998-1077-49ec-8266-f42218a6f59b" />

4. Locate the **Coordinate Reference System (CRS)**.

### Expected Result

- The CRS should be **WGS 1984 (EPSG: 4326)**.

---

### Navigating the Map

- Use the **Pan map** tool to move around the dataset.
- Zoom in/out to inspect boundaries more closely.

## What to look for

When inspecting the dataset, check for:

- Missing or incomplete polygons
- Misaligned boundaries
- Gaps or overlaps between regions
- Unusually simplified shapes
- Incorrect geographic placement

## Additional Resources

If additional support is needed to open a file, refer to the [Official QGIS documentation](https://docs.qgis.org/3.44/en/docs/training_manual/basic_map/preparation.html) to read more regarding loading and inspecting data.

---
