---
aliases:
  - Timesheet Export
tags:
  - tool
  - postgresexport
  - Rostering
  - workinstructions
---

# 🛠️ Export Timesheet payroll

*Adam Sawtell | Last Updated: 2025-05-01*

Exports approved timesheet records to CSV for upload into external payroll systems (e.g. KeyPay, HR3, Xero), filtered by date, roster period, and shift settings.

---

## 📚 Description  
The **Timesheet Export** tool simplifies payroll processing by generating CSV files from approved timesheet records. Users select a specific roster period and date range to export relevant data, ensuring accuracy through mandatory filters. Optional parameters allow further tailoring.

---

## 🧭 Navigation  
- **Main menu** → **Export Timesheet Payroll**

---

## ⚙️ Functionality

- Generates a CSV with filtered timesheet data for payroll upload.  
- **Mandatory Fields**:
  - `Date From` / `Date To`: Defines export range.
  - `Roster Period`: Ensures alignment with payroll cycle.
- **Optional Filters**:
  - `Is Employee`: Default = Y; filters out contractors if unticked.
  - `Timesheet Status`: Only export approved/processed entries.
  - `Document Type`: Currently supports “Time Sheet”.
  - `Shift Type`: Filters to include only specific types (e.g. SIL, Community).
  - `External ID is Null`: Ensures only unexported records are included.
  - `Run as Job`: Executes in background with system scheduler.

- **Output Format**:
  - CSV formatted for import into payroll systems.
  - Naming convention: `timesheet_export_[rosterperiod]_[timestamp].csv`

---

## 💡 Tips

- Always review `Date From`, `Date To`, and `Roster Period` to avoid missed or duplicate records.
- Run a small export to confirm structure matches payroll system expectations.
- If omitting `Roster Period`, ensure `Date From` and `Date To` are tightly scoped.
- Use `Run as Job` for large exports; review logs afterward.
- Confirm all timesheets are approved before export to ensure completeness.

---

## 📝 Notes

- Tool requires:
  - Document type “Time Sheet” to be configured.
  - Roster Periods correctly created and maintained.
  - Appropriate user role permissions.
- Export structure must match external system formatting (can be adapted if needed).
- Roster Period is required unless only using date filters.

---

## 🔧 Related Tools
- [AbERP-Postgres-Export-Copy-Command](AbERP-Postgres-Export-Copy-Command.md)
