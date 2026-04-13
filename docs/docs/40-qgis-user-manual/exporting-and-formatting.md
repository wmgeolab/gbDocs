# Exporting and Formatting

Follow these steps to propertly export your boundary file and prepare it for submission.

## Exporting the File

1. Remove any unnecessary layers (e.g., georeferencing images or unprojected layers). Right-click the layer and select "Remove Layer".
<img width="1101" height="489" alt="Screenshot 2026-04-13 192149" src="https://github.com/user-attachments/assets/cb1c895d-d3af-4927-a64c-d8d2fa6b0010" />

---


2. Export the shapefile layer. Double click (or right-click) the shapefile layer. Select "Export" -> "Save Features as".

<img width="415" height="451" alt="image" src="https://github.com/user-attachments/assets/6dd3bcbe-1d27-4f28-b240-7f0cec9077c2" />

3. Set the export format. Choose **geoJSON** as the file format.

<img width="883" height="984" alt="image" src="https://github.com/user-attachments/assets/a827ca80-a148-4298-95d8-6777b592a5ff" />

4. Ensure that the fields match the below screenshot:
<img width="440" height="491" alt="image" src="https://github.com/user-attachments/assets/dfe14a1c-ecea-4bbd-bec6-8352f83e25ab" />

When typing the name of the shapefile, select a location for the exported file by selecting the **three dots (...)**.

<img width="472" height="127" alt="image" src="https://github.com/user-attachments/assets/78dca398-e696-4dde-b7f7-00e5d6a811b4" />

---

## Preparing Submission Files

Before compressing your files, ensure the following required files are present:

- **Boundary file(s)**
- **Metadata file** (`meta.txt`)
- **License screenshot** (`license.png`)

### meta.txt

This file description of what this file should include can be located in the [Deliverables and Artifacts](https://wmgeolab.github.io/gbDocs/10-workflow-overview/deliverables-and-artifacts/) sheet.

### license.png

- A screenshot of the license from the source website  
- Must clearly show the **license type** and **URL**  
- Must be readable and uncropped  

---

## Compressing the Files

Once all required files are ready:

1. Select all required files (boundary file(s), `meta.txt`, `license.png`).

<img width="479" height="166" alt="image" src="https://github.com/user-attachments/assets/1637e1ee-dee0-4591-ab03-7d25117e5283" />

---

2. Create a compressed folder.

- Right-click the selected files  
- Choose **Send to → Compressed (zipped) folder**

<img width="975" height="752" alt="Screenshot 2026-04-13 193340" src="https://github.com/user-attachments/assets/60ad147e-420e-41fb-894d-1f147130220c" />

---

## Final Step

- Rename the `.zip` folder using the required format: `ISO_ADM#`

---

## Final Checklist

Before submission, confirm:

- [ ] Boundary file(s) is correctly named  
- [ ] `meta.txt` is complete and accurate  
- [ ] `license.png` is included and readable  
- [ ] All files are included in the `.zip` folder  
- [ ] Folder is named correctly (`ISO_ADM#`)  

---

## Summary

- Export the boundary as a **GeoJSON** or **Shapefile**
- Include required supporting files (`meta.txt`, `license.png`)
- Compress everything into a `.zip` file
- Follow strict naming conventions for submission
