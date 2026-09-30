# Phase 5: Project Development

**Project:** Import Data using Transform Maps (Spreadsheet) – ServiceNow

## Team Details

| Name | Reg No | Department | College |
|------|--------|-----------|---------|
| Afrabanu S | C4S31901 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |
| Kethrin Jenifer | C4S31902 | 3rd B.Sc Mathematics | Mary Matha College of Arts and Science |

---

This document walks through the complete implementation, phase by phase, with screenshots.

## Step 1: Prepare the Sheets

1. Open a new Google Spreadsheet.
2. Create the sample data (Employee ID, Name, Email, Department, Location).
3. Download it as `Sample Spreadsheet.xlsx` (File → Download → Microsoft Excel).

![Sample spreadsheet](../screenshots/01_sample_spreadsheet.png)

*Sample spreadsheet*

![Download as .xlsx](../screenshots/02_download_xlsx.png)

*Download as .xlsx*

## Step 2: Create the Custom Table

**Navigation:** Tables → Create New

- Label: `Employee Test`
- Name: `u_employee_test`

![Tables navigation](../screenshots/03_tables_navigation.png)

*Tables navigation*

![Create table with columns](../screenshots/04_create_table_columns.png)

*Create table with columns*

To add fields: open the table form → Form Context Menu → Configure → **Form Layout** → New. Create these String fields: **Employee ID, Employee Name, Email, Department, Location**, then Save.

![Configure → Form Layout](../screenshots/05_form_layout_configure.png)

*Configure → Form Layout*

![Employee Test form with all fields](../screenshots/06_employee_test_form.png)

*Employee Test form with all fields*

## Step 3: Import Set Table (Load Data)

**Navigation:** Application Navigator → Load Data

- Label: `Employee Import`
- Name: `u_employee_import` (auto-populated)
- Source: File → `Sample Spreadsheet.xlsx`, Sheet number 1, Header row 1
- Click **Submit**, then click **Create Transform Map**

![Load Data navigation](../screenshots/07_load_data_navigation.png)

*Load Data navigation*

![Load Data form](../screenshots/08_load_data_form.png)

*Load Data form*

![Import complete – 15 processed, 15 inserts](../screenshots/09_import_success.png)

*Import complete – 15 processed, 15 inserts*

## Step 4: Create the Transform Map

- Name: `Sample Spreadsheet Import`
- Source table: Employee Import (auto-populated)
- Target table: Employee Test
- Click **Auto Map Matching Fields**, then open **Mapping Assist** to verify, and Save.

![Transform Map form](../screenshots/10_transform_map_form.png)

*Transform Map form*

![Mapping Assist](../screenshots/11_mapping_assist.png)

*Mapping Assist*

![Field maps (5)](../screenshots/12_field_maps.png)

*Field maps (5)*

Now click **Transform** in Related Links, select the import set and map, and press **Transform**.

![Transform related link](../screenshots/13_transform_link.png)

*Transform related link*

![Specify import set and transform map](../screenshots/14_transform_button.png)

*Specify import set and transform map*

![Transformation complete – Success](../screenshots/15_transform_success.png)

*Transformation complete – Success*

## Step 5: Transform Data & Validate

Open **Employee Tests** from the Application Navigator. Use **Personalize List Columns** to arrange the fields (Employee ID, Employee Name, Email, Department, Location).

![Employee Test navigation](../screenshots/16_employee_test_navigation.png)

*Employee Test navigation*

![Records created in Employee Test](../screenshots/17_employee_test_records.png)

*Records created in Employee Test*

![Personalize List Columns](../screenshots/18_personalize_list_columns.png)

*Personalize List Columns*

![Final result – 15 records](../screenshots/19_final_15_records.png)

*Final result – 15 records*

## Step 6: Enable Coalesce

Coalesce prevents duplicate records: existing rows are updated with new values, and only new rows are inserted.

1. Open **Transform Maps** (System Import Sets / System LDAP menu).
2. Open **Sample Spreadsheet Import**.
3. In the **Field Maps** related list, set **Coalesce = true** for **Employee ID**.
4. Save.

![Transform Maps navigation](../screenshots/20_transform_map_navigation.png)

*Transform Maps navigation*

![Transform Maps list](../screenshots/21_transform_maps_list.png)

*Transform Maps list*

![Sample Spreadsheet Import form](../screenshots/22_transform_map_form.png)

*Sample Spreadsheet Import form*

![Coalesce = true on u_employee_id](../screenshots/23_coalesce_true.png)

*Coalesce = true on u_employee_id*

## Step 7: Insert New Data (Excel)

Navigate to **Load Data** and choose **Existing table → Employee Import**, select the modified file, Sheet number 1, Header row 1, and Submit. Then use **Run Transform** in *Next steps*.

The new file contains 4 rows:
- SB-0010: email changed `test10@gmail.com → test18@gmail.com`
- SB-0004: name changed `Ajay Kumar → Ajay`
- Two brand new employee IDs (SB-0016, SB-0017)

