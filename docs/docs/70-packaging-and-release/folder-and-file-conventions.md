# Folder and File Conventions

This page defines the required folder structure and file naming conventions for all boundary datasets.

Following these conventions ensures consistency, clarity, and compatibility across the repository.

---

## Root Folder Naming

Each dataset must be packaged in a folder using the format:

`ISO_ADM#`

### Examples

- `USA_ADM0`
- `BRA_ADM1`
- `VNM_ADM2`

---

## Required Files

Each folder must contain the following files:

- `ISO_ADM#.geojson` → boundary data  
- `meta.txt` → metadata information  
- `license.png` → screenshot of source license  

### Example Structure

USA_ADM1/
├── USA_ADM1.geojson
├── meta.txt
├── license.png


---

## File Naming Rules

### GeoJSON File

- Must match the folder name exactly  
- Format: `ISO_ADM#.geojson`

### Metadata File

- Must be named exactly: `meta.txt`

### License File

- Must be named exactly: `license.png`

---

## Naming Standards

- Use **uppercase ISO codes** (e.g., `USA`, `BRA`)
- Use **ADM levels** in the format `ADM#`
- Do not include spaces or special characters
- Keep naming consistent across all files

---

## What to Avoid

- Incorrect file names (e.g., `usa_adm1.geojson`)
- Extra or unnecessary files in the folder
- Mismatched folder and file names
- Missing required files

---

## Packaging

Before submission:

- Ensure all required files are present
- Confirm naming conventions are followed
- Compress the folder into a `.zip` file

The `.zip` file should also be named:

`ISO_ADM#.zip`

---

## Summary

- Folder name must follow `ISO_ADM#`
- All required files must be included
- File names must match exact conventions
- Consistency is required for all submissions

Proper file structure ensures datasets can be easily reviewed, stored, and published.
