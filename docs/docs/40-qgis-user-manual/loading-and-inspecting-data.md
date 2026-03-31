# Loading and Inspecting Data

Once the data has been downloaded following the steps of the [Downloading Data page](https://wmgeolab.github.io/gbDocs/30-data-acquisition/downloading-data/), it is time to load it into QGIS.

1. Open QGIS
2. Drag the GeoJSON over into the starting up QGIS window.
<img width="913" height="348" alt="Drag_Drop" src="https://github.com/user-attachments/assets/6aa740c1-e08d-4c4d-aa35-dc76f491fbaa" />
3. Select add layers.
<img width="434" height="267" alt="add_layers" src="https://github.com/user-attachments/assets/67a0d8e8-f976-4a33-bca7-fc3b6005b133" />
4. The selected boundary should appear in the window. `USA_ADM1` is listed as an example. 
<img width="821" height="484" alt="USA_example" src="https://github.com/user-attachments/assets/066c3749-93bc-4773-872f-85550baad40f" />

## Inspecting Data

There are two main ways to inspect the data:
1. Check the attribute table
2. Check the polygons themselves.

### Attribute Table

To check the attribute table:

1. Click with two fingers on the name of the layer listed in the Layers pane.
2. Select "Open Attribute Table"
<img width="451" height="681" alt="Screenshot 2026-03-30 212425" src="https://github.com/user-attachments/assets/a65ae895-9869-4fb5-9d88-d9bf015b4770" />
3. Inspect the columns in order to see if each required column is there. The required columns are described in the "Checking the Attribute Table" section of the [End-to-End Pipeline section](https://wmgeolab.github.io/gbDocs/10-workflow-overview/end-to-end-pipeline/).

### Polygons

1. Select a single feature by using the "Select Features" tool.
<img width="566" height="350" alt="image" src="https://github.com/user-attachments/assets/bbc735aa-75ad-4ccf-8749-7f244e518c61" />
2. Check the projection of the entire GeoJSON by following these steps
  - Click with two fingers on the name of the layer.
  - Select "Properties"
<img width="245" height="304" alt="image" src="https://github.com/user-attachments/assets/5ed47d80-5821-4831-9efa-7aa31f64c70b" />
  - Select the "Information" pane.
<img width="634" height="530" alt="image" src="https://github.com/user-attachments/assets/99a8a998-1077-49ec-8266-f42218a6f59b" />
  - The name of the geographical coordinate system is under "Coordinate Reference System (CRS)".
3. Use the "Pan map" tool to scroll through the polygon(s).

If additional support it needed to open a file, the user may visit the [QGIS documentation](https://docs.qgis.org/3.44/en/docs/training_manual/basic_map/preparation.html) to read more regarding loading and inspecting data.




