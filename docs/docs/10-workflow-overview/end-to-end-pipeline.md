# End-to-End Pipeline for geoBoundaries

## Using GitHub

Tasks are located on GitHub and are called **“[issues](https://github.com/wmgeolab/geoBoundaries/issues)”**.

## Overview of Issue Workflow

1. Identify the country and administrative division (ADM level) using [ISO codes](#identifying-the-country).
2. Understand the [task type](#understand-the-task-type) on GitHub.
3. Follow the corresponding detailed guide:
   - **[Research a shapefile](#researching-boundaries)**
   - **[Digitize a shapefile](#)**
   - **[Other issues](#)**
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


In order to continue the process of boundary research, up to this point a valid boundary would contain:
 1. A license that is appropriate for all uses (commercial, educational...)
 2. A source that we are able to provide, who geoBoundaries does not supply boundaries for.
 3. Relevant boundary information that would update the boundary in comparison to the one geoBoundaries already has.

After all of these requirements are met, then the shapefile should be downloaded and verified for complete accuracy.

### Checking the Shapefile

1. If the file is zipped, unzip the file.
2. Open **ArcGIS Pro** or **QGIS**
3. Drag/upload the shape file onto the map.
4. Check the attribute table for naming accuracy
5. Check the polygon for drawn accuracy.

---
If you cannot find an acceptable license or usable data online, you may digitze the boundary, using the following steps.


## Digitizing

If an acceptable licensed shapefile is not found:

1. Open **ArcGIS Pro** or **QGIS**
2. Find an image to georeference.
3. ... 

---

## Other Common Issues

- Quick fixes, e.g., correcting typos in boundary names.
- Fixing a polygon to contain another polygon, or not contain another polygon
- Adding polygons to pre-existing boundaries

Tips:
- Always double-check the license when updating old files, as they may be outdated
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
