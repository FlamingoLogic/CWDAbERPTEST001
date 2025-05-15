---
aliases:
  - Alerts-SR
tags:
  - workinstructions
  - tool
  - employee
  - client
  - compliance
---

# 🏷️ Alerts – Support Receiver and Employee

*Matt Law | Last Updated: 2025-05-02*

This document defines the **Alerts** tab used on the **Support Receiver (client)** and **Employee** windows in AbilityERP, focused on safeguarding, compliance, and operational communication.

---

### 📚 Description
The **Alerts – Support Receiver and Employee** tool logs individual alerts relating to a specific participant or staff member. These alerts are used to enforce safeguarding rules (e.g., allergy risks, behavioural triggers) and improve shift planning and quality assurance.

This alert functionality is based on the `AbERP_Alert_SR` table and is distinct from the `AbERP_Alert` table used for operational alerts (e.g., vehicles, support locations).

---

### 🧭 Navigation
- Access via:  
  - Support Receiver window → Alerts tab  
  - Employee window → Alerts tab

---

### 🛠️ Functionality
- **Alert Type**: Lookup field linked to [Alert Type](Alert-Type.md). Only types ticked for *Support Receiver Alert* or *Employee Alert* are selectable.
- **Show as Alert**: If ticked, this alert is displayed on the header window.
- **Name**: Short label to describe the alert.
- **Description**: Full details of the risk, issue, or note.
- **Valid From / To**: Dates controlling when the alert is active.

---

### 🎯 Tips
- Use alerts to highlight behavioural risks, allergies etc.
- Ensure all critical alerts are flagged with “Show as Alert”.
- Regularly review expired alerts for archival or update.

---

### 📝 Notes
- This alert table is used for safeguarding and compliance, not general operations. For site or vehicle-based alerts, use [Alerts – Operations](Alerts–Operations.md).
- Alerts in this tab are referenced in shift planning, staff restrictions, and validation rules.

---
(end of note)
