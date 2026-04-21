# Acceptance Criteria

This page defines the conditions that must be met for a boundary dataset to be accepted into the repository.

All criteria must be satisfied before a dataset can be approved and merged.

---

## Core Requirement

> A dataset is accepted only if it meets **all quality, structural, and licensing standards**.

---

## 1. Source and Licensing

- Source is clearly identified and documented in the `licence.png` file
- License allows redistribution and use (including commercial use)
- `license.png` is included and matches the source
- Source corresponds to the submitted data

→ See: [Licensing and Permissions](../20-research-and-sourcing/licensing-and-permissions.md)

---

## 2. Geometry Quality

- No gaps between polygons
- No overlapping polygons
- No unintended slivers
- Geometry is valid (no self-intersections)
- Boundaries are not overly simplified or pixelated

→ See:  
- [Common Errors and Fixes](../50-geometry-fixes-and-standards/common-errors-and-fixes.md)  
- [Multipart, Slivers, Gaps, Overlaps](../50-geometry-fixes-and-standards/multipart-slivers-gaps-overlaps.md)

---

## 3. Geographic Accuracy

- Boundaries match the source data
- Coastlines, lakes, and enclaves are handled correctly
- No visible misalignment with basemap
- All regions are correctly represented

→ See: [Coastlines, Lakes, Enclaves](../50-geometry-fixes-and-standards/coastlines-lakes-enclaves.md)

---

## 4. Projection

- Dataset uses **WGS 1984 (EPSG:4326)**
- No projection-related distortion or misplacement

→ See: [Projection and Precision](../50-geometry-fixes-and-standards/projection-and-precision.md)

---

## 5. Attribute Table

- Required fields are present:
  - `Name`
  - `Level`
  - `ISO_Code` (if applicable)
- Field names and types are correct
- No missing or null values
- ISO codes are accurate and properly assigned

→ See: [Attribute Schema](../40-qgis-user-manual/attribute-schema.md)

---

## 6. Completeness

- All administrative units are included
- No missing polygons
- Islands and multipart features are correctly handled

---

## 7. File Structure and Naming

- Files follow naming convention: `ISO_ADM#`
- GeoJSON is correctly formatted
- `meta.txt` is complete
- `license.png` is included
- All files are packaged in a `.zip` folder

→ See: [Project Structure](../40-qgis-user-manual/project-structure.md)

---

## 8. Consistency

- Level of detail is consistent across the dataset
- Naming conventions are uniform
- Data aligns with geoBoundaries standards

→ See: [Generalization vs. Fidelity](../50-geometry-fixes-and-standards/generalization-vs-fidelity.md)

---

## Automatic Rejection Conditions

A dataset should be rejected if:

- License is missing or unacceptable
- Source is unreliable or unverifiable
- Geometry is severely inaccurate or incomplete
- Required files are missing
- Issues cannot be reasonably corrected

---

## Final Decision

A dataset may be:

- **Accepted** → All criteria are met  
- **Revised** → Issues identified, requires changes  
- **Rejected** → Does not meet standards and cannot be fixed  

---

## Summary

- All criteria must be met for acceptance  
- No single category can be skipped  
- Acceptance decisions should be consistent and based on documented standards  

Clear acceptance criteria ensure fairness, consistency, and high-quality data across the repository.
