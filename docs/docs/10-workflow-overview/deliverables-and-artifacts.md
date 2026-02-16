# Deliverables and Artifacts

## Purpose
This page defines the required outputs for the geoBoundaries workflow, so that the efforts can be completely reproducible. It will demonstrate an overview of what should be created and provide a downloadable example of a shape file and meta data file. 

## Inputs
In order to start the workflow, there must be a problem with a layer of data, which can be found at the **[Issues](https://github.com/wmgeolab/geoBoundaries/issues?page=1)** page. After understanding the issue, the user will go through the steps to solving the issue, which is thoroughly detailed in **[End to End Pipeline](https://wmgeolab.github.io/gbDocs/10-workflow-overview/end-to-end-pipeline/)** Section. 

## Outputs
The expected output is a zip file containing:
   1. The corrected **shapefile**, or a **geojson**, with the related boundary, `ISO_ADM#`.
   2. A **screenshot of the source license** in PNG format, `license.png`.
   3. A **metadata file**, `meta.txt`.

Boundary File:

   - If the zip file contains a **shapefile** rather than a geojson, it will also contain a minimum of three file types that must be present: `.shp`, `.shx`, and `.dbf`. The other component files that may be present are `.prj`, and `.cpg`.
   - If the zip file contains a **geojson**, it will contain the geojson and no other component files.

License File:
The screenshot must include the url of the license source, a full screen screenshot is preferred.

Metadata File:

Within the `meta.txt` file, there are several subfields that describe the data.

Boundary Representative of Year: Year that the data was created
ISO-3166-1 (Alpha-3): ISO 3-letter country code 
Boundary Type: Administrative Division level
Canonical Boundary Type Name: Official name of the boundary
Source 1: Data Source #1
Source 2: Data Source #1
Release Type: gbOpen 
License: Type of license the data is shared under
License Notes: Specifications on license usage
License Source: Link to the licensing information
Link to Source Data: Link to the source data information
Other Notes: ...

## Steps
The steps to creating these files will be described in the Pipeline section, as previously stated.

## Validation / QA
Here is a downloadable example of a zip file containing the 3 expected outputs, using Angola's country border, administrative division 0 (AGO_ADM0).

<a href="https://github.com/wmgeolab/geoBoundaries/raw/refs/heads/main/sourceData/gbOpen/AGO_ADM0.zip?download=" 
   target="_blank" 
   rel="noopener"
   style="display:inline-block;background:#115740;color:#fff;text-decoration:none;
          padding:.9em 1.6em;border-radius:9999px;font-weight:700;letter-spacing:.02em;
          box-shadow:0 8px 24px rgba(0,0,0,.08);transition:transform .05s ease-out">
  ⬇︎ Download the data here
</a>

Within the zip file, there is the `.shp` file, and the other component files that are crucial for spatial accuracy, the `meta.txt` file, and the `license.png` screenshot of the boundary's license.

## Common Errors
There are usually errors regarding the component files that automatically generate with the shape file. In addition, within `meta.txt`, it is important to accurately display the boundary as the country itself calls it. 
