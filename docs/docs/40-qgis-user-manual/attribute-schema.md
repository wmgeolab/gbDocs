# Attribute Schema

This page defines the required structure of the attribute table for all boundary datasets.

A correctly formatted attribute table ensures consistency, usability, and compatibility across geoBoundaries data.

---

## Overview

Each boundary file must include a standardized attribute table with specific required fields.

Even if the source data contains many columns, only a subset is needed. Extra or unnecessary fields should be removed.

If you are working with a boundary file obtained through research, you should begin by reviewing the existing attribute table to ensure that all required fields (`Name`, `Level`, and `ISO_Code`) are present, correctly formatted, and fully populated. In many cases, these fields may already exist but require cleaning, renaming, or standardization. However, if you created the boundary file from scratch through digitization, the attribute table will likely be empty or incomplete. In this case, you must manually create each required field and populate it according to the schema outlined below.

---

## Opening the Attribute Table

To view the attribute table in QGIS:

1. Right-click the layer in the **Layers panel**

<img width="451" height="681" alt="image" src="https://github.com/user-attachments/assets/f09637d7-cd0a-4124-9bcb-5639d5c91841" />

2. Select **Open Attribute Table**

---

## Identifying Existing Fields

Before making changes:

- Identify which column contains the **names of administrative divisions**
- Determine whether required fields already exist
- Plan whether to **rename** or **create new fields**

---

## Entering Edit Mode

To modify the attribute table:

1. Click the **Toggle Editing** button (pencil icon)

<img width="1505" height="782" alt="image" src="https://github.com/user-attachments/assets/c1553e10-8427-4d26-b942-9cd380403bcb" />

2. The table is now editable

---

## Required Fields

The following fields must exist in every dataset:

### Name

- Field name: `Name`
- Type: **Text**
- Length: **50**

**Description:**
- Contains the name of each administrative unit
- Should match official naming conventions

---

### Level

- Field name: `Level`
- Type: **Text**
- Length: **10**

**Description:**
- Indicates the administrative level
- Format: `ADM#` (e.g., `ADM1`, `ADM2`)

---

### ISO_Code

- Field name: `ISO_Code`
- Type: **Text**
- Length: **10**

**Applies to:**
- Required for **ADM1 and below**

**Description:**
- For **ADM0**: use the country ISO code
- For **ADM1**: use **ISO 3166-2 codes** (unique per feature)
- For lower levels: follow project-specific guidance if applicable

Reference:  
ISO codes can be found using the [ISO Online Browsing Platform](https://www.iso.org/obp/ui/#home)

---

## Adding New Fields

To add a field:

1. Ensure editing mode is enabled
2. Click **Add Field** (bottom of the attribute table window)
3. Enter:
   - Field name
   - Type (**Text**)
   - Length (as specified above)
4. Click **OK**

Repeat for each required field.

---

## Modifying Existing Fields

If a similar field already exists:

- Rename it to match the required field name
- Ensure the data type and length are correct
- Verify that the data is accurate and complete

---

## Removing Unnecessary Fields

After creating the required fields:

1. Right-click the column header (or field name)
2. Select **Delete Field**
3. Save edits

Only required fields should remain unless otherwise specified.

---

## Populating Fields

### Name Field

- Use the existing column that contains administrative names
- Use **Field Calculator** to copy values if needed

---

### Level Field

- Assign the same value to all rows:
  - Example: `"ADM2"`

---

### ISO_Code Field

- For ADM0:
  - Use the country ISO code (e.g., `"USA"`)

- For ADM1:
  - Use ISO 3166-2 codes (e.g., `"US-VA"`)

- Each feature must have a **unique code**

---

## Common Mistakes

- Incorrect field names (must match exactly)
- Wrong data type (must be Text)
- Missing required fields
- Duplicate ISO codes for ADM1
- Leaving unnecessary fields in the table
- Not saving edits

---

## Final Checklist

Before proceeding, confirm:

- [ ] All required fields exist (`Name`, `Level`, `ISO_Code`)
- [ ] Field names are spelled and capitalized correctly
- [ ] Field types and lengths are correct
- [ ] Values are populated correctly
- [ ] No extra fields remain
- [ ] Edits have been saved

---

## Summary

- Standardized attribute tables are required for all datasets
- Only specific fields should be included
- Naming, types, and values must follow strict guidelines

A correct attribute schema is essential for ensuring consistency across geoBoundaries data.
