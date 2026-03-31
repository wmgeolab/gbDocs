# Georeferencing Workflow

Basic tools and what they do:
<img width="557" height="227" alt="image" src="https://github.com/user-attachments/assets/a1870147-f1fb-4d5a-8cd8-74064bf9b4a6" />

## Selecting an Image to Georeference

bad example: 

<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/dfe05d19-6d06-47a2-a199-b4418be16e1a" />



## Georeferencing

When adding a picture of a map to QGIS, it appears in the middle of the ocean. Georeferencing is when we take an image, and manually tell QGIS where to place it on a base map.

1. Add a basemap of your choice. For this example, we will use the OSM basemap.

<img width="452" height="380" alt="image" src="https://github.com/user-attachments/assets/3ae19182-d602-4221-a47a-00cbc0c95833" />

3. Click Layer, then the **Georeferencer** tool.

<img width="316" height="165" alt="image" src="https://github.com/user-attachments/assets/eb93f67c-340a-4d03-94bd-08037c2bee7d" />

3. Once in the georeferencing tool, you need to open your raster (the image of your map). 

<img width="132" height="102" alt="image" src="https://github.com/user-attachments/assets/3606e8cf-828e-425a-911c-4393ba67ad06" />

You must download the raster image using one of these formats: GeoTIFF (.tif, .tiff), JPEG (.jpg, .jpeg), PNG (.png), BMP (.bmp). GIF (.gif), and a few others.

4. Now it is time to georeference. Zoom to the area you want to project onto
