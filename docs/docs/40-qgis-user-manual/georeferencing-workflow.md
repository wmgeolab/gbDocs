# Georeferencing Workflow

Here is a handy image of some of the important QGIS tools to keep an eye out for:
<img width="557" height="227" alt="image" src="https://github.com/user-attachments/assets/a1870147-f1fb-4d5a-8cd8-74064bf9b4a6" />

This tutorial will review the Georeferencing and Digitizing workflow. Georeferncing is the process of assigning real-world geographic coordinates (latitude/longitude or projection coordinates) to raster data like scanned maps, aerial photos, or satellite imagery. Digitizing is the process of converting information from physical (a paper map, a scanned image, a satellite photo, etc.) into a vector format.

If there is no data available on the country's administrative division based off of your research, it can be helpful to georeference an image of the boundary that has an appropriate license and then digitize the said image to create a polygon.

## Selecting an Image to Georeference

One tip to select an appropriate and acceptable image to georeference is to use a search query with the words "border", "outline", and "map". In order to demonstrate this, Williamsburg, Virginia will be used an example. The query "williamsburg virginia boundary map outline" was used to find an image with an acceptable license. The license specifically clarifies that the image can be used for any purposes, **even commercial**. To know which licenses are acceptable, review [this page](https://wmgeolab.github.io/gbDocs/20-research-and-sourcing/licensing-and-permissions/)/ 

Here is the image that was selected for the georeferencing of Williamsburg, VA.

<img width="713" height="726" alt="image" src="https://github.com/user-attachments/assets/6d24d032-2277-4d3f-bcd6-5fadaf7d743f" />

This is a good example because
- The quality of the image is good
- The edges are very detailed and precise
- There is an acceptable license listed

Here is a bad example of an image for georeferencing:

<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/dfe05d19-6d06-47a2-a199-b4418be16e1a" />

This is a bad example because:
- The quality of the image is bad
- The segments are not detailed and precise enough
- There is no license listed on the website

## Georeferencing

When adding a picture of a map to QGIS, it appears in the middle of the ocean. Georeferencing is when we take an image, and manually tell QGIS where to place it on a base map. Open up a QGIS project to get started with georeferencing. 

1. To add a basemap of your choice, ensure the "Browser Panel" is visible.
<img width="347" height="344" alt="image" src="https://github.com/user-attachments/assets/feb6f77c-e1bf-4e4b-b424-451a43c130ad" />

2.  Scroll until you locate the "XYZ Tiles" For this example, we will use the OSM basemap.

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
<img width="277" height="212" alt="image" src="https://github.com/user-attachments/assets/26e600ac-c57d-4abf-81b4-4cca8f418f57" />

8. Select **From Map Canvas** to select the corresponding same corner from the base map to start the aligning/georeferencing process.

9. Once the corresponding corner has been selected on the basemap, select **OK** on the pop-up.

10. Continue this process at least 5 more times, to conclude with at least 5 GCPs, or control points. (Repeat steps 6-9 five more times)

11. Select **Start Georeferencing**
    <img width="522" height="428" alt="image" src="https://github.com/user-attachments/assets/11669a4b-70f4-419e-af9b-2f017d77ffb3" />

12. Ensure the settings in the pop-up menu match these below. Select OK.

<img width="654" height="1012" alt="image" src="https://github.com/user-attachments/assets/7803ae0e-ef30-4f66-94f3-01cd86feba05" />

13. Select the **Start Georeferencing** button again.

14. Close the Georeferencing tab to see the georeferenced raster image!

## Digitizing

Now it is time to create the shapefile

1. Go to Layer -> Create Layer -> New Shapefile Layer...
2. A menu will pop up. For geometry type, select Polygon. Save in a location **other than the hard drive of your computer**. Select OK.

<img width="1289" height="676" alt="image" src="https://github.com/user-attachments/assets/ea72711a-f827-4f58-af14-8a581b9f4f01" />

3. Before we can use any tools, we have to toggle editing on the layer. Go to the newly created layer in the contents section and select toggle editing.

<img width="1505" height="782" alt="image" src="https://github.com/user-attachments/assets/12cb09e9-870d-4c47-abe7-1749449db7ac" />

4. Select the **Add Polygon Feature** tool

<img width="248" height="109" alt="image" src="https://github.com/user-attachments/assets/4d69c3ee-316d-4de2-9a60-9eb4c4cd5a91" />

5. Trace your shapefile by clicking around your raster image map. Each time you click it will add another vertex to your shape. The more vertexes the better and more accurate the polygon will be!

<img width="153" height="167" alt="image" src="https://github.com/user-attachments/assets/6f45d335-342d-4c9c-a255-cc741bd29eb1" />

6. When you have fully traced your shape, right-click to save the polygon and label the polygon with a **temporary** id number. The ID column will later be deleted once the rest of the required fields are entered.
    - When there is an area of your shape that you would like to edit, select the Vertex Tool.
<img width="173" height="80" alt="image" src="https://github.com/user-attachments/assets/a00d6f5e-4861-45ef-be7f-73c13ceb3b8c" />
When you hover over your shape, it will show you all of the vertices. Using this tool, you can move vertices, move segments, add or delete vertices. You do not need to use this tool every time you digitize, it is just helpful for fixing errors.

---

## Snapping Multiple Polygons and Merging Polygons

If you need to step away from the project and continue adding vertices to a polygon, or if you need to add a polygon that is adjacent to another polygon, follow the tutorial below. This tutorial is also helpful if you are digitizing many divisions and would like to trace the surrounding polygons as a basis.


1. Select "View" and then "Toolbars". Ensure all of these toolbars below are selected so that the needed tools are available. The required toolbars are "Advanced Digitizing Toolbar" and "Snapping Toolbar".
<img width="410" height="613" alt="image" src="https://github.com/user-attachments/assets/20de296a-b7b2-48ca-878e-38e200f2f83b" />

2. Ensure that these tools are selected to be able to snap the new polygon to the old one. Click "Enable Snapping". Select "Vertex", "Segment", and "Area" within the "Area" tool. Set the "Snapping Tolerance in Defined Units" to 5 meters. Select "Enable Snapping on Intersection", "Enable Tracing", and "Enable self-snapping". 
<img width="386" height="157" alt="image" src="https://github.com/user-attachments/assets/f749b474-af54-4153-a814-6d1ca77fb2b1" />

3. Select the "Select Features by Area or Single Click" tool and select the polygon that you would like to add more vertices to. 
<img width="334" height="400" alt="image" src="https://github.com/user-attachments/assets/87020a3d-11f5-49a1-b982-3cdd0921a1f9" />

4. Select the "Add Polygon Feature" tool. 
<img width="112" height="66" alt="image" src="https://github.com/user-attachments/assets/ec00ebcc-4bc9-49f9-af3e-7104a1d749d8" />

5. Hover over the vertex you would like to begin from. Once you see the pink square, click the vertex.
<img width="678" height="354" alt="Screenshot 2026-04-05 223804" src="https://github.com/user-attachments/assets/c70473f6-f719-4c01-a5b6-de0d1869e753" />

6. Drag along the segment of the original polygon and click when you see a pink "X".
<img width="561" height="287" alt="image" src="https://github.com/user-attachments/assets/b2b304d4-d1ae-4685-a9ac-a42f095b7ad0" />

7. Trace the area with vertexes just like you did with the original polygon. Once you have returned to the starting point of this new polygon, hover over the starting point and press with two fingers to close the polygon.
<img width="515" height="370" alt="image" src="https://github.com/user-attachments/assets/001f2799-a6ef-4da3-aae4-31d44a5619cc" />

8. Give the new polygon a **temporary** id number. The ID column will later be deleted once the rest of the required fields are entered.

Here is where you would stop if you only need to create an adjacent polygon using the snapping tool. If you would like to merge the polygons, continue to step 9.

9. Using the "Select Features by Area or Single Click" tool, select both polygons to begin a merge.
10. Select the "Merge Selected Features" tool. This will combine the two polygons into one. Select "OK".
<img width="343" height="434" alt="image" src="https://github.com/user-attachments/assets/37c578a3-8a6f-41a1-9eab-22b58aeb37b7" />

Now your two Polygons are merged into one!

---

## Saving the Polygon(s) as a Shapefile

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
