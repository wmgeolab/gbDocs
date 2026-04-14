# Projection and Precision

This page defines the required standards for coordinate reference systems (CRS) and geometric precision in boundary datasets.

Ensuring correct projection and appropriate precision is essential for maintaining consistency and accuracy across geoBoundaries data.

---

## Projection (CRS)

### Required Standard

All boundary files must use:

- **WGS 1984**
- **EPSG:4326**

This is the standard geographic coordinate system used across geoBoundaries.

---

### Why This Matters

Using a consistent CRS ensures:

- Alignment across datasets
- Compatibility with web mapping tools
- Accurate geographic positioning

---

### Common Issues

- Data appears in the wrong location
- Layers do not align with basemaps
- CRS is missing or incorrectly defined

---

### Fix

- Set or reproject the layer to **WGS 1984 (EPSG:4326)**

→ See: [End-to-End Pipeline (Projecting the Shapefile)](../10-workflow-overview/end-to-end-pipeline.md)  
→ See: [QGIS Documentation – Projections](https://docs.qgis.org/3.44/en/docs/user_manual/working_with_projections/working_with_projections.html)

---

## Precision

### What It Means

Precision refers to the level of detail in the geometry, including:

- Number of vertices
- Smoothness of boundaries
- Accuracy of shape representation

---

### Best Practices

- Preserve the **original level of detail** from the source data
- Avoid unnecessary simplification
- Ensure boundaries are not overly jagged or pixelated

---

### Common Issues

- Over-simplified boundaries (loss of detail)
- Excessively complex geometry (too many vertices)
- Jagged or inconsistent edges

---

### Fix

- If too simplified:
  - Find a higher-quality source
  - Re-digitize if necessary

- If overly complex:
  - Simplify carefully without losing accuracy

→ See: [Editing Geometries](../40-qgis-user-manual/editing-geometries.md)

---

## Balancing Accuracy and Simplicity

Good boundary data should:

- Accurately represent real-world geography
- Avoid unnecessary complexity
- Be consistent across the dataset

Avoid:

- Over-editing geometries
- Modifying boundaries beyond the source data

---

## Validation

Before submission:

- Confirm CRS is **WGS 1984 (EPSG:4326)**
- Inspect boundaries at multiple zoom levels
- Ensure geometry is clean and consistent

→ See: [Topology and Validity](../40-qgis-user-manual/topology-and-validity.md)

---

## Summary

- Use **WGS 1984 (EPSG:4326)** for all datasets
- Maintain appropriate geometric precision
- Avoid unnecessary simplification or over-complexity
- Validate projection and geometry before submission

Consistent projection and well-managed precision are essential for high-quality geospatial data.
