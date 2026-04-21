# Manual Review Checklist

This checklist is used to evaluate boundary datasets after automated checks have been completed.

Manual review ensures that the data is accurate, complete, and aligned with geoBoundaries standards.

---

## How to Use This Checklist

- Confirm that all criteria are met
- If any item fails, the dataset should be **revised** before approval

---

## 1. Source and Licensing

- [ ] Source is clearly identified in the included (`licence.png`) file
- [ ] License is acceptable for use and redistribution under all purposes including commercial
- [ ] License screenshot (`license.png`) is included
- [ ] Source matches the dataset provided

→ See: [Licensing and Permissions](../20-research-and-sourcing/licensing-and-permissions.md)

---

## 2. Geometry Quality

- [ ] No gaps between polygons (unless gaps do truly exist in the boundary)
- [ ] No overlapping polygons
- [ ] No slivers or unintended small polygons
- [ ] Geometry is valid (no self-intersections)
- [ ] Boundaries appear smooth and precise (not pixelated)

→ See:  
- [Common Errors and Fixes](../50-geometry-fixes-and-standards/common-errors-and-fixes.md)  
- [Multipart, Slivers, Gaps, Overlaps](../50-geometry-fixes-and-standards/multipart-slivers-gaps-overlaps.md)

---

## 3. Geographic Accuracy

- [ ] Boundaries match the source data
- [ ] Coastlines are correctly represented with adequate precision
- [ ] Lakes and inland water boundaries are handled appropriately
- [ ] Enclaves/exclaves are included and correctly assigned
- [ ] No obvious misalignments with basemap

→ See: [Coastlines, Lakes, Enclaves](../50-geometry-fixes-and-standards/coastlines-lakes-enclaves.md)

---

## 4. Projection and Alignment

- [ ] CRS is **WGS 1984 (EPSG:4326)**
- [ ] No distortion or shifting of boundaries

→ See: [Projection and Precision](../50-geometry-fixes-and-standards/projection-and-precision.md)

---

## 5. Attribute Table

- [ ] Required fields are present:
  - `Name`
  - `Level`
  - `ISO_Code` (Required for ADM1 and below)
- [ ] Field names are correctly formatted
- [ ] No empty or null values
- [ ] ISO codes are correct and unique where required
- [ ] Attribute values match the source data

→ See: [Attribute Schema](../40-qgis-user-manual/attribute-schema.md)

---

## 6. Completeness

- [ ] All administrative units are included
- [ ] No missing regions or polygons
- [ ] Islands are included where applicable

---

## 7. File Structure and Naming

- [ ] File is named using `ISO_ADM#`
- [ ] GeoJSON file is correctly formatted
- [ ] `meta.txt` is included and complete
- [ ] `license.png` is included
- [ ] Files are packaged in a `.zip` folder

→ See: [Project Structure](../project-structure.md)

---

## 8. Consistency

- [ ] Level of detail is consistent across the dataset
- [ ] Naming conventions are consistent
- [ ] No mixing of different data sources without justification in the notes section of the `meta.txt` file

→ See: [Generalization vs. Fidelity](../50-geometry-fixes-and-standards/generalization-vs-fidelity.md)

---

## Final Decision

- [ ] **Approve** — Dataset meets all requirements
- [ ] **Revise** — Issues identified and commented, needs correction
- [ ] **Reject** — Does not meet standards or source is unacceptable

---

## Summary

- Manual review verifies quality beyond automated checks
- Focus on geometry, attributes, and source integrity
- All checklist items must be satisfied before approval

A thorough review ensures that datasets are reliable, consistent, and ready for use.
