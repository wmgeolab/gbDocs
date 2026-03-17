# Source Evaluation Rubric

## Rubric to follow

| Decision | License / Creator | Metadata | Data |
|----------|------------------|----------|------|
| **Accept** | National Mapping Agency with Public Domain License | Complete | Clean polygons with a complete attribute table |
| **Conditional (Possible to make edits)** | License is not listed (Contributor reaches out to data owner) | Partial (Contributor fills in) | Data is accurate but is missing attribute table information (Contributor fixes attribute table) |
| **Reject** | Blog/unknown source with no license | None available | Data is completely inaccurate and has discrepancies with other sources |
---

## Deciding whether a source is acceptable to use

The datasets we incorporate into the GeoBoundaries dataset have to be openly licensed so that we can redistribute and not get yelled at. If a source does not have an appropriate license, for example, a source that does not allow the commercial usage of their data would be considered an unacceptable source. 

### Unacceptable Sources

A source is considered **unacceptable** if it meets any of the following criteria:

- No clear metadata is available.
- License restrictions prevent usage (e.g., non-commercial only).
- Polygons are oversimplified or lack accuracy.
- Administrative division (ADM) levels differ from other reliable sources.
- Source is outdated and lacks temporal relevance.

---

### Sites Commonly Not Allowed

The following sources are **not acceptable**:

- GADM
- earthworks.stanford.edu
- maps.princeton.edu
- geodata.lib.berkeley.edu
- OpenStreetMap
- humdata/hdx
- Any source with a license that includes “sharealike”

These types of data licenses help us deduce whether or not a source is acceptable or not:

  - **Public Domain**: Most open of them all, free to share, create, and adapt, no attribution needed. This is the best kind of license available, and we absolutely want to include data like this. 
Some sources are under this license, but they aren’t found as often in the wild
  - **Creative Commons**: all creators of data retain copyright while allowing others to copy, distribute, and make uses of their work (https://creativecommons.org/licenses/). There are lots of different versions of this license, but (almost) all allow us to copy, tweak, and redistribute non-commercially at least. When coming across this license, make sure that we have the legal ability to make changes (i.e. change geometry or attribute table) and redistribute for free. 
A lot of the data on government portals are under this license
Be sure to avoid Share-alike clauses

- [List of licenses we **can** and **cannot** use](https://github.com/wmgeolab/gbDocs/blob/main/docs/Licenses%20for%20gB%20Open.md)  

> **Note:** This list is not comprehensive. Notify the team if a new license type is found.

### Acceptable Sources

A source is considered **acceptable** if it meets all of the following criteria:

1. Provides a license that allows usage for **all purposes** (commercial, educational, etc.).
2. Contains data that we are able to supply, but for which **geoBoundaries currently does not provide boundaries**.
3. Includes **relevant boundary information** that improves or updates the boundary compared to what geoBoundaries already has.

> Once all of these criteria are satisfied, the shapefile should be **downloaded** and **verified** for complete accuracy before proceeding.
### A **curator** may need to intervene or give input on a source's credibility if there are:
  - Conflicting official sources
  - Political boundary disputes
  - Other issues that make source evaluation unclear


