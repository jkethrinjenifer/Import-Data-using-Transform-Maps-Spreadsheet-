# Import Data using Transform Maps (Spreadsheet) – ServiceNow

A ServiceNow micro project that imports bulk employee data from an Excel spreadsheet into ServiceNow using **Import Sets** and **Transform Maps**, prevents duplicates with **Coalesce**, and visualises the data with **Reports** and a **Dashboard**.

## Team Details

| Name | Reg No | Department | College |
|------|--------|-----------|---------|
| Afrabanu S | C4S31901 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |
| Kethrin Jenifer | C4S31902 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |

## Project Links

| Resource | Link |
|----------|------|
| GitHub Repository | [https://github.com/jkethrinjenifer/Import-Data-using-Transform-Maps-Spreadsheet-](https://github.com/jkethrinjenifer/Import-Data-using-Transform-Maps-Spreadsheet-) |
| Demo Video (Google Drive) | [Watch / Download](https://drive.google.com/file/d/1h7N6aCIalcucP7SH_ZIPwA-rWEZ-ESrn/view?usp=drivesdk) |

## Repository Structure (Phase-wise)

| # | Phase | Folder |
|---|-------|--------|
| 1 | Brainstorming & Ideation | [1_Brainstorming_Ideation_Phase](1_Brainstorming_Ideation_Phase/README.md) |
| 2 | Requirement Analysis | [2_Requirement_Analysis_Phase](2_Requirement_Analysis_Phase/README.md) |
| 3 | Project Design | [3_Project_Design_Phase](3_Project_Design_Phase/README.md) |
| 4 | Project Planning | [4_Project_Planning_Phase](4_Project_Planning_Phase/README.md) |
| 5 | Project Development | [5_Project_Development_Phase](5_Project_Development_Phase/README.md) |
| 6 | Project Testing | [6_Project_Testing_Phase](6_Project_Testing_Phase/README.md) |
| 7 | Project Documentation | [7_Project_Documentation_Phase](7_Project_Documentation_Phase/README.md) |
| 8 | Project Demonstration | [8_Project_Demonstration_Phase](8_Project_Demonstration_Phase/README.md) |

All screenshots are stored in the [`screenshots`](screenshots/) folder and referenced from the phase documents.

## Key Objects Created in ServiceNow

| Object | Name |
|--------|------|
| Target table | Employee Test (`u_employee_test`) |
| Import set (staging) table | Employee Import (`u_employee_import`) |
| Transform map | Sample Spreadsheet Import |
| Coalesce field | Employee ID |
| Reports | Employees by Department (Pie), Employees by Location (Bar), Employee List Report (List) |
| Dashboard | Employee Analytics Dashboard |
