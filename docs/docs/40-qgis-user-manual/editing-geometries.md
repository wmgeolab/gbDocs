# Editing Geometries

This page covers how to modify and correct boundary geometries in QGIS.

Geometry editing is necessary when:

- Boundaries are inaccurate or misaligned
- Polygons contain gaps or overlaps
- Shapes are incomplete or broken
- Administrative divisions need to be split or merged

---

## Entering Edit Mode

Before making any changes:

1. Right-click the layer in the **Layers panel**
2. Select **Toggle Editing**

- The layer is now editable and editing tools will become available.

When finished:

- Click **Save Edits**
- Toggle editing off

---

## Common Editing Tasks

### Moving Vertices

Used to correct boundary alignment.

1. Select the **Vertex Tool**
2. Click on a polygon
3. Drag vertices to adjust the boundary

---

### Adding or Removing Vertices

- **Add vertex**: Click on an edge
- **Delete vertex**: Right-click a vertex and remove it

Use this to refine shape accuracy.

---

### Splitting Polygons

Used when one polygon should be divided into multiple units.

1. Select the **Split Features Tool**
2. Draw a line across the polygon
3. Confirm the split

---

### Deleting Features

Used to remove incorrect or duplicate polygons.

1. Select the feature
2. Press **Delete** or use the delete tool

---


[This page](https://wmgeolab.github.io/gbDocs/40-qgis-user-manual/snapping-and-shared-borders/) discusses Snapping and Merging in detail.

### Merging Polygons

Used when multiple polygons should be combined.

1. Select multiple features
2. Right-click → **Merge Selected Features**

### Snapping and Precision

To ensure clean boundaries:

- Enable **Snapping**
- Snap vertices to nearby edges or points

This prevents:

- Gaps between polygons
- Overlapping boundaries

---

## Topology Best Practices

Good geometry must:

- Have no gaps between adjacent polygons
- Have no overlaps
- Share clean borders
- Fully cover the intended area

---

## Validating Geometry

Before proceeding:

1. Open **Processing Toolbox**
2. Search for **Check Validity**
3. Run the tool on your layer

Fix any errors identified.

---

## Visual Inspection

Zoom in and inspect:

- Borders between adjacent polygons
- Corners and edges
- Coastal or irregular boundaries

Look for:

- Jagged or pixelated edges
- Misalignment with reference data
- Missing regions

---

## Common Mistakes

- Forgetting to enable editing mode
- Not saving edits
- Creating overlaps between polygons
- Leaving gaps between regions
- Over-editing (making shapes less accurate)

---

## Summary

- Enter edit mode before making changes
- Use vertex tools to adjust boundaries
- Split or merge polygons when needed
- Ensure clean topology (no gaps or overlaps)
- Validate geometry before moving forward

Accurate geometry is critical to producing high-quality boundary data.
