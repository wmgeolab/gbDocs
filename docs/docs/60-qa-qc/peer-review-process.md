# Peer Review Process

This page outlines the process for reviewing submitted boundary datasets through GitHub pull requests (PRs).

Peer review ensures that all data meets geoBoundaries standards before being accepted into the repository.

---

## Roles

### Contributor
- Submits a dataset via the geoBoundaries submission website
- Ensures files meet formatting and documentation requirements
- Responds to reviewer feedback

### Reviewer
- Evaluates the submission for quality and completeness
- Provides feedback and requested changes
- Approves or rejects the submission

---

## Review Workflow

### 1. Submission

- Contributor submits a completed boundary through the geoBoundaries website
- The submission includes:
  - GeoJSON file (`ISO_ADM#`)
  - `meta.txt`
  - `license.png`

---

### 2. Initial Review

The reviewer performs a high-level check:

- File structure and naming, ensuring files match the required `ISO_ADM#` format
- Presence of required files (GeoJSON file (`ISO_ADM#.geoJSON`), `meta.txt`, `license.png`)

If major components are missing:
- Request changes immediately before deeper review

---

### 3. Detailed Review

The reviewer evaluates the dataset using the  
[Manual Review Checklist](./manual-review-checklist.md)

Key areas include:

- Geometry quality
- Attribute table accuracy
- Projection and alignment
- Source and licensing

---

### 4. Feedback and Revisions

If issues are found:

- Reviewer leaves **clear, specific comments** on the PR
- Contributor revises the dataset and resubmits the edited boundary
- Reviewer re-checks the updated version

This process may repeat until standards are met.

---

### 5. Decision

After review, the reviewer selects one of the following:

#### Approve
- Dataset meets all standards
- Ready to be merged

#### Request Changes
- Issues remain that must be fixed
- Contributor must revise before approval

#### Reject
- Dataset cannot be corrected (e.g., unacceptable license)

---

## Review Best Practices

### For Reviewers

- Be clear and specific in feedback
- Reference documentation when possible
- Focus on standards

---

### For Contributors

- Address all reviewer comments
- Ask for clarification if needed

---

## Common Review Outcomes

- Minor fixes → quick approval after revision  
- Moderate issues → 1–2 revision cycles  
- Major issues → rejection or restart with new source  

---

## Summary

- Peer review ensures consistent data quality
- Reviewers evaluate submissions using defined standards
- Contributors and reviewers collaborate to improve datasets
- Only approved datasets are merged into the repository

A clear and consistent review process is essential for maintaining high-quality geospatial data.
