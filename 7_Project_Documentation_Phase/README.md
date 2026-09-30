# Phase 7: Project Documentation

**Project:** Import Data using Transform Maps (Spreadsheet) – ServiceNow

## Team Details

| Name | Reg No | Department | College |
|------|--------|-----------|---------|
| Afrabanu S | C4S31901 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |
| Kethrin Jenifer | C4S31902 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |

---

## Overview
This micro project imports structured employee data from an external spreadsheet into ServiceNow using Import Sets and Transform Maps. The spreadsheet is loaded into an Import Set table (staging area); a Transform Map maps source fields to the target table; running the transformation creates records that are then validated.

## Summary of Implementation

| Phase | What was done |
|-------|---------------|
| 1 | Prepared employee sheet and exported `.xlsx` |
| 2 | Created custom table **Employee Test** (`u_employee_test`) |
| 3 | Loaded data into **Employee Import** (`u_employee_import`) |
| 4 | Created and ran the **Sample Spreadsheet Import** Transform Map |
| 5 | Validated 15 records and arranged list columns |
| 6 | Enabled **Coalesce** on Employee ID |
| 7 | Imported modified data: 2 inserts, 2 updates; identical re-import: 4 ignored |
| 8 | Created 3 reports (Department pie, Location bar, Employee list) |
| 9 | Built **Employee Analytics Dashboard** with all 3 reports |

## Key Learnings
- Import Set tables act as a staging area before data reaches the target table.
- Auto Map Matching Fields and Mapping Assist speed up field mapping.
- **Coalesce** is essential for real-world imports: it updates matching records and avoids duplicates.
- Reports and dashboards give administrators/HR teams a single view of data distribution.
- Dashboard creation via `PA_DASHBOARDS.FORM` requires **Admin overrides** on the `pa_dashboards` create ACL.

## Conclusion
1. The project implemented an automated employee data management solution using Import Sets and Transform Maps, ensuring accuracy, efficiency and data integrity.
2. Enabling Coalesce on Employee ID prevents duplicates and makes repeated imports update existing data instead of inserting redundant entries.
3. Reports and a dashboard were added to provide visibility into employee data (department-wise and location-wise distribution and a full employee list).
4. The dashboard consolidates these reports into one centralized view for administrators and HR teams.

## Documentation Index
- GitHub Repository: [https://github.com/jkethrinjenifer/Import-Data-using-Transform-Maps-Spreadsheet-](https://github.com/jkethrinjenifer/Import-Data-using-Transform-Maps-Spreadsheet-)
- Demo Video: [Google Drive](https://drive.google.com/file/d/1h7N6aCIalcucP7SH_ZIPwA-rWEZ-ESrn/view?usp=drivesdk)
- Phase-wise documents are in the numbered folders of this repository.
- Screenshots are in [`/screenshots`](../screenshots/).
