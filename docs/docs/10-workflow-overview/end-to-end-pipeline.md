# End-to-End Pipeline for geoBoundaries

## Using GitHub

Tasks are located on GitHub and are called **“[issues](https://github.com/wmgeolab/geoBoundaries/issues)”**.

## Overview of Issue Workflow

<img src="../../images/workflow.png" width="400">

1. Identify the country and administrative division (ADM level) using [ISO codes](#identifying-the-country).
2. Understand the [task type](#understand-the-task-type) on GitHub.
3. Follow the corresponding detailed guide:
   - **[Research a shapefile](#researching-boundaries)**
   - **[Digitize a shapefile](#digitizing)**
   - **[Other issues](#other-common-issues)**
4. Compile the completed files into a zip file and submitting
---

## Identifying the country
### Finding ISO Codes

An ISO Code is a standardized, unique, short identifier for countries that is established by the International Organization for Standardization.

The **issue title** indicates the country and administrative division level. 

Example: `VNM_ADM2` → `VNM` = Vietnam, `ADM2` = administrative division level 2.

Here is the official [ISO website](https://www.iso.org/obp/ui/#search) that allows you to search up a country and its corresponding ISO code. 

## Understand the task type
There are usually three possible scenarios that contributors can be tasked with.

1. [Researching a new source of data with an accurate license.](#researching-boundaries)
2. [Digitizing a boundary in ArcGIS Pro or QGIS.](#digitizing)
3. [Quick fix issues such as typos or polygon fixes.](#other-common-issues)

## Researching Boundaries

### General Searching Tips

- Research background info on the country (number of divisions, ADM names)
- Use search terms like: "**country name** shapefile **administrative division**"
- Utilize government websites, census bureaus, and national mapping agencies
- Try searching in the local language

### Sources to Avoid (License Issues)
- Avoid these common sources due to license issues:

    - GADM
    - earthworks.stanford.edu
    - maps.princeton.edu
    - geodata.lib.berkley.edu
    - Open Street Map
    - humdata/hdx

> Avoid any license that contains “sharealike.”

### License Information

- [List of licenses we **can** and **cannot** use](https://github.com/wmgeolab/gbDocs/blob/main/docs/Licenses%20for%20gB%20Open.md)  

> **Note:** This list is not comprehensive. Notify the team if a new license type is found.

### If the License Is Unclear

- Contact the data owner for permission  
- Use the [permission tracking template provided](https://github.com/wmgeolab/gbDocs/blob/main/docs/templates/Boundary%20Request.md)
- If the owner responds and affirms the data's usage, save the correspondence in the zip file for the boundary, as it is proof that the data can be used.
---
In order to continue the process of boundary research, up to this point a valid boundary would contain:

1. A license that is appropriate for all uses (commercial, educational...)
2. A source that we are able to provide, who geoBoundaries does not supply boundaries for.
3. Relevant boundary information that would update the boundary in comparison to the one geoBoundaries already has.

After all of these requirements are met, then the shapefile should be downloaded and verified for complete accuracy.

### Checking the Shapefile

1. Download the shapefile.
2. Extract the data from the zipped file.
   a. Right click the folder and hit "extract all" in the top ribbon. It will prompt you to save it in a certain location on the computer (do this wherever you see fit).
   b. When you navigate to your chosen folder, you’ll see the zip file plus the separate files with the same name. Make sure you see “filename.shp”
3. Open **ArcGIS Pro** or **QGIS**. Select the "blank map" option. Name it `ISO_ADM#` with the corresponding iso code and ADM level of your boundary.
4. Click the “Add Data” button in the top ribbon (if it doesn’t appear, hit the “Map” tab), then hit “Data” in the dropdown. Navigate to the folder where you saved the extracted ADM files. Click on it, then hit “OK”.
5. Checking the attribute table
   a. The boundary will appear in the map frame and the name of the shapefile will appear in the left pane.
   b. Right click on the shapefile name, then hit the “Attribute Table” option.
   c. The attribute table shows you all of the features within the shapefile.
      - The number of features is the total number of polygons in the shapefile. This equates to the number of features within the administrative division.
      - Make sure the number of polygons within the shapefile is correct (see your previous research) and that the names of each feature are correct.
      - We’ll revise the attribute table later. It’s best to check it early to make sure your data is correct and complete (don’t waste your time processing a faulty boundary).
   d. Projecting the Shapefile





---
If you cannot find an acceptable license or usable data online, you may digitze the boundary, using the following steps.


## Digitizing

**Digitizing** is the process of converting features from an image into digital vector data (a polygon).

If an acceptable licensed shapefile is not found, follow these steps:
<details>
   <summary>Digitizing Steps</summary>

### **Finding an image to georeference**
   In order to start the digitizing process, you must find an image that has the appropriate boundary of your country. There are a lot of ways to find an image that works, here are some common options:

1. Wikimedia
   - Make sure to check the license on the wikimedia page, and that it is acceptable.
2. Google images

Once you have found the image with an acceptable license, you can start the process of georeferencing.

### **Georeferencing your image**

1. Open **ArcGIS Pro** or **QGIS** on the computer. Select the "blank map" option. Name it with the corresponding country ISO code and ADM level, `ISO_ADM#`.
2. Add Data → Data in ArcGIS Pro to import your image (if it doesn’t appear hit the “Map” tab). Then hit “Data” in the dropdown, and navigate to the folder where you saved the extracted ADM files, or the image that you will digitize over.
_insert image of argis / qgis tools bar_
3. Your image will show up in the middle of the ocean, that’s expected. If moving/adjusting the image will help, there are some tools to use.
   - In the top ribbon, under the Imagery tab, click on Georeference. The Fit to Display, Move, Scale, and Rotate tools can help adjust your image.
4. In the top ribbon, under the Georeference tab, click Add Control Points.
  a. First, click a on a point of the image that will be easy to align with the basemap.
   - It will be easier to make the image somewhat transparent. Under the Appearance tab, adjust the transparency under the Effects section of the top ribbon.
  b. Second, click where you want that point to align with on the basemap.
  c. Do this several times along the border to best match up the image with the basemap.
  d. After you’ve added a lot of control points, they will have shifted. Under the Georeference tab in the top ribbine, click on Transformation, and then Adjust. This will transform the image to make all of the control points line up.
  e. When done, click Save in the top ribbon under the Georeference tab. Then click Close Georeference.

### **Digitizing**
1. In the Catalog Pane on the right side, open the Folders drop down. You should see a folder with your project name.
2. Right click on the project folder → New → Shapefile.
   _Insert image of new shapefile_
   a. Add the Feature Class Name, Geometry Type (this workflow will go through polygon and polyline, and Coordinate System (**WGS 1984**).
   b. Should look like the screenshot below, and then click run. To find the coordinate system, click on the circle next to that field and search “WGS 1984” (Click on the globe and search WGS 1984, filter through geographic coordinates system and then world.
   _insert image of geoprocessing tab_
3. Under the Edit tab in the top ribbon, click Create in the Features section
   a. In the right side pane, click on the feature you want to create for.
   b. Start clicking along the lines of your boundary for one of the subdivisions, making sure that you are clicking based on where the boundary line is in the image, not the basemap. Turn the transparency of the image back to 0%
    - When you are done with the polygon, or with a section of one, double click on the vertex that you started with to close the polygon.
   c. When starting on a different section, you can use the trace tool on the bottom pop-up for adjacent features to trace the border of an existing polygon so you don't have to make sure all of the vertices are matched up manually.
   _insert photo of the trace tool_
   d. When done, click the Save button under the Edit tab in the top ribbon.
   e. Add all of the required fields for these polygons in the attribute table.

### Attribute Table
After completing the digitizing steps, ensure there are the same number of features as there are supposed to be subdivisions for your given country.

1. Navigate to the attribute table
_insert screenshot of attribute table guidance_
2. Edit the Fields of the attribute table
3. Ensure the following fields exist in the attribute table:
   a. Name (Text type, length = 50)
   b. ISO Code (Text type, length = 50)
   c. ADM Level (Text type, length 50)
   d. Object ID
   e. Shape
   To add a field, hit the "add field" ribbon near the bottom of the pane, using the respective criteria.
4. Delete all the other fields that aren't needed. To do so, right click on the green box to the left of the field name and click delete. Save all progress.
5. Fill in the fields accurately.
   a. Return to the original attribute table table.
   b. The fields just made should be empty, but we'll be using the "Calculate Field" tool to populate them.
     1. Hit the name of the field you want to populate. Hit the “Calculate Field” button, located at the top of the table. The “Calculate Field” pane will appear.
     2. In the “Field Name” box, select the name of the field you want to populate. We can start with the “**Name**” field.
        a. For the “Name” field, we’re just copying the contents of an existing field. The box that says “Name” = ____ is where we build the expression.
        b. Double click the name of the original field with the names of the divisions. It will automatically fill in the blank.
        c. Hit run.
     3. **ISO_Code and Level**
        a. The “Calculate Field” pane will still be up. Let’s do “ISO_Code” next.
        b. Select “ISO_Code” from the “Field Name” dropdown. You’re not copying information from another column; you’re simply filling in the same ISO code for each row in the table. In the “ISO_Code” = ___ space, type in (include the quotes): “County’s ISO Code” Quotes are how you represent a string/text in python.
        c. ISO codes are only needed for **ADM0s** and **ADM1s**. For ADM0 use the generalized “country’s ISO code”, but for ADM1 use the 3166-2 code as specified, accessible [here](https://www.iso.org/obp/ui/#home) with “country codes” selected.
        _insert photo of example with the 3166-2 code_
        d. Hit “OK” or “Apply”
        e. Repeat the same thing for level, except you would fill the “Level” = ____ space with “ADMX”. For example, the level for an ADM4 boundary would be “ADM4”.

Now that all fields are populated in the Attribute Table
1. Order the fields in this order: Object ID, Shape, Name, Level, ISO_Code
   a. Click on the title of the column and drag to relocate the fields.
   _insert final attribute table example_
   

   
   


</details>
---

## Other Common Issues

- Quick fixes, e.g., correcting typos in boundary names.
- Fixing a polygon to contain another polygon, or not contain another polygon
- Adding polygons to pre-existing boundaries

Tips:
- Always double-check the license when updating old files, as they may be outdated.
- Ensure that you submit the correct file, as when renaming files to our naming convention, there may be mixups with the old file that has the same name.

---

If there is a quick fix in a boundary that does not require researching a new boundary, or digitizing from scratch, follow the proceeding steps:

### How to Find and Download geoBoundaries Data from the GitHub

GeoBoundaries source data is hosted on GitHub:

1. Navigate to the [Source Data repository](https://github.com/wmgeolab/geoBoundaries/tree/main/sourceData/gbOpen)
2. Locate the country and ADM level (alphabetical then ADM order)
3. Click the folder and download using **View raw** or the download button  
4. Extract all files from the zipped folder:
   - Right-click → **Extract All**
   - Save to local folder (OneDrive recommended)
5. Drag the `.shp` shapefile or `.geojson` into a new ArcGIS Pro or QGIS map
6. Complete the quick fix.

---

## Clean Up and Submission

Before submitting:

1. Ensure shapefile is in the correct geographic projection: 'WGS 1984'
2. Check that all of the fields in the attribute table exist including:
     -  Name
     -  Level (ADM 0-4+)
     -  ISO_Code (only for ADM levels 0-1, ADM2+ levels do not have an ISO field because they are too granular)
3. Export shapefile with the proper name (ISO_ADM#)
4. Take a screenshot of the license with the URL visible, and name it `license.png`
5. Create a new text file for the metadata. Make sure it follows the format described [here](https://github.com/wmgeolab/gbDocs/blob/main/docs/docs/10-workflow-overview/deliverables-and-artifacts.md)
6.  Ensure that the `meta.txt` file and the `license.png` screenshot and the shapefile are in the same folder
7.  Compress/zip all files, and ensure the compressed file (zip file) has the same name as the ADM (ex - USA_ADM2) for GitHub submission


## Submission via Website

[Submit ZIP here](https://www.geoboundaries.org/gbContribute.html)
