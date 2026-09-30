# Phase 1: Brainstorming & Ideation

**Project:** Import Data using Transform Maps (Spreadsheet) – ServiceNow

## Team Details

| Name | Reg No | Department | College |
|------|--------|-----------|---------|
| Afrabanu S | C4S31901 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |
| Kethrin Jenifer | C4S31902 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |

---

## Problem Statement
Organisations often receive employee data from external sources as Excel sheets. Entering hundreds of records manually into ServiceNow is slow and error-prone, and re-importing the same sheet can create duplicate records.

## Idea
Use ServiceNow **Import Sets** as a staging area and **Transform Maps** to map spreadsheet columns to a custom target table, so bulk data is migrated accurately and efficiently.

## Ideas Considered

| Idea | Outcome |
|------|---------|
| Enter employee records manually | Rejected – slow and error-prone |
| Import directly into the target table | Rejected – no staging or validation step |
| Import Set + Transform Map | **Selected** – staging, field mapping and validation |
| Coalesce on Employee ID | **Added** – prevents duplicates on repeated imports |
| Reports and Dashboard | **Added** – visibility into department/location distribution |

## Expected Outcome
- Employee data loaded from `.xlsx` into an Import Set table
- Records transformed into the custom **Employee Test** table
- No duplicate records on re-import (existing records updated instead)
- Three reports combined in one dashboard

## Sample Data Idea
Employee ID, Name, Email, Department, Location (15 sample employees).

![Sample employee spreadsheet used for the project](../screenshots/01_sample_spreadsheet.png)

*Sample employee spreadsheet used for the project*

