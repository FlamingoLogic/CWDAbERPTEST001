---
aliases: 
tags:
  - workinstructions
  - tool
  - operations
  - tab
  - fleet
  - compliance
---

# 🏷️ Alerts – Operations

*Matt Law | Last Updated: 2025-05-02*

This document defines the **Alerts – Operations** tool functionality, navigation, tips, and related tools within AbilityERP. It is used to display critical alerts for [[Support-Location]], [[Vehicle]] and [Group Session](Group-Sessions.md).

---

### 📚 Description
The **Alerts – Operations** tool simplifies the management of critical operational alerts for support locations and vehicles by storing and displaying risk, maintenance, or safety-related information.  
It provides contextual alerts visible on parent records (e.g., asbestos warnings, maintenance schedules), helping organisations comply with health, safety, and operational readiness requirements.

---

### 🧭 Navigation
- Access via: Open window → Alerts tab.
- Not available as a standalone window; it is a tab from table `AbERP_Alert`.

---

### 🛠️ Functionality
- Create alerts for operational purposes linked to a support location or vehicle.
- **[Alert Type](Alert-Type.md)**: Defines the nature of the alert (e.g., Asbestos, Staffing, Service Due).
- **Show As Alert**: When ticked, the alert appears prominently on the parent window.
- **Name** and **Description**: Short summary and details of the alert.
- **Valid From / Valid To**: Controls when the alert is active.
- **Line No**: Used to determine the display order of multiple alerts.
- Behaves slightly differently depending on the parent window (fields or layout may vary).

---

### 🎯 Tips
- Use `Line No` to prioritise which alerts appear first (lowest number = highest priority).
- Leave `Valid To` blank for permanent alerts like asbestos.
- Use `Show As Alert` for safety-critical messages that should always display on the main window.

---

### 📝 Notes
- This table (`AbERP_Alert`) is separate from client/staff alerts.
- The same alert types can be reused across support locations and vehicles for standardisation.
- This tool improves field safety, reduces incident risk, and enhances NDIS compliance.

---
(end of note)
