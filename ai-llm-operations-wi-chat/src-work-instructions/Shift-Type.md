---
aliases:
  - Shift-Type
  - Tool-ShiftType
  - Lookup-ShiftType
tags:
  - abilityerp
  - tool
  - rostering
  - payroll
  - configuration
  - lookup
---

# 🏷️ Shift Type

*Matt Law | Last Updated: 2025-05-15*

The **Shift Type** window defines the classification and treatment of shifts within AbilityERP. These types are selected on individual shifts, shift templates, and timesheets to help interpret the nature of work (e.g. paid/unpaid, leave, admin, travel).

---

## 📚 Description

Each Shift Type maps to a specific context such as direct support, leave categories, travel, or meetings. These values may inform payroll systems, award interpretation tools, or internal tracking logic.

While the “Auto Break” field provides information to users, the actual handling of breaks is usually determined downstream by the payroll or award system using the mapped type.

---

## 🧭 Navigation

- Access via: **Main Menu → Shift Type**
- Used by:  
  - [Shift (Rostered)](Shift-(Rostered).md)  
  - [Shift (Rostered) Template](Shift-(Rostered)-Template.md)  
  - [(Draft)Timesheets](Timesheet.md)  

---

## 🪟 Key Fields

| Field | Description |
|-------|-------------|
| **Search Key** | Short code (e.g. `SDD`, `AL`, `SLEEP`). Often used in search. |
| **External ID** | Often used in exports and payroll mapping. |
| **Name** | Human-readable name of the shift type. |
| **Description** | Clarifies how this type maps to payroll logic or award rules. |
| **Shift Category** | Category grouping (e.g. Active, Leave). |
| **Auto Break** | *Yes/No* — indicates if breaks are expected to be unpaid (informational only). |
| **Exclude from Working Hours** | Optional checkbox for leave types like LSL or unpaid time. |
| **Account Element** | Optional GL mapping. Information only. |
| **UOM (Unit of Measure)** | Defaults to Hour. |
| **Default** | Flag to identify the system’s fallback shift type. |

---

## 🔍 Common Types

| Code | Name | Notes |
|------|------|-------|
| `SDD` | Service Delivery – Direct (unpaid break) | Most common support worker shift. |
| `SLEEP` | Sleepover | For passive overnight presence. |
| `AL` | Annual Leave | Leave category. |
| `PH` | Public Holiday not Worked | May affect timesheet costing. |
| `TRAVEL` | Travel (unpaid break) | Use for travel-to/from client. |
| `ONCALL` | On Call | Triggers different costing. |
| `PAID` | Service Delivery – Paid Meal Break | Used when break is paid. |

---

## 🎯 Tips

- This list should be reviewed during payroll or award mapping setup.
- Auto Break is **not enforced** by the ERP — it simply guides interpretation.
- Can be used as a filter for audit, reporting, or employee costing.

---
(end of note)
