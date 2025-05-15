---
aliases:
  - Tool-GenerateRosteredShifts
  - AbERP-Generate-Rostered-Shifts
  - RosterShift-Generator
tags:
  - workinstructions
  - tool
  - rostering
  - abilityerp
  - process
---

# 🏷️ AbERP Generate Rostered Shifts

*Matt Law | Last Updated: 2025-05-15*

This tool automates the generation of **rostered shifts** in AbilityERP based on [Shift-(Rostered)-Template](Shift-(Rostered)-Template.md) and selected parameters. It reduces manual rostering and enforces consistency across a roster period.

---

### 📚 Description
The **Generate Rostered Shifts** process is a rostering function used to generate shifts from templates that match specific criteria. It’s typically run once per roster period and forms the basis for downstream allocation, attendance, and payroll.

---

### 🧭 Navigation
- Access via: **Main Menu => AbERP Generate Rostered Shifts**

---

### 🛠️ Functionality
- **Input Parameters**:
  - **Status**: Filter to only generate shifts for templates in a certain status (optional).
  - **Rostering Officer**: Limits shift generation to templates assigned to a particular officer (optional).
  - **Shift (Rostered) Template**: Restricts generation to a specific template (optional).
  - **Roster Period**: Select the defined period (e.g., week, fortnight, month) for which shifts should be generated.
  - **Target Shift Status**: Defines the resulting status for new shifts (e.g., Draft, Proposed).
  - **Run as Job**: Enables background processing, useful for bulk shift generation.

- **Behavior**:
  - Matches templates based on filters.
  - Generates [Shift-(Rostered)](Shift-(Rostered).md) per day within the [roster-period](roster-period.md).
  - Populates the Shift (Rostered) table with new records.

---

### 🎯 Tips
- Always check the **Roster Period** exists and has the correct date range before running.
- Use **Target Shift Status** to control visibility/editability (e.g., keep as Draft while reviewing).
- Run in **test environments first** if using new templates.

---

### 📝 Notes
- This tool is part of the core rostering cycle in AbilityERP.
- Can be scheduled for automation using the [Scheduler](Scheduler.md).

---
(end of note)
