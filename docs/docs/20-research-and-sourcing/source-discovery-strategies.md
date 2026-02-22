# Source Discovery Strategies
This document will answer the following questions:
How do researchers find boundary sources in the first place?
Where do we look?

1. ## Discovery Framework
When searching for boundary data that could solve an issue, it is recommended to start with understanding background information on the country, such as:
  - What is the country's official language?
  - What is the name of the administrative division that you are searching for? Examples under ADM1 could include districts, provinces, regions, prefectures, etc.
  - Does the name of the administrative division have a local name?
  - How many of that administrative division do they have? For example, USA_ADM1 has 50 divisions, or 50 states.

Take note everything on relevance to have a log.

It is helpful to start the search with credible and trustworthy sites, for example the official government website of the country may often have the data already.

---

2. ## Search Methods
Use the background information to aid in your search.

**Search Template** to get an idea of _how the country is divided at each level_, replacing the word "country" with your assigned country name:
  - "**Country** administrative boundary divisions"

**Search Template** to _find actual data_:
- “[country name] shapefile administrative divisions”

**Other helpful methods**
- Searching in a the official language of the country
- Search for "**country** open data portal - some countries or groups of countries may have a website where they have a collection of data sets
    - Look out for categories like “Administrative Divisions”, “Territories”, “Geography”
    - These open data portals may have shapefiles but under different categories. Look into census data, health data, or political data. They may be divided by ADM.

**Places to Look For**
- Goverment websites
- Census bureaus
- National mapping agencies
- GitHub (a platform where individuals can post datasets and code) could be a good resource. If you find a good shapefile there, you’ll have to contact the creator of the data set to make sure it’s ok to redistribute.
- Academic papers and websites
    - If you find a map that includes the ADM but doesn’t have the shapefile to download, look at the webpage’s / paper’s bibliography. They may cite the page that contains the downloadable shapefile.
- Constitutions and other official documents are helpful

---

3. ## How we decide a source is unacceptable to use
  - no metadata
  - bad license, that says no commercial use
  - over simplified polygons
  - differeing ADM level definitions from other sources

4. ## What do we require when documenting the source
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

