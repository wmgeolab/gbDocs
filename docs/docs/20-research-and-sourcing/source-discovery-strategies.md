How do researchers find boundary sources in the first place?

Where do we look?

1. Discovery Framework
  - Official government data
  - ...

2. Search Methods
- Searching in a different language
- keywords (shapefile, adm#, ...)

3. How we decide a source is unacceptable to use
  - no metadata
  - bad license, that says no commercial use
  - over simplified polygons
  - differeing ADM level definitions from other sources

4. What do we require when documenting the source
   everything that appears in the meta.txt file
  - url
  - license
  - year

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

