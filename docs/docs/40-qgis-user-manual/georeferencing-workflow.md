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

4. Now it is time to georeference. Zoom to the area you want to project onto on the window with the basemap.

<img width="1717" height="890" alt="image" src="https://github.com/user-attachments/assets/74f6822d-acf0-4690-a30e-6a6bca2dbc64" />

5. Select **Add GCP Point** in the Georeferencing pane.

6. Select a notable corner/point on the raster image.

7. Ensure the projection is set to WGS 84/Pseudo-Mercator.

8. Select **From Map Canvas** to select the corresponding same corner from the base map to start the aligning/georeferencing process.

9. Once the corresponding corner has been selected on the basemap, select **OK** on the pop-up.

10. Continue this process at least 5 more times, to conclude with at least 5 GCPs, or control points. (Repeat steps 6-9 five more times)

11. Select **Start Georeferencing**
    <img width="522" height="428" alt="image" src="https://github.com/user-attachments/assets/11669a4b-70f4-419e-af9b-2f017d77ffb3" />

12. Ensure the settings in the pop-up menu match these below. Select OK.

<img width="654" height="1012" alt="image" src="https://github.com/user-attachments/assets/7803ae0e-ef30-4f66-94f3-01cd86feba05" />

13. Select the **Start Georeferencing** button again.

14. Close the Georeferencing tab to see the georeferenced raster image!

## Creating the Shapefile

Now it is time to create the shapefile

1. Go to Layer -> Create Layer -> New Shapefile Layer...
2. A menu will pop up. For geometry type, select Polygon. Save the location other than the hard drive of your computer. Select OK.

<img width="1289" height="676" alt="image" src="https://github.com/user-attachments/assets/ea72711a-f827-4f58-af14-8a581b9f4f01" />

3. Before we can use any tools, we have to toggle editing on the layer. Go to the newly created layer in the contents section and select toggle editing.

<img width="1505" height="782" alt="image" src="https://github.com/user-attachments/assets/12cb09e9-870d-4c47-abe7-1749449db7ac" />

4. Select the **Add Polygon Feature** tool

<img width="248" height="109" alt="image" src="https://github.com/user-attachments/assets/4d69c3ee-316d-4de2-9a60-9eb4c4cd5a91" />

5. Trace your shapefile by clicking around your raster image map. Each time you click it will add another vertex to your shape. The more vertexes the better and more accurate the polygon will be!

<img width="153" height="167" alt="image" src="https://github.com/user-attachments/assets/6f45d335-342d-4c9c-a255-cc741bd29eb1" />

6. When you have fully traced your shape, right-click to save the polygon and label the polygon with an id number.
    - When there is an area of your shape that you would like to edit, select the Vertex Tool.
<img width="173" height="80" alt="image" src="https://github.com/user-attachments/assets/a00d6f5e-4861-45ef-be7f-73c13ceb3b8c" />
When you hover over your shape, it will show you all of the vertices. Using this tool, you can move vertices, move segments, add or delete vertices. You do not need to use this tool every time you digitize, it is just helpful for fixing errors.

7. Now it is time to export the polygon as a shapefile.
    - First, toggle off editing.
    - Next, go to your layer and select export-save features as...

<img width="429" height="392" alt="image" src="https://github.com/user-attachments/assets/42a49e45-1339-4ba3-b59a-234dba984a3a" />

<img width="438" height="493" alt="image" src="https://github.com/user-attachments/assets/14a2a87a-8105-4999-be8e-2addf3516411" />

8. This menu will pop up. Here you can name your file, according to the ISO Code of the Layer and the ADM level. In this case, since Williamsburg is under ADM3, the title of the file would be `USA_ADM3`. Make sure the encoding is UTF-8 and that the CRS is correct.  The format we use is ESRI Shapefile.
Remember to change where it saves from your hard drive to literally anywhere else. DO NOT SAVE TO YOUR HARD DRIVE. 
Click Ok when done. 

The final product should be the 6 files that automatically load when saved:

<img width="614" height="142" alt="image" src="https://github.com/user-attachments/assets/9a6f9f51-1206-4c68-b45f-ef5c801a25ed" />

9. Copy all 6 files and compress them in a zip folder.

<img width="516" height="320" alt="image" src="https://github.com/user-attachments/assets/a1672463-abce-4b7d-a6fe-8907a15b043b" />

10. Add the `meta.txt` file and the `license.png` screenshot to the zip folder, and you are ready to submit!
