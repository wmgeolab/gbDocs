# Coastlines, Lakes, and Enclaves

This page outlines how to correctly handle complex geographic features such as coastlines, lakes, and enclaves when working with boundary data.

These features often introduce ambiguity and require careful attention to maintain accuracy and consistency.

---

## Coastlines

### What to Consider

Coastlines define the outer boundary of a country or administrative unit.

### Best Practices

- Follow the **source data exactly** — do not generalize or redraw unnecessarily
- Maintain **high-resolution detail** when available
- Ensure boundaries align with the coastline (no gaps or inland shifts)

### Common Issues

- Over-simplified coastlines
- Misalignment with basemap
- Jagged or pixelated edges

### Fix

- Adjust vertices carefully using the **Vertex Tool**
- Re-digitize if the coastline is significantly inaccurate

→ See: [Editing Geometries](../40-qgis-user-manual/editing-geometries.md)

---

## Lakes and Inland Water Bodies

### What to Consider

Administrative boundaries may:

- Follow the edge of a lake
- Extend into a lake
- Divide a lake between regions

### Best Practices

- Match the **source definition of the boundary**
- Do not assume boundaries follow the shoreline unless specified
- Ensure polygons do not unintentionally overlap water boundaries

### Common Issues

- Boundaries incorrectly cutting across lakes
- Missing water boundaries
- Misinterpretation of shared water regions

### Fix

- Verify against source data
- Adjust boundaries to match official definitions

---

## Enclaves and Exclaves

### Definitions

- **Enclave:** A territory completely surrounded by another
- **Exclave:** A territory separated from its main region

### What to Consider

These are legitimate geographic features and must be preserved.

### Best Practices

- Ensure enclaves/exclaves are:
  - Included in the correct administrative unit
  - Properly connected in the attribute table
- Multipart features may be appropriate in these cases

### Common Issues

- Enclaves missing entirely
- Assigned to the wrong administrative unit
- Incorrectly merged with surrounding regions

### Fix

- Verify using multiple sources
- Assign correct attributes
- Separate or merge features as needed

→ See: [Multipart Features](./multipart-slivers-gaps-overlaps.md)

---

## Islands

### What to Consider

Many administrative units include offshore islands.

### Best Practices

- Include all islands that belong to the administrative unit
- Maintain their correct association in the attribute table
- Use multipart features where appropriate

### Common Issues

- Missing small islands
- Islands assigned to incorrect regions

---

## General Guidance

- Always prioritize **accuracy over simplicity**
- Do not modify boundaries unless necessary
- When unsure, **cross-check multiple sources**

---

## Summary

- Coastlines must align accurately with source data
- Lakes require careful interpretation of boundaries
- Enclaves and exclaves must be preserved correctly
- Islands should be included and properly attributed

Handling these features correctly ensures geographic accuracy and consistency across datasets.
