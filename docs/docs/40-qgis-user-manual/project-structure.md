# Project Structure

When starting an open issue that is listed on the [geoBoundaries GitHub](https://github.com/wmgeolab/geoBoundaries/issues?page=1), it is important to first understand the existing boundary in order to identify the problem. Follow the instructions from the [downloading data page](https://wmgeolab.github.io/gbDocs/30-data-acquisition/downloading-data/) to access the current dataset. 

## Overarching Folder

All work should be contained within a single folder named: `ISO_ADM#`, corresponding to the ISO Code of the issue and the administrative division level.
Example: `USA_ADM1`

This folder name must match:
  - The issue title
  - The dataset name
  - The GeoJSON name

## Expected Folder Contents

The folder contents differ when working on QGIS vs ArcGIS Pro. The remaining tutorials will reference QGIS, and QGIS only.

The folder should contain the following files:

1. Boundary file (GeoJSON or shapefile)
2. `meta.txt` (metadata file)
3. `license.png` (license screenshot)

A description of what each file should contain is listed [at this page](https://wmgeolab.github.io/gbDocs/10-workflow-overview/deliverables-and-artifacts/). 

## Example Folder Structure

`USA_ADM1/
│
├── USA_ADM1.geojson
├── meta.txt
└── license.png`

## Boundary File (GeoJSON)

The boundary file contains:

- Polygon geometry for all administrative units
- The attribute table with required fields

### Naming Rules

- Must match the folder name exactly: `ISO_ADM#`
- No spaces or special characters

### Requirements

- Correct ADM Level
- Valid geometry (no broken polygons)
- Complete attribute table

---
## Common Mistakes

- Incorrect folder name (not matching `ISO_ADM#`)
- Missing files
- Mismatched file names (e.g. when the folder name does not match the GeoJSON file name)
- Including extra unnecessary files
- Using spaces or inconsistent naming

---
