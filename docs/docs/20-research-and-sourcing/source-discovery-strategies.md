# Source Discovery Strategies
This document will answer the following questions:
How do researchers find boundary sources in the first place?
Where do we look?

## 1. Discovery Framework
When searching for boundary data that could solve an issue, it is recommended to start with understanding background information on the country, such as:
  - What is the country's official language?
  - What is the name of the administrative division that you are searching for? Examples under ADM1 could include districts, provinces, regions, prefectures, etc.
  - Does the name of the administrative division have a local name?
  - How many of that administrative division do they have? For example, USA_ADM1 has 50 divisions, or 50 states.

Take note everything of relevance, to have a log.

It is helpful to start the search with credible and trustworthy sites, for example the official government website of the country may often have the data already.

---

## 2. Search Methods
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

## 3. How we decide a source is unacceptable to use

The datasets we incorporate into the GeoBoundaries dataset have to be openly licensed so that we can redistribute and not get yelled at. If a source does not have an appropriate license, for example, a source that does not allow the commercial usage of their data would be considered an unacceptable source. 

What makes a source unacceptable:
  - No metadata
  - Unacceptable license, that says no commercial use
  - Over simplified polygons
  - Differeing ADM level definitions from other sources

Here are common sites we cannot use:
  - GADM
  - earthworks.stanford.edu
  - maps.princeton.edu
  - geodata.lib.berkley.edu
  - Open Street Map
  - humdata/hdx
  - any license with "sharealike" in the name

These types of data licenses help us deduce whether or not a source is acceptable or not:

  - **Public Domain**: Most open of them all, free to share, create, and adapt, no attribution needed. This is the best kind of license available, and we absolutely want to include data like this. 
Some sources are under this license, but they aren’t found as often in the wild
  - **Creative Commons**: all creators of data retain copyright while allowing others to copy, distribute, and make uses of their work (https://creativecommons.org/licenses/). There are lots of different versions of this license, but (almost) all allow us to copy, tweak, and redistribute non-commercially at least. When coming across this license, make sure that we have the legal ability to make changes (i.e. change geometry or attribute table) and redistribute for free. 
A lot of the data on government portals are under this license
Be sure to avoid Share-alike clauses

- [List of licenses we **can** and **cannot** use](https://github.com/wmgeolab/gbDocs/blob/main/docs/Licenses%20for%20gB%20Open.md)  

> **Note:** This list is not comprehensive. Notify the team if a new license type is found.

A source is acceptable if it is:
1. A license that is appropriate for all uses (commercial, educational...)
2. A source that we are able to provide, who geoBoundaries does not supply boundaries for.
3. Relevant boundary information that would update the boundary in comparison to the one geoBoundaries already has.

After all of these requirements are met, then the shapefile should be downloaded and verified for complete accuracy.

## 4. What do we require when documenting the source

When documenting the source, the meta data must be accurately filled out and placed in the zip file so others can access it.

[This page describes what must be included in the `meta.txt` file](https://wmgeolab.github.io/gbDocs/10-workflow-overview/deliverables-and-artifacts/), specifically under the meta data file in the Output section.

Here is an example using Angola ADM0.

```
Boundary Representative of Year: 2021
ISO-3166-1 (Alpha-3): AGO
Boundary Type: ADM0
Canonical Boundary Type Name: República de Angola
Source 1: Open Street Map
Source 2: 
Release Type: gbOpen 
License: Creative Commons Attribution-ShareAlike 2.0
License Notes: 
License Source: https://osm-boundaries.com/Documentation
Link to Source Data: https://osm-boundaries.com/ 
Other Notes: 
```
