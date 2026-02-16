# Deliverables and Artifacts

## Purpose
This page defines the required outputs for the geoBoundaries workflow, so that the efforts can be completely reproducible. It will demonstrate an overview of what should be created and provide a downloadable example of a shape file and meta data file. 

## Inputs
In order to start the workflow, there must be a problem with a layer of data, which can be found at the **[Issues](https://github.com/wmgeolab/geoBoundaries/issues?page=1)** page. After understanding the issue, the user will go through the steps to solving the issue, which is thoroughly detailed in **[End to End Pipeline](https://wmgeolab.github.io/gbDocs/10-workflow-overview/end-to-end-pipeline/)** Section. 

## Outputs
A **zip file** containing the corrected **shapefile**, or a **geojson**, with the related boundary, a **screenshot of the source license** in PNG format, and a **metadata file** will be produced. 

- If the zip file contains a **shapefile** rather than a geojson, it will also contain a minimum of three file types that must be present: `.shp`, `.shx`, and `.dbf`. The other component files that may be present are `.prj`, and `.cpg`.
- If the zip file contains a **geojson**, it will contain the geojson and no other component files.

## Steps
The steps to creating these files will be described in the Pipeline section, as previously stated.

## Validation / QA
Here is a downloadable example using Angola's country border, administrative division 0 (AGO_ADM0).

<a href="https://github.com/wmgeolab/geoBoundaries/raw/refs/heads/main/sourceData/gbOpen/AGO_ADM0.zip" 
   target="_blank" 
   rel="noopener"
   style="display:inline-block;background:#115740;color:#fff;text-decoration:none;
          padding:.9em 1.6em;border-radius:9999px;font-weight:700;letter-spacing:.02em;
          box-shadow:0 8px 24px rgba(0,0,0,.08);transition:transform .05s ease-out">
  ⬇︎ Download the data here
</a>

## Common Errors
What usually goes wrong.

## Related Pages
Links
