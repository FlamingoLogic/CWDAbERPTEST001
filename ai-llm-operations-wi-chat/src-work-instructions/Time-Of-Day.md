---
aliases:
  - Time-Of-Day
  - Lookup-TimeOfDay
  - Tool-TimeOfDay
tags:
  - abilityerp
  - tool
  - lookup
  - rostering
---

# 🏷️ Time Of Day

*Matt Law | Last Updated: 2025-05-15*

The **Time Of Day** lookup window is used within AbilityERP to classify shifts and timesheets based on when the support was delivered. These values can support downstream costing, payroll mapping, and compliance checks where required.

---

## 📚 Description

Each record in this window represents a category such as weekday AM, weekend, or public holiday. These tags are selectable on [Timesheet](Timesheet.md) and [Shift-(Rostered)](Shift-(Rostered).md) records to enable reporting, award interpretation, and filtering.

These categories are especially useful when assigning cost overrides or estimating support delivery types for internal and external analysis.

---

## 🧭 Navigation

- Access via: **Main Menu → Time Of Day**
- Used on:
  - [Timesheet](Timesheet.md)
  - [Shift-(Rostered)](Shift-(Rostered).md)

---

## 🪟 Fields

| Field | Description |
|-------|-------------|
| **Search Key** | Short code (e.g., `PASS`, `PH`, `SUN`) |
| **Name** | Human-readable label for selection |
| **Description** | Clarifies the scope or logic (e.g., “Passive support overnight”) |
| **Active** | Whether the option is available for use |

---

## 🎯 Tips

- - Search key should be unique and consistent.

---
(end of note)
