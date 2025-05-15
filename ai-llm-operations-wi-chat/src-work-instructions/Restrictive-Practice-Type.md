---
aliases:
  - Restrictive Practice Type
  - Restrictive Type Setup
tags:
  - workinstructions
  - tool
  - client
  - compliance
  - lookup
---

# 🏷️ Restrictive Practice Type

*Matt Law | Last Updated: 2025-05-07*

This document outlines how to use the **Restrictive Practice Type** window in AbilityERP.  
This window is used to define and classify categories of [Restrictive-Practices](Restrictive-Practices.md), along with specific line items commonly used for NDIS reporting and compliance purposes.

---

### 📚 Description
The **Restrictive Practice Type** window allows you to define high-level types of restriction (e.g., Environmental, Chemical, Physical) and manage standardised **lines** under each type.  
These entries appear as selectable values when logging Restrictive Practices in the Support Receiver tab.

---

### 🧭 Navigation
- Access via: **Main Menu** → search “Restrictive Practice Type”
- Used in: **Restrictive Practices Tab** (Support Receiver)

---

### 🛠️ Functionality

#### Header Fields
- **Search Key**: Short code for internal use (e.g., "CHEM").
- **Name**: Full label (e.g., "Chemical Restraint").
- **Description**: Optional clarification of category purpose.
- **Active**: Controls visibility in dropdowns across the system.

#### Lines (Tab: *Restrictive Practice Type Line*)
- Define specific restriction items (e.g., "Lock – fridge", "Electronic Monitoring Devices").
- Each line includes:
  - **Search Key**
  - **Name**
  - **Optional Description**

---

### 🎯 Tips
- Use the lines tab to prefill common items used during compliance reporting.
- Keep outdated or unused options **inactive** to reduce clutter in user-facing windows.

---

### 📝 Notes
- Header stored in `AbERP_Restr_Practice_Type`

---
(end of note)
