# Phase 6: Project Testing

**Project:** Import Data using Transform Maps (Spreadsheet) – ServiceNow

## Team Details

| Name | Reg No | Department | College |
|------|--------|-----------|---------|
| Afrabanu S | C4S31901 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |
| Kethrin Jenifer | C4S31902 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |

---

## Test Cases

| ID | Test | Steps | Expected Result | Actual Result | Status |
|----|------|-------|-----------------|---------------|--------|
| TC-1 | Load spreadsheet into Import Set | Load Data → Employee Import → Submit | State Complete, Success; 15 processed, 15 inserts | 15 processed, 15 inserts, 0 errors | Pass |
| TC-2 | Transform to target table | Run Transform Map | All 15 records in Employee Test | 15 records (1 to 15 of 15) | Pass |
| TC-3 | Field mapping | Check Field Maps related list | 5 source → target mappings | 5 mappings present | Pass |
| TC-4 | Coalesce – update existing | Import 4-row file with 2 changed rows (SB-0004, SB-0010) | 2 rows updated | 2 updates | Pass |
| TC-5 | Coalesce – insert new | Same file has 2 new IDs | 2 new rows inserted | 2 inserts (SB-0016, SB-0017) | Pass |
| TC-6 | Re-import identical data | Import the same 4-row file again | No inserts, no updates, no duplicates | Total 4, Inserts 0, Updates 0, Ignored 4 | Pass |
| TC-7 | Data verification after update | Open Employee Tests | 17 records; SB-0004 name = Ajay; SB-0010 email = test18@gmail.com | Verified | Pass |
| TC-8 | Reports | Run each report | Pie by Department, Bar by Location, List of 17 | All rendered correctly | Pass |
| TC-9 | Dashboard | Add 3 reports to dashboard | All widgets visible | All 3 visible | Pass |

## Evidence

### TC-1 / TC-2: Initial import and transform
![Import set load – 15 inserts](../screenshots/09_import_success.png)

*Import set load – 15 inserts*

![Transformation complete – Success](../screenshots/15_transform_success.png)

*Transformation complete – Success*

![15 records in Employee Test](../screenshots/19_final_15_records.png)

*15 records in Employee Test*


### TC-3: Field mapping
![Field maps](../screenshots/12_field_maps.png)

*Field maps*


### TC-4 / TC-5: Coalesce – updates and inserts
![Transform history – Total 4, Inserts 2, Updates 2](../screenshots/31_transform_history_2_inserts_2_updates.png)

*Transform history – Total 4, Inserts 2, Updates 2*

![Employee Test after update](../screenshots/32_employee_test_after_update.png)

*Employee Test after update*


### TC-6: Duplicate prevention
![Re-import of same file – all 4 rows ignored](../screenshots/33_transform_history_4_ignored.png)

*Re-import of same file – all 4 rows ignored*


### TC-8 / TC-9: Reports and dashboard
![Employees by Department](../screenshots/39_report1_style_run_save.png)

*Employees by Department*

![Dashboard with three reports](../screenshots/63_dashboard_three_reports.png)

*Dashboard with three reports*


## Conclusion
All test cases passed. Coalesce on **Employee ID** ensures repeated imports update existing records instead of inserting duplicates.
