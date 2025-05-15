---
aliases:
  - Shift-Rostered
  - Tool-ShiftRostered
  - Rostered-Shift
tags:
  - workinstructions
  - tool
  - rostering
  - abilityerp
  - validation
---

# 🏷️ Shift (Rostered)

*Matt Law | Last Updated: 2025-05-15*

The **Shift (Rostered)** window is central to rostering, compliance, claiming, and payroll functions in AbilityERP. Each record represents a scheduled shift, either manually entered or generated from [Shift-Rostered-Template](Shift-(Rostered)-Template.md). These records control service delivery, drive allocation and timesheets, and form the basis for validation and claiming.

---

## 📚 Description

Shift (Rostered) is the *actual shift* — created per roster period — with key fields for time, location, staff, clients, and support needs. It includes tools for validation, allocation, communication (via SMS), and downstream claiming and payroll.  

An **after-save event** is triggered each time a shift is saved. If any assigned employee is on approved leave during the shift time, they are automatically marked as **on leave**, and a **new blank employee line** is created to represent the now-unfilled slot.  
See: [(Draft)Unavailability-Leave]((Draft)Unavailability-Leave.md)

---

## 🧭 Navigation

- Access via: **Main Menu → Shift (Rostered)**
- Also generated from: [Generate Rostered Shifts](AbERP-Generate-Rostered-Shifts.md)

---

## 🪟 Header Overview

| Field | Description |
|-------|-------------|
| **Name** | Optional name (e.g. “Monday AM - SIL”). |
| **Start/End DateTime** | Duration of the shift. |
| **Location / Activity / Vehicle** | Where the support takes place and what it's for. |
| **Roster Period** | Links to a defined roster cycle. |
| **Shift Type / Category** | E.g., Admin, Leave. |
| **Position Needed** | Role required (e.g., Support Worker). |
| **No. Staff Required / Support Receivers** | Expected counts. |
| **Status** | Workflow status (e.g. Drafted, Proposed, Confirmed). |
| **Rostering Officer** | Person responsible for shift delivery. |
| **Buttons** | Send shift updates or SMS offers (via Bird SMS plugin). |

---

## 📋 Tabs Overview

### 👥 Employee

- Assigns employees to the shift.
- Tracks:
  - Internal vs. agency
  - Breaks and working time
  - Clock in/out
  - Timesheet link
- Clock buttons: **AbERP Shift Clock In / Out**

#### ⚙️ After-Save Logic
When a shift is saved:
- If an **assigned employee has an active leave record**, they are marked **on leave** (usually by setting Shift Type to *Annual Leave*).
- A **new blank employee record** is created for the same shift, representing the now-unfilled slot.
- This ensures continuity and allows the unfilled slot to be picked up.
- Related tool: [(Draft)Unavailability-Leave]((Draft)Unavailability-Leave.md)

---

### 👤 Support Receiver

- Links participant(s) to the shift.
- Tracks:
  - Service Agreement + Line
  - Booking reference
  - Duration and activity
  - Attendance status

---

### 📝 Activity

- Log shift-related notes, events, or communication (e.g. case notes, task updates, SMS logs).
- Driven by: [Activity Viewer](Activity-Viewer.md)
- Activity Type examples: Task, Phone call, Text/SMS, etc.

---

### 📎 Rostering Needs

- Add **shift-specific** rostering needs.
- Types: Credential, Gender, Restricted Employees.
- Does **not** inherit from templates — these are local to this shift only.
- See: [(Draft)Rostering-needs]((Draft)Rostering-needs.md)

---

### 🔁 Related Rostering Needs

- Displays inherited needs from Support Receiver or Location.
- View-only.
- Also documented in: [(Draft)Rostering-needs]((Draft)Rostering-needs.md)

---

### 🔄 Response Log

- Shows responses to **Available Shift Offers**.
- Staff can request or decline.
- Driven by logic described in: [(Draft)Available-Shifts]((Draft)Available-Shifts.md)

---

### ✅ Validate

- Triggers validation using [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md)
- Common test on this window:
  - ❌ **Overlapping Shifts**: Detects if an employee is assigned to multiple overlapping shifts
- All rules are listed in: [Validation-Tests](Validation-Tests.md)

---

### 🧮 Allocation Records

- Shows time-split allocations across support receivers.
- Basis for downstream bookings, claiming, and cost calculation.
- Regenerated when needed using: **Regenerate Allocation Records** button.
- See: [Allocation-Records](Allocation-Records.md)
- Can be [Scheduler](Scheduler.md)

---

## 🎯 Tips

- Validate and check all assignments before confirming or exporting for claiming.
- If a shift changes, re-check allocations and validation.
- Use SMS buttons for urgent fill attempts or shift updates (integrated with Bird SMS).
- If a staff member is marked on leave automatically, review and fill the replacement employee line promptly.
- Use [Shift-(Rostered)-Employee-View](Shift-(Rostered)-Employee-View.md) to fill unfilled shifts. 
- Generate [Timesheet](Timesheet.md)s from shifts using the [AbERP-Generate-Timesheets](AbERP-Generate-Timesheets.md)

---
(end of note)
