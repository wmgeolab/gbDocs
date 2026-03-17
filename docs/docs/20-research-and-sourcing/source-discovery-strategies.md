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

### Other Helpful Search Methods

- Search using the **official language of the country**.
- Search for "**country name** open data portal". Some countries (or regional organizations) maintain centralized websites that host collections of public datasets.

  Look for categories such as:
  - **Administrative Divisions**
  - **Territories**
  - **Geography**

  Note that these portals may not always label datasets clearly. Administrative boundaries may appear under other categories, such as:

  - Census data
  - Health data
  - Political or electoral data

  In many cases, these datasets are organized by **ADM level**.

---

### Places to Look for Boundary Data

- **Government websites**
- **Census bureaus**
- **National mapping agencies**

- **GitHub**  
  GitHub is a platform where individuals and organizations share datasets and code. It can sometimes contain useful shapefiles.  
  If you find a suitable dataset on GitHub, you must **contact the creator to confirm that redistribution is permitted**.

- **Academic papers and research websites**
  - If you find a map showing administrative boundaries but no downloadable shapefile, check the **bibliography or references**.
  - Authors often cite the original source where the dataset can be downloaded.

- **Constitutions and other official government documents**  
  These can help confirm the **official structure and naming of administrative divisions**, even if they do not provide shapefiles directly.
