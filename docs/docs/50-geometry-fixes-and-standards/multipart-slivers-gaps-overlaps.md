# Multipart Features, Slivers, Gaps, and Overlaps

This page outlines key geometry issues that must be identified and resolved before submission. These issues are common in boundary datasets and are critical to data quality.

For step-by-step fixes, refer to the linked QGIS documentation pages.

---

## Multipart Features

### What They Are

A **multipart feature** is a single record in the attribute table that contains multiple disconnected polygons.

### Why This Matters

- Each administrative unit should typically be represented as a **single feature**
- Multipart features can:
  - Break analysis workflows
  - Cause inconsistencies in the dataset

### When They Are Acceptable

- When a single administrative unit is naturally composed of multiple parts (e.g., islands)

### Fix

- Use **Multipart to Singleparts** to separate features if needed

→ See: [Editing Geometries](../40-qgis-user-manual/editing-geometries.md)

---

## Slivers

### What They Are

**Slivers** are very small, thin polygons that are often created unintentionally during editing or overlay operations.

### Why This Matters

- They do not represent real administrative areas
- They introduce errors in area calculations and analysis

### Fix

- Identify and delete sliver polygons
- Merge them into the correct neighboring polygon if necessary

→ See: [Topology and Validity](../40-qgis-user-manual/topology-and-validity.md)

---

## Gaps

### What They Are

**Gaps** are empty spaces between polygons where no feature exists.

### Why This Matters

- The dataset should fully cover the administrative area
- Gaps indicate incomplete or misaligned boundaries

### Fix

- Enable **Snapping**
- Adjust vertices so polygons share borders exactly

→ See:  
- [Editing Geometries](../40-qgis-user-manual/editing-geometries.md)  
- [Topology and Validity](../40-qgis-user-manual/topology-and-validity.md)

---

## Overlaps

### What They Are

**Overlaps** occur when two or more polygons cover the same geographic area.

### Why This Matters

- Creates duplicate representation of space
- Leads to incorrect analysis results

### Fix

- Adjust boundaries to eliminate overlap
- Validate using geometry tools

→ See: [Topology and Validity](../40-qgis-user-manual/topology-and-validity.md)

---

## How to Check for These Issues

Use QGIS tools to identify problems:

- **Check Validity**
- **Fix Geometries**
- Visual inspection at high zoom levels

→ See: [Topology and Validity](../40-qgis-user-manual/topology-and-validity.md)

---

## Best Practices

- Always enable **Snapping** when editing
- Zoom in when working along shared borders
- Regularly validate geometry during editing
- Inspect small or complex regions carefully

---

## Summary

- Multipart features, slivers, gaps, and overlaps are common geometry issues
- Some (like multipart features) may be acceptable depending on context
- All others must be resolved before submission

Ensuring clean geometry is essential for producing accurate and reliable boundary data.
