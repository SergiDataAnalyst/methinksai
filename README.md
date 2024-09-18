# methinksAI

# Data Processing Summary

This notebook processes medical imaging data to extract relevant study information and filter it for analysis. The primary objective is to identify and analyze the earliest CT scans for each patient.

- **ContentDateTime** was created by combining `ContentDate` and `ContentTime` after correcting time formatting issues.
- Filtered rows where `ModalitiesInStudy` contains "CT".
- Excluded instances starting with "CTA" that have exactly one comma preceded by a number and followed by a space.
- Grouped by `PatientID` and selected the first (oldest) instance based on `ContentDateTime`.
- Counted the unique number of `PatientID`s for analysis.
