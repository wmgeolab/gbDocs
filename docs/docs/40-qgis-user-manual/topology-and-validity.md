# Topology and Validity

While the [Editing Geometries](https://wmgeolab.github.io/gbDocs/40-qgis-user-manual/editing-geometries/) page reviewed **how** to fix polygons and what tools to use, this Topology and Validity page will review how to check if the polygons are correct qualitatively.

# Topology and Validity

This page explains how to ensure that boundary geometries are **topologically correct** and **valid** before submission.

Topology refers to how geometries relate to one another, while validity ensures that each individual geometry is correctly formed.

---

## Why This Matters

Even if a dataset looks correct visually, it may still contain technical errors that can:

- Break analyses
- Cause issues in GIS software
- Lead to rejection during review

All geometries must pass both **visual inspection** and **technical validation**.

---

## Common Topology Errors

### Gaps (unless gaps do truly exist in the boundary)

- Empty spaces between adjacent polygons 
- Occur when boundaries do not align perfectly

### Overlaps (unless OVerlaps do truly exist in the boundary)

- Two polygons cover the same area
- Causes duplication and incorrect data representation

### Self-Intersections

- A polygon crosses over itself
- Creates invalid geometry

### Duplicate Geometries

- Identical polygons exist more than once

---

## What Good Topology Looks Like

A valid dataset should:

- Have **no gaps** between adjacent boundaries
- Have **no overlaps**
- Have **clean, shared borders**
- Fully cover the intended geographic area

---

## Checking Geometry Validity in QGIS

1. Open the **Processing Toolbox**

<img width="429" height="317" alt="image" src="https://github.com/user-attachments/assets/2f50f274-a4c4-44b6-afc3-f18f4ff75232" />

2. Search for **Check Validity**

<img width="230" height="252" alt="image" src="https://github.com/user-attachments/assets/b1a1c5ca-95dd-4ec9-83db-4d07c1d2b64f" />

3. Select your layer as the input

<img width="515" height="407" alt="image" src="https://github.com/user-attachments/assets/ce017a95-6467-4497-9b10-efa6b32c3d99" />

4. Run the tool
5. Check to see if the layer is valid.

<img width="299" height="317" alt="image" src="https://github.com/user-attachments/assets/047378d5-61ab-4c0b-ae49-3cf781d61541" />

If the layer is invalid, use the **Fix Geometries** tool in the proccessing toolbox which is reviewed below.

### Output

The tool will identify:

- Valid features
- Invalid features
- Specific geometry errors

---

## Fixing Geometry Errors

### Fix Geometries Tool

1. Open **Processing Toolbox**
2. Search for **Fix Geometries**
3. Run the tool on your layer

This automatically repairs many common issues.

---

### Manual Fixes

If errors persist:

- Use the **Vertex Tool** to adjust shapes
- Snap vertices to neighboring boundaries
- Remove duplicate features
- Redraw problematic polygons if necessary

---

## Snapping Settings

Enable snapping to improve precision:

- Turn on **Snapping Toolbar**
- Set snapping to:
  - Vertex
  - Segment

This helps ensure boundaries align correctly.

---

## Visual Inspection

After fixing errors:

- Zoom into borders between polygons
- Check for:
  - Gaps
  - Overlaps
  - Misaligned edges

Pay special attention to:

- Coastal boundaries
- Complex borders
- Small or irregular regions

---

## Common Mistakes

- Not running the **Check Validity** tool
- Ignoring small gaps or overlaps
- Overusing automatic fixes without checking results

---

## Final Validation Checklist

Before submission, confirm:

- [ ] No gaps between polygons
- [ ] No overlaps between polygons
- [ ] All geometries are valid
- [ ] No duplicate features
- [ ] Boundaries align cleanly

---

## Summary

- Topology ensures boundaries relate correctly to each other
- Validity ensures each geometry is technically correct
- Always run validation tools and perform visual checks

Clean topology is essential for producing reliable and usable boundary data.

