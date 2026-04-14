# QGIS Troubleshooting

This page covers common issues in QGIS and how to resolve them.  
For more detailed guidance, refer to the official QGIS documentation linked throughout.

---

## Data Will Not Load

**Possible causes:**
- File is still compressed (`.zip`)
  
- Missing shapefile components
  
- Unsupported format

**Fix:**
- Extract the file before loading
  
- Use **Layer → Add Layer → Add Vector Layer**

[More help located on the QGIS Documentation Page](https://docs.qgis.org/3.44/en/docs/user_manual/managing_data_source/opening_data.html)

---

## Layer Appears in the Wrong Location

**Cause:** Incorrect Coordinate Reference System (CRS)

**Fix:**
- Right-click layer → **Set Layer CRS**

- Select **WGS 1984 (EPSG:4326)**

[More help located on the QGIS Documentation Page](https://docs.qgis.org/3.44/en/docs/user_manual/working_with_projections/working_with_projections.html)

---

## Cannot Edit Layer

**Cause:** Editing mode is off

**Fix:**
- Click **Toggle Editing** (pencil icon)

---

## Attribute Table Issues

**Common problems:**
- Cannot edit fields
  
- Missing required fields

**Fix:**
- Enable editing mode
  
- Refer to the [Attribute Schema](https://wmgeolab.github.io/gbDocs/40-qgis-user-manual/attribute-schema/)

---

## Geometry Errors

**Common problems:**
- Overlaps, gaps, or broken polygons

**Fix:**
- Run **Check Validity**
  
- Use **Fix Geometries**

[More help located on the QGIS Documentation Page](https://docs.qgis.org/3.44/en/docs/user_manual/processing_algs/qgis/vectorgeometry.html)

---

## Export Not Working

**Fix:**
- Ensure geometry is valid
  
- Export as **GeoJSON**
  
- Check file name and location (`ISO_ADM#`)

---

## QGIS Running Slowly

**Fix:**
- Remove unnecessary layers
  
- Restart QGIS
  
- Save frequently

---

## Need More Help?

- [QGIS Documentation](https://docs.qgis.org/3.44/en/docs/index.html)
  
- [QGIS Training Manual](https://docs.qgis.org/3.44/en/docs/training_manual/)

---

## Summary

Most issues can be resolved by checking:

- CRS (projection)
  
- Editing mode
  
- File structure

If problems persist, revisit earlier workflow steps or ask a team lead.
