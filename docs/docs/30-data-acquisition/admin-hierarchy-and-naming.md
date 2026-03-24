# Administrative Hierachy and Naming

This page defines how administrative divisions (ADM levels) are stuctured and how they must be named within geoBoundaries.

Consistency in hierarchy and naming is essential for usability and comparability.

---

## Overview

Administrative boundaries are organized into hierarchical levels:

- **ADM0** – Country
- **ADM1** – First-level administrative divisions (e.g., states, provinces)
- **ADM2** – Second-level divisions (e.g., counties, districts)
- **ADM3+** – Lower-level subdivisions (varies by country)

Each country must correctly identify and represent its ADM level, as they may differ country to country.

---

## Important notes:
- Names and structures differ across countries.
- Not all countries have the same number of ADM levels.
- Some levels may be skipped or combined.
- It is helpful to rely on **official government definitions** when determining hierarchy.

## Identifying the Correct ADM Level

To determine the correct ADM level:

- Review official government sources
- Check how the country defines its administrative structure
- Compare with multiple authoritative sources if needed

## ISO Code Naming Convention

All datasets must follow the **ISO_ADM# format**.

### Examples

- `USA_ADM0`
- `BRA_ADM1`
- `VNM_ADM2`

### Rules

- Use the **3-letter ISO country code** (ISO 3166-1 alpha-3)
- Use uppercase letters
- Replace `#` with the ADM level number
- Do not include spaces

---

## File Naming Standards

All files within a dataset should follow consistent naming:

### Required Naming

- Shapefile: `ISO_ADM#`
- Example: `KEN_ADM2.shp`

---
