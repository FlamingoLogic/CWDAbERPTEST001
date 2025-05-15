---
aliases:
  - Allocation-Records
tags:
  - abilityerp
  - tool
  - rostering

---

# 🛠️ Tool: Allocation Records (AbERP_SRAllocation)

*Matt Law | Last Updated: 2025-04-30*

---

## 📘 Description

The **Allocation Records** tab under the **Shift (Rostered)** window tracks the distribution of support time between Support Receivers (clients) during a shift. Each record represents a time-bound support ratio block and forms the basis for downstream allocation to bookings or invoiceable outputs.

Records are automatically generated when the shift or relevant SR timing data changes, using a hash system to detect meaningful updates. Manual record creation is disabled.

---

## 📍 Navigation

- **Main Menu** → **Shift (Rostered)** → Tab: **Allocation Records**
- **Main Menu** → **Allocation Records**
- Records cannot be manually added. Use the **Regenerate Allocation Records** button to refresh.

---

## 🔧 Key Fields

| Field | Purpose |
|:---|:---|
| **Support Receiver** | The participant receiving support during the time block. |
| **Start Date / End Date** | The time block this ratio applies to. |
| **Duration** | Total hours of the ratio block. |
| **Part Type** | Ratio (e.g., 1:1, 1:2) applied to the time block. |
| **No. SR** | Total number of participants in this block. |
| **Shift Type** | Type of delivery (e.g., Direct Support). |
| **Activity / Product / UOM** | Describes the service delivered during the block. |
| **Staff Portion** | Portion of staff time allocated to this participant. |
| **Booking Line Allocation** | Optional field for linking directly to a booking line. |
| **Processed** | Indicates whether this record has been consumed downstream. |
| **Allocation Hash** | Unique hash to identify the current support block. |

---

## ⚙️ Automation Rules

- Records are regenerated when a **hash change** is detected (i.e. when shift or participant times are updated).
- Button: **Regenerate Allocation Records** triggers manual regeneration.
- Hash ensures records are only recreated when allocation-relevant data changes.

---

## 🧠 Usage Tips

- Use this tab for review or audit — most downstream use (e.g., booking validation or cost allocation) will reference these records.
- Will later support allocations against **timesheets** and **shift templates**.

[Allocation-Records-MattNotes](Allocation-Records-MattNotes.md)


---
(end of note)
