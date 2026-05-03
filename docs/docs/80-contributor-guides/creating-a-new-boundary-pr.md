# Creating a New Boundary PR

This document outlines the submission process for creating a new boundary pull request (PR) in the geoBoundaries contribution workflow.

---

## Submission Link

All boundary submissions must be uploaded through the official submission portal:

[https://www.geoboundaries.org/gbContribute.html](https://www.geoboundaries.org/gbContribute.html)

---

## Submission Page Overview

The submission page is where contributors upload their zipped boundary files and provide required metadata.

![Submission Page](https://github.com/user-attachments/assets/1958490e-9e95-41e8-9627-c2867e3e7776)

---

## Linking a Zip File

After navigating to the submission page, you will upload your boundary dataset as a ZIP file. Once the ZIP file is successfully uploaded, the system will process it and display details for the contributor to fill out.

![After Upload Upload Confirmation](https://github.com/user-attachments/assets/fbefb651-2fca-44a8-ae4d-493f905aae19)

---

## Filled Out ZIP File Information

This section shows the information that is required from the contributor.

![ZIP File Information](https://github.com/user-attachments/assets/7fb211d2-e7cd-4535-8c22-7ca8fae1e84b)

---

## Metadata Screenshot

The metadata section includes key descriptive information about the dataset, such as administrative level, country, source details, etc.

![Metadata Section](https://github.com/user-attachments/assets/b6520784-6d96-4d48-b1d5-99d77ab0fa9c)

---

## Contributor Information

Contributors must provide their personal and/or institutional details for attribution and follow-up purposes.

![Contributor Information](https://github.com/user-attachments/assets/bff44ce6-79f4-4b67-9e80-125c88c7778c)

---

## After Submission: Pull Request Creation & Automated Checks

After you submit your boundary ZIP file, the system takes a few minutes to process your submission. Once processing is complete, a new pull request (PR) is automatically created in the geoBoundaries repository.

<img width="899" height="511" alt="image" src="https://github.com/user-attachments/assets/48fbbdd5-50aa-45b0-960b-62fa2b91d31b" />

## Viewing Your Pull Request

Once your submission is processed, navigate to the generated PR to review its status and validation results.

You can view all pull requests here: https://github.com/wmgeolab/geoBoundaries/pulls

## Checking Automated Validation Results

Each pull request runs a set of automated validation checks. To verify whether your submission passed:

- Open your pull request page.


<img width="929" height="212" alt="image" src="https://github.com/user-attachments/assets/01f2a419-40d4-484b-a9f0-6aef9276dc1c" />


- Click the Checks section.


<img width="488" height="370" alt="image" src="https://github.com/user-attachments/assets/b9f05306-5b0e-4d9b-a462-e8e8aab824a0" />


- Review the status of the automated validation jobs.

Typically, there are 4 automated checks that run on every submission. 

1. geoBoundaryZipfileChecks
2. geoBoundaryMetaDataCheck
3. geoBoundaryDataCheck
4. prResponse

Each check will show one of the following statuses:

✅ Green checkmark: Passed successfully

❌ Red X: Failed and requires correction

⏳ Hour Glass: Still running

All checks must pass for the pull request to be approved and merged.

## Summary

To successfully submit a new boundary PR:

- Visit the submission portal.
- Upload your ZIP file.
- Complete metadata fields.
- Provide contributor information.
- Ensure automated checks passed.

Ensure all required fields are completed accurately before final submission.
