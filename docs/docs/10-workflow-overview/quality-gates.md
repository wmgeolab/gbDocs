# Quality Gates

This document outlines the standards used to assess whether a boundary dataset is ready for inclusion.

Quality gates ensure consistency, accuracy, and usability across all administrative boundary contributions.

---

## 1. Assessing Inclusion for a New Boundary

Before technical checks begin, we assess whether the boundary should be included at all.

### Representation Standard

- Does the boundary represent the country as it represents itself?
- Is the source official or widely recognized?
- Does it reflect current administrative reality?

---

## 2. Source Validation

### Triangulation of Sources

All boundaries should be validated using multiple sources when possible.

- Government publications
- Official statistical offices
- Authoritative mapping agencies
- Academic or internationally recognized datasets

If sources disagree:
- Document discrepancies
- Explain why one source was prioritized in the notes of the `meta.txt` file

---

## 3. Projection and Geometry Standards

### Projection

- Data must use the required coordinate reference system (typically WGS 1984).
- Projection must be verified before submission.

### Geometry Quality

- No invalid geometries
- No self-intersections
- No unclosed polygons
- No duplicate features

---

## 4. Visual Inspection

Some issues cannot be caught automatically and require human review.

### Pixelated Boundaries

We question boundaries that appear:

- Overly simplified
- Excessively jagged
- Suspiciously pixelated
- Clearly raster-derived without proper smoothing

If geometry looks unusual:
- Re-check the source
- Confirm resolution
- Verify scale appropriateness

---

## 5. Naming Conventions

All files and attributes must follow established naming conventions.

- Zip file must be in ISO_ADM# format
- ISO codes must be correct
- ADM level must match task instructions
- Field names must match schema
- Feature names must reflect official naming

Inconsistent naming slows review and may block approval.

---

## 6. Islands and Coastal Countries

### Islands (if applicable)

Ensure:

- Islands are not accidentally removed
- Small offshore territories are included when appropriate
- Multi-part geometries are handled correctly

If islands are excluded, document why.

### Coastal Countries

Ensure:

- The shores are accurately drawn, so that they are not too jagged or too smooth either

---

## 7. What Might Be Broken

Common failure points include:

- Incorrect ADM level
- Misaligned projections
- Missing islands (if applicable)
- Attribute schema mismatches
- Broken geometries
- Incorrect ISO codes
- Zipping the wrong files

Always test the zip file before submission.

---

## 8. Automated Quantitative Checks

We implement automated validation checks, such as:

- Geometry validity tests
- ...

Automated checks assist reviewers but do not replace manual review.

---

## Final Checklist Before Submission

- [ ] Correct country and ADM level
- [ ] CRS verified
- [ ] Geometry validated
- [ ] Islands checked (if applicable)
- [ ] Naming conventions followed
- [ ] Metadata completed
- [ ] Zip file tested

Only submit once all boxes are checked.

