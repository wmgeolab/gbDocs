# End-to-End Pipeline for geoBoundaries

## Using GitHub

Tasks are assigned via GitHub and are called **“[issues](https://github.com/wmgeolab/geoBoundaries/issues)”**.

---

## How to Find the Data

GeoBoundaries source data is hosted on GitHub:

[Source Data Repository](https://github.com/wmgeolab/geoBoundaries/tree/main/sourceData/gbOpen)

---

## Overview of Issue Workflow

1. Identify the country and administrative division (ADM level) using **[ISO codes](#finding-iso-codes)**.
2. Understand the task type on GitHub and follow the corresponding detailed guide:
   - **[Research a shapefile](#researching-boundaries)** <!-- TODO: Add link to research guide -->
   - **[Digitize a shapefile](#)** <!-- TODO: Add link to digitize guide -->
   - **[Other issues](#)** <!-- TODO: Add link -->
3. Compiling the completed files into a zip file and submitting
---

## Finding ISO Codes

An ISO Code is a standardized, unique, short identifier for countries that is established by the International Organization for Standardization.

The **issue title** indicates the country and administrative division level. 

Example: `VNM_ADM2` → `VNM` = Vietnam, `ADM2` = administrative division level 2.

Here is the official [ISO website](https://www.iso.org/obp/ui/#search) that allows you to search up a country and its corresponding ISO code. 

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

## License Information

- [List of licenses we **can** and **cannot** use](https://github.com/wmgeolab/gbDocs/blob/main/docs/Licenses%20for%20gB%20Open.md)  

> **Note:** This list is not comprehensive. Notify the team if a new license type is found.

### If the License Is Unclear

- Contact the data owner for permission  
- Use the [permission tracking template provided](https://github.com/wmgeolab/gbDocs/blob/main/docs/templates/Boundary%20Request.md)
- If the owner responds and affirms the data's usage, save the correspondence in the zip file for the boundary, as it is proof that the data can be used.

In order to continue the process of boundary research, up to this point a valid boundary would contain:
 1. A license that is appropriate for all uses (commercial, educational...)
 2. A source that we are able to provide
 3. Up to date boundary information that would update the boundary in comparison to the one geoBoundaries already has.

After all of these requirements are met, then the shapefile should be downloaded and verified for complete accuracy.

### Checking the Shapefile

Once you find a shapefile with an acceptable license:

1. Open the file in **ArcGIS Pro** or **QGIS**
2. Verify accuracy of polygons and attributes

<!-- TODO: Add screenshot of ArcGIS Pro verification -->

---



---

## Downloading geoBoundaries Data from GitHub

1. Navigate to the [Source Data repository](https://github.com/wmgeolab/geoBoundaries/tree/main/sourceData/gbOpen)
2. Locate the country and ADM level (alphabetical then ADM order)
3. Click the folder and download using **View raw** or the download button  
4. Extract all files:
   - Right-click → **Extract All**
   - Save to local folder (OneDrive recommended)
5. Drag the `.shp` shapefile into a new ArcGIS Pro map

<!-- TODO: Add screenshots for ZIP extraction and ArcGIS drag -->

---

## Digitizing

If an acceptable licensed shapefile is not found:

1. Open **ArcGIS Pro**  
2. Sign in using organizational link (`wm-gis`)  
3. Drag/upload shapefiles from unzipped folder  
4. Check attribute table and polygons  

<!-- TODO: Add screenshots for each step -->

---

## Other Common Issues

- Quick fixes, e.g., correcting typos in boundary names  
- Always double-check licenses when updating old files  

---

## Clean Up and Submission

Before submitting:

1. Ensure shapefile is clean  
2. Project polygons correctly (coordinate system)  
3. Export shapefile properly  
4. Zip all files for GitHub submission

### Required Files in Submission ZIP

- Clean shapefile  
- `.png` screenshot of license information showing source URL  
- `.txt` file with metadata information  

<!-- TODO: Add screenshot showing example ZIP contents -->

---

## Submission

[Submit ZIP here](#) <!-- TODO: Replace with actual submission link -->



