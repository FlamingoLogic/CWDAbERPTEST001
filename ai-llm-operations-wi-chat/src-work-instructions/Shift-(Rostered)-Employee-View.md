---
aliases:
  - Shift-Rostered-Employee-View
  - View-Rostered-Employees
  - EmployeeShiftView
tags:
  - workinstructions
  - tool
  - rostering
  - reporting
  - dataaccess
  - abilityerp
  - efficiency
---

# 🏷️ Shift (Rostered) Employee View

*Matt Law | Last Updated: 2025-05-15*

The **Shift (Rostered) Employee View** is a high-utility, grid-based in-window report used for monitoring staff allocation against rostered shifts. It combines shift and employee data into a flattened view that supports quick scanning, filtering, and action — particularly around unfilled shifts and support coverage.

---

## 📚 Description

This view is primarily used in **grid view** and built on a custom SQL view that joins Shift (Rostered) headers with the Employee tab. It allows rostering teams to work quickly and visually, without drilling into each record individually.

Users typically configure and save **custom grid layouts** showing only the fields they care about — e.g. employee name, support receiver list, shift time, ratio, and activity.

---

## 🧭 Navigation

- Access via: **Main Menu → Shift (Rostered) Employee View**
- Frequently opened with saved searches or from homescreen DSI's.

---

## 🛠️ Functionality Highlights

- View is read-only, optimised for:
  - Spotting **unfilled or partially filled shift slots**
  - Filtering shifts by **location, officer, activity, or support receiver**
- Users can:
  - Save personal grid layouts
  - Export filtered data
  - Zoom across to shift, employee, or activity detail
  - Launch actions via linked processes (e.g., assign staff, send offers)
  - Create [Request](Request.md)

> ⚠️ Many fields exist to provide full coverage, but most users interact only via configured grid layouts focused on their workflow.

---

## 🎯 Tips

- Sort or filter by **Unfilled Staff Allocations** to find gaps quickly.
- Pair with [(Draft)Available-Shifts]((Draft)Available-Shifts.md) to initiate offers for uncovered shifts.
- Staff records automatically added as **on leave** will still appear — use this view to ensure a replacement is created.
- Combine with custom grid user query presets (e.g. “By Officer”, “Day Options Only”, “Vacant Slots”) to streamline workflows.

---

## 🛠️ Related Tools

- [Shift (Rostered)](Shift-(Rostered).md)

---
(end of note)
