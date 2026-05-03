# Metadata Requirements

This page defines the required structure and content of the `meta.txt` file.

The metadata file provides essential information about the dataset, including its source, licensing, and structure. It is required for all submissions.

---

## Purpose

The `meta.txt` file ensures that each dataset is:

- Transparent in its origin
- Properly licensed
- Reproducible and verifiable
- Consistent with geoBoundaries standards

---

## Metadata File

Within the `meta.txt` file, there are several subfields that describe the data:

```text
Boundary Representative of Year: Year of data creation, publication, or most recent update.

ISO-3166-1 (Alpha-3): ISO 3-letter country code 

Boundary Type: Administrative Division level (0-5+)

Canonical Boundary Type Name: The local name for the ADM (ex - USA ADM 1 would have “state” here), for ADM 0 make sure to put what the country calls itself (ex - Germany calls itself Deutschland, so we’d enter “Deutschland”)

Source 1: The site name for where the shapefile comes from (geoBoundaries if digitized)

Source 2: Secondary source name (if applicable)

Release Type: What gB release category (or categories) the shapefile falls into (gbOpen, gbHumanitarian, or gbAuthoritative)

License: License type name (note this is case sensitive)

License Notes: Notes on the license (if applicable)

License Source: Link to the page on the website that details the license information

Link to Source Data: Link to the page where the shapefile can be found

Other Notes: Any other relevant information (if applicable)
```

### Example

<img width="708" height="271" alt="image" src="https://github.com/user-attachments/assets/96958e45-514d-4784-b7d4-8bea08de2e0e" />

## Formatting Requirements

- Each field must be included, even if marked as not applicable
- Use consistent field names exactly as shown above
- Separate each field with a new line
- Use plain text format (.txt)
- Do not add extra fields unless necessary
- Required vs Optional Fields
- Required Fields

---

The following fields must always be completed:

- Boundary Representative of Year
- ISO-3166-1 (Alpha-3)
- Boundary Type
- Canonical Boundary Type Name
- Source 1
- Release Type
- License
- License Source
- Link to Source Data

---

Optional Fields

These fields may be left blank or marked as N/A if not applicable:

- Source 2
- License Notes
- Other Notes

---

Best Practices
- Ensure all links are valid and accessible
- Match metadata values to the dataset exactly
- Use official names and terminology where possible
- Double-check ISO codes and ADM levels
- Keep descriptions concise but informative

---

Common Issues
- Missing required fields
- Incorrect or inconsistent field names
- Broken or missing links
- License information that does not match license.png
- Vague or incomplete source descriptions

---

## Summary
- The meta.txt file is required for all datasets
- All required fields must be completed accurately
- Metadata must match the dataset and its source
- Proper metadata ensures usability, transparency, and compliance

Accurate metadata is essential for maintaining high-quality and reliable geospatial data.
