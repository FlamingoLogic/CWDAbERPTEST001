---
aliases:
  - Timesheet
  - Tool-Timesheet
tags:
  - abilityerp
  - tool
  - rostering
  - payroll
  - validation
---

# 🏷️ Timesheet

*Matt Law | Last Updated: 2025-05-15*

The **Timesheet** window in AbilityERP records completed staff work hours for payroll, costing, and compliance purposes. It links directly to a **[Shift-(Rostered)](Shift-(Rostered).md)** record.

---

## 📚 Description

Timesheets are usually created via the [AbERP Generate Timesheets](AbERP-Generate-Timesheets.md) process after shifts are confirmed.  
They store working time, break details, reference data, and can include validation and costing layers.

---

## 🧭 Navigation

- Access via: **Main Menu → Timesheet**
- Created by: [AbERP Generate Timesheets](AbERP-Generate-Timesheets.md)

---

## 🪟 Key Fields

| Section | Field | Description |
|--------|-------|-------------|
| **Header** | Document Type | Usually 'Time Sheet' |
| | Roster Period | Links to rostered cycle |
| | Employee (User) / Agency Staff | Person who worked the shift |
| | Support Start/End Day | Day of week (auto-filled) |
| | Location | Where the shift occurred |
| **Details** | Shift Type | Lookup from [Shift Type](Shift-Type.md) |
| | Description | Optional notes |
| **Break** | Break Start/End | Records any unpaid breaks |
| | Break Duration | Auto-calculated |
| **Reference** | Activity | Optional reference to client-related work |
| | Rostered Shift | Source shift this is linked to |
| | Group Session | Optional group link |
| **Costing** | Time of Day | Lookup from [Time-Of-Day](Time-Of-Day.md). 
| **Validation** | Validated | Result from [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md) |

---

## ✅ Validation

This window supports the **Document Validation Plugin**.  
Common test includes:

- **Shift–Timesheet Date/Time Comparison**  
  Compares timesheet's start/end with the related shift. If they differ, a *warning* is issued.  

See: [Validation-Tests](Validation-Tests.md)

---

## 🧮 Tabs

### 🔹 Support Receiver
- Mirrors support receiver info from the shift.
- Fields: Business Partner, Service Booking, Service Agreement, Activity, Attended, Duration.

### 🔹 Cost Component  
- Used for internal cost estimation. See: [Cost-Component](Cost-Component.md)

### 🔹 Validate  
- Shows results of document validation if plugin is active.

---

## 🎯 Tips

- Break info is recorded but **not enforced** — award engine or payroll handles rules.
- Time of Day can help group shifts / timesheets by context.

---
(end of note)
