---
aliases:
  - Timesheet Approval
  - InfoWindow-TimesheetApproval
  - Approve-Timesheet
tags:
  - abilityerp
  - tool
  - info
  - payroll
  - rostering
  - employee
---

# 🏷️ Timesheet Approval

*Matt Law | Last Updated: 2025-05-15*

The **Timesheet Approval** info window allows bulk approval of completed timesheets in AbilityERP. It uses filters at the top of the window and a bulk action button at the bottom to change status for selected records.

---

## 📚 Description

This tool is used to mark ctimesheets as **approved** and set the status on the timesheet accordingly. It operates over a filtered list of timesheets and allows multi-select status update actions using the button:  
`📎 AbERP Set Timesheet Approved Status`

---

## 🧭 Navigation

- Access via: **Main Menu → Timesheet Approval**
- Action performed: Click **AbERP Set Timesheet Approved Status** after selecting rows.

---

## 🪟 Filters

Filter timesheets by:
- Employee
- Business Partner (Client)
- Activity
- Contract Location
- Supervisor
- Status
- Date ranges (Start/End)
- Timesheet fields including Shift Type and Description

---

## ✅ Status Workflow

Timesheets use embedded **Request Status logic**, allowing them to move through a defined lifecycle. [Request-Status](Request-Status.md)

The **Approved** process sets the status to a final close locking the timesheet from further edits. 
Signaling eligibility for downstream processing like payroll or reporting

---

## 🎯 Tips

- Use filters to isolate timesheets ready for approval.
- Select multiple rows and apply the status update in one action.
- Review timesheet validations prior to approval.
- You can customise available statuses via the [Request-Status](Request-Status.md) window.

---
(end of note)
