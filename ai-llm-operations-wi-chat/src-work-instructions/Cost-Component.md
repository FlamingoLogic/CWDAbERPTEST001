---
aliases:
  - Cost-Component
tags:
  - abilityerp
  - timesheet
  - costing
  - tool
---

# 🏷️ Tool: Cost Component (Timesheet)

*Matt Law | Last Updated: 2025-04-30*

---

## 📋 Description
**NOT CURRENTLY IN USE**

The **Cost Component** tool allows users to estimate and allocate service delivery costs against individual timesheet records in AbilityERP.  
It supports splitting costs into components (e.g., standard hours, breaks, penalties) based on remuneration rules and applied rates.

**Note**: This tool is for internal costing and forecasting purposes. It is **not a payroll module** and does **not** currently calculate overtime.

---

## 📍 Navigation
- **Main Menu ➔ Timesheet ➔ Timesheet Window ➔ Cost Component Tab**
- **Main Menu ➔ Cost Component**

---

## 🛠️ Functionality
- Attach multiple **Cost Component** records to a single timesheet.
- Split hours and costs based on remuneration rules and split rules.
- Calculate **Line Amount** as `Applied Rate × Quantity`.
- Track and report on estimated labour costs at a detailed level.
- Update cost component via button on the timesheet. 

---

## 🖥️ Key Fields

| Field | Purpose |
|:---|:---|
| **TimeSheet and Expenses ID** | Link to the parent timesheet record. |
| **Split Rules Applied** | Displays split rules used (e.g., meal break). |
| **Rem Rules Applied** | Displays remuneration categories applied (e.g., Permanent Ordinary). |
| **Start Date / End Date** | Time period for the specific cost component. |
| **Quantity** | Hours worked or allocated for the cost block. |
| **Applied Rate** | Hourly rate used for costing. |
| **Line Amount** | Total cost calculated (Quantity × Applied Rate). |
| **Remuneration Types** | Primary remuneration type (e.g., Permanent, Casual). |
| **Remuneration Line** | Specific remuneration item within the type (e.g., ordinary hours). |

---

## 🔄 Key Behaviour
- **Manual Adjustment**: Users can manually edit quantity and applied rate if needed.
- **Audit Trail**: Created/updated by users with timestamps.
- **Split Support**: Allows multiple cost blocks over one timesheet (e.g., after meal break).

---

## 🚀 Future Development Ideas

| Idea | Description |
|:---|:---|
| Link to Allocation Record | Allow mapping between shift allocations and cost components for deeper cost tracing. |
| Overtime Handling | Extend rules to automatically apply overtime rates. |
| Shift | Also apply cost component to shift. Include an estimate for when no staff is selected or Agency are selected |
| Margin Analysis | Compare internal costs against claimable amounts from bookings. |

---
(end of note)
