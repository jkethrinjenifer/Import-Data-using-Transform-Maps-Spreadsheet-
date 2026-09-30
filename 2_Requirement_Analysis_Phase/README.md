# Phase 2: Requirement Analysis

**Project:** Import Data using Transform Maps (Spreadsheet) – ServiceNow

## Team Details

| Name | Reg No | Department | College |
|------|--------|-----------|---------|
| Afrabanu S | C4S31901 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |
| Kethrin Jenifer | C4S31902 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |

---

## Functional Requirements

| ID | Requirement |
|----|-------------|
| FR-1 | Prepare an employee spreadsheet and export it as `.xlsx` |
| FR-2 | Create a custom table `u_employee_test` with 5 string fields |
| FR-3 | Load the spreadsheet into an Import Set table `u_employee_import` |
| FR-4 | Create a Transform Map from the import table to the target table |
| FR-5 | Map fields (Name, Employee ID, Department, Location, Email) |
| FR-6 | Run the transform and verify records in the target table |
| FR-7 | Enable Coalesce on Employee ID to avoid duplicates |
| FR-8 | Re-import modified data: update existing records, insert new ones |
| FR-9 | Create 3 reports and add them to a dashboard |

## Data Requirements

| Column | Type | Description |
|--------|------|-------------|
| Employee ID | String | Unique ID, e.g. SB-0001 (used as Coalesce field) |
| Employee Name | String | Full name |
| Email | String | Email address |
| Department | String | ServiceNow / Salesforce / AIML |
| Location | String | Hyderabad / Chennai |

## Technical / Tool Requirements
- ServiceNow instance with admin access
- Google Sheets (or Excel) to prepare the `.xlsx` file
- Modules used: Tables, Load Data, Transform Maps, Reports, Dashboards, Access Control (ACL)

## Non-Functional Requirements
- **Accuracy** – all 15 source rows must appear in the target table
- **Data integrity** – repeated imports must not create duplicates
- **Usability** – list columns arranged in the same order as the source sheet

![Source data requirement – employee sheet](../screenshots/01_sample_spreadsheet.png)

*Source data requirement – employee sheet*

