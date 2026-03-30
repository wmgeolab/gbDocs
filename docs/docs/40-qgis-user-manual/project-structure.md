# Project Structure

When starting an open issue that is listed on the [geoBoundaries GitHub](https://github.com/wmgeolab/geoBoundaries/issues?page=1), it is important to first understand what the original boundary looks like in order to spot the problem. Follow the instructions from the [downloading data page](https://wmgeolab.github.io/gbDocs/30-data-acquisition/downloading-data/) to download the boundary. 

## Overarching Folder

The folder that you download from the GitHub repository be titled `ISO_ADM#`, corresponding to the ISO Code of the issue and the administrative division level. The folder should contain three files:

1. The GeoJSON containing the polygon(s) of the boundary and its attribute table.
2. The meta.txt file containing the meta data.
3. The license.png file containing a screenshot of the license.

## GeoJSON


The shapefile or GeoJSON will be located inside of a folder with the ISO Code and the corresponding administrative division level, in this format: `ISO_ADM#`. For example for an issue with the United States of America, the administrative division level one, or ADM1, corresponds to the 50 states. The title of the folder and the geojson should match, and for the example, it would be titled `USA_ADM1`. 
