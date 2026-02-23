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