![Load Data navigation](../screenshots/24_load_data_navigation_2.png)

*Load Data navigation*

![Load Data – existing table](../screenshots/25_load_data_existing_table.png)

*Load Data – existing table*

![New Excel data (4 rows)](../screenshots/26_new_excel_data.png)

*New Excel data (4 rows)*

![Previously added data](../screenshots/27_previous_excel_data.png)

*Previously added data*

![Import complete – 4 processed](../screenshots/28_import_progress_4_rows.png)

*Import complete – 4 processed*

![Run Transform](../screenshots/29_specify_import_set.png)

*Run Transform*

![Transformation complete – Success](../screenshots/30_transform_success_2.png)

*Transformation complete – Success*

![Transform history: 4 total, 2 inserts, 2 updates](../screenshots/31_transform_history_2_inserts_2_updates.png)

*Transform history: 4 total, 2 inserts, 2 updates*

![Employee Test after update – 17 records](../screenshots/32_employee_test_after_update.png)

*Employee Test after update – 17 records*

## Step 8: Create Reports

**Navigation:** All → Reports → Usage and governance → Reports → New

| Report | Type | Configuration |
|--------|------|---------------|
| Employees by Department | Pie | Table: Employee Test; Group by Department; Aggregation Count |
| Employees by Location | Bar | Table: Employee Test; Group by Location; Aggregation Count |
| Employee List Report | List | Columns: Employee ID, Name, Email, Department, Location |

For each report: **Run** to execute and **Save** to store it.

### Report 1 – Employees by Department
![Reports navigation](../screenshots/34_reports_navigation.png)

*Reports navigation*

![Reports list](../screenshots/35_reports_list.png)

*Reports list*

![Data tab](../screenshots/36_report1_data.png)

*Data tab*

![Type – Pie chart](../screenshots/37_report1_type_pie.png)

*Type – Pie chart*

![Configure – Group by Department, Count](../screenshots/38_report1_configure.png)

*Configure – Group by Department, Count*

![Style, Run and Save](../screenshots/39_report1_style_run_save.png)

*Style, Run and Save*

### Report 2 – Employees by Location
![Reports navigation](../screenshots/40_report2_reports_navigation.png)

*Reports navigation*

![Reports list](../screenshots/41_report2_reports_list.png)

*Reports list*

![Data tab](../screenshots/42_report2_data.png)

*Data tab*

![Type – Bar chart](../screenshots/43_report2_type_bar.png)

*Type – Bar chart*

![Configure – Group by Location, Count](../screenshots/44_report2_configure.png)

*Configure – Group by Location, Count*

![Style](../screenshots/45_report2_style.png)

*Style*

### Report 3 – Employee List Report
![Reports navigation](../screenshots/46_report3_reports_navigation.png)

*Reports navigation*

![Reports list](../screenshots/47_report3_reports_list.png)

*Reports list*

![Data tab](../screenshots/48_report3_data.png)

*Data tab*

![Type – List](../screenshots/49_report3_type_list.png)

*Type – List*

![Configure – select columns](../screenshots/50_report3_columns.png)

*Configure – select columns*

![Style, Run and Save](../screenshots/51_report3_style.png)

*Style, Run and Save*

## Step 9: Dashboard

**Enable dashboard creation via backend name:** open **Access Control (ACL)**, search `pa_dashboards`, open the **create** operation row, tick **Admin overrides**, and Update. Then open `PA_DASHBOARDS.FORM` and create the dashboard named **Employee Analytics Dashboard**.

![ACL navigation](../screenshots/52_acl_navigation.png)

*ACL navigation*

![pa_dashboards ACLs](../screenshots/53_acl_pa_dashboards.png)

*pa_dashboards ACLs*

![Create operation – Admin overrides enabled](../screenshots/54_acl_create_admin_overrides.png)

*Create operation – Admin overrides enabled*

![PA_DASHBOARDS.FORM](../screenshots/55_pa_dashboards_form_search.png)

*PA_DASHBOARDS.FORM*

![Dashboard form](../screenshots/56_dashboard_form.png)

*Dashboard form*

**Add each report to the dashboard:** open the report → View Report → Share → **Add to Dashboard** → choose *Employee Analytics Dashboard* → Add.

![Reports navigation](../screenshots/57_reports_navigation_dashboard.png)

*Reports navigation*

![Three reports created](../screenshots/58_reports_list_three.png)

*Three reports created*

![View Report](../screenshots/59_view_report.png)

*View Report*

![Share → Add to Dashboard](../screenshots/60_share_add_to_dashboard.png)

*Share → Add to Dashboard*

![Select dashboard and Add](../screenshots/61_add_to_dashboard_dialog.png)

*Select dashboard and Add*

![Dashboard with first report](../screenshots/62_dashboard_pie.png)

*Dashboard with first report*

![Dashboard with all three reports](../screenshots/63_dashboard_three_reports.png)

*Dashboard with all three reports*

![Share dashboard by users, groups and roles](../screenshots/64_dashboard_share.png)

*Share dashboard by users, groups and roles*

