# Source Evaluation Rubric

## Rubric to follow

| Criterion         | Accept | Conditional (Possible to make edits) | Reject |
|--------------|------------------|-------------------|--------------------------|
| License/Creator  | National Mapping Agency with Public Domain License | License is not listed (Contributor reaches out to data owner)| Blog/unknown source with no License |
| Metadata   |   Complete       | Partial (Contributor fills in)     | None available         |
| Data   | Clean polygons with a complete attribute table  | Data is accurate but is missing attribute table information (Contributor fixes attribute table)  | Data is completely inaccurate and has discrepencies with other sources                     |

---

## Deciding whether a source is acceptable to use

The datasets we incorporate into the GeoBoundaries dataset have to be openly licensed so that we can redistribute and not get yelled at. If a source does not have an appropriate license, for example, a source that does not allow the commercial usage of their data would be considered an unacceptable source. 

What makes a source **unacceptable**:
  - No clear metadata available
  - Unacceptable license, that says no commercial use
  - Over simplified polygons
  - Differing ADM level definitions from other sources
  - Temporal relevance, the source should not be outdated

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

### A **curator** may need to intervene or give input on a source's credibility if there are:
  - Conflicting official sources
  - Political boundary disputes
  - Other issues that make source evaluation unclear


