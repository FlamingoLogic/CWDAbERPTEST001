---
aliases:
  - Shift-Rostered-Template
  - Roster-Template
  - Tool-ShiftTemplate
tags:
  - abilityerp
  - rostering
  - tool
  - workinstructions
---

# 🏷️ Shift (Rostered) Template

*Matt Law | Last Updated: 2025-05-14*

This document defines the functionality of the Shift (Rostered) Template window and its related tabs in AbilityERP. Templates are used to build out standardised rosters for a fortnightly cycle [Roster-Period](Roster-Period.md) and are processed using a separate **[AbERP-Generate-Rostered-Shifts](AbERP-Generate-Rostered-Shifts.md)** tool to create actual [shifts(Draft)-Shift-(Rostered)](Shift-(Rostered).md) for rostering.

---

## 📚 Description

The **Shift (Rostered) Template** allows organisations to define repeatable fortnightly support rosters. The template can include shifts, staff, participants, and rostering needs that repeat every two weeks. A separate scheduled process — **Generate Rostered Shifts** — uses these templates to generate actual **Shift (Rostered)** records.

---

## 🧭 Navigation

- Access via: **Main Menu → Shift (Rostered) Template**

---

## 🪟 Header – Shift (Rostered) Template

| Field | Description |
|-------|-------------|
| **Search Key** | Unique identifier used in automation and shift generation. |
| **Name** | Human-readable description (e.g., "Amelia Week 1"). |
| **Start Date / End Date** | Effective dates that determine when the template is valid. |
| **Organization** | Required field for grouping shifts by organisational unit. |
| **Roster Officer** | Optional field used to assign accountability. |
| **Status** | Optional status field (e.g., Drafted, Active). Uses [Request-Status](Request-Status.md) |

---

## 📋 Tabs Overview

### 1. **Shift (Rostered)**

Defines the shift structure within the template.

| Field | Description |
|-------|-------------|
| **Start Day / End Day** | Dropdowns 01–14 aligning with the roster period. |
| **Start Time / End Time** | Time range for the shift instance. |
| **Duration** | Optional manually entered or system-derived. |
| **Shift Type / Category** | Defines support type and classification (e.g. Direct Support, Admin). |
| **Position Needed** | E.g., Support Worker |
| **No. of Staff Required** | Staff count needed for the shift. |
| **Location / Activity** | Where and what the support is. |
| **Claimable** | Tick if this shift should be claimable once generated. |
| **Group Sessions** | Used to indicate group delivery logic (e.g., SIL shared supports). |

---

### 2. **Employee**

Defines the employees (internal or agency staff) planned for this template shift.

| Field | Description |
|-------|-------------|
| **Employee (BP)** | Staff person linked to shift. |
| **Break Start / End Day** | Day values 01–14 within the fortnight cycle. |
| **Break Start / End Time** | Break times (optional). |
| **Working Hours** | Duration - break. |

---

### 3. **Support Receiver**

Adds participants expected to attend each shift.

| Field | Description |
|-------|-------------|
| **Support Receiver (BP)** | Participant or client on shift. |
| **Start / End Day** | Day values 01–14 during the roster cycle. |
| **Start / End Time** | Time window of support delivery. |
| **Service Agreement / Line** | Link to funding. |
| **Service Booking** | Optional reference for tracking actual support plan. |
| **Activity** | e.g. Community Access, SIL, Respite. |

---

### 4. **Rostering Needs**

Attach support needs (e.g. credentials, behavioural strategies) to a template shift.

| Field | Description |
|-------|-------------|
| **Need Type** | Credential, |
| **Contract Term / Start Date** | Optional duration of need. |
| **Comments** | Additional context or staff notes. |

---

### 5. **Related Rostering Needs**

View any needs linked to Support Receivers or Locations used on this shift.  

---

## 🧠 Tips

- Template shifts align to a **14-day cycle**.
- Use templates to maintain consistency, ensure it matches contracted supports and reduce admin.
- Related rostering needs give oversight across both participant and environment-based requirements.

---
(end of note)
