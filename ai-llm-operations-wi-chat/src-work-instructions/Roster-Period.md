---
aliases:
  - Roster-Period
  - Tool-RosterPeriod
tags:
  - abilityerp
  - rostering
  - tool
  - workinstructions
  - claiming
  - lookup
---

# 🏷️ Roster Period

*Matt Law | Last Updated: 2025-05-15*

This window defines each **fortnightly roster cycle** in AbilityERP. It acts as a simple lookup used across rostering, booking, and payroll functionality to align data to standard pay periods.

---

## 📚 Description

The **Roster Period** is a simple reference table defining the start and end dates of a fortnightly cycle. It ensures consistent alignment for:

- [Shift-(Rostered)](Shift-(Rostered).md)
- [Service-Booking](Service-Booking.md)
- Payroll and reporting

---

## 🧭 Navigation

- Access via: **Main Menu → Roster Period**

---

## 🪟 Fields

| Field | Description |
|-------|-------------|
| **Client** | Usually set to default (e.g., AbilityERP). |
| **Organization** | Required for filtering/segmentation. |
| **Name** | Free-text label (e.g. “2027 Bi Weekly Pay Period”). |
| **Search Key** | System key (e.g. “202710” for 10th period of 2027). |
| **Year** | Four-digit year. |
| **Payroll Period Number** | Numeric identifier (e.g. “89”). |
| **Start Date / End Date** | Defines the fortnight’s exact range. |
| **Description** | Optional notes (usually mirrors Name). |
| **Active** | Tick to enable selection in other tools. Used to soft delete. |

---

## 🧠 Tips

- Search Key format is typically `YYYYPP` (e.g. `202710`).
- Keep these records complete for the whole year so templates and bookings stay aligned.

---
(end of note)
