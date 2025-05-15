---
aliases: 
tags:
  - workinstructions
  - tool
  - core
  - lookup
  - compliance
---

# 🏷️ Alert Type

*Matt Law | Last Updated: 2025-05-02*

This document defines the **Alert Type** lookup window (table: AbERP_Alert_Type) used to categorise alerts in both operational and client contexts across multiple AbilityERP windows.

---

### 📚 Description
The **Alert Type** tool standardises alert naming across AbilityERP. It is shared by two different alert tables:
- `AbERP_Alert` – used in **Support Location**, **Vehicle**, and **Group Session** windows.
- `AbERP_Alert_SR` – used in **Support Receiver** and **Employee** windows.

It defines what each alert relates to (e.g., Allergy, Asbestos, Incident Risk), enabling categorisation, filtering, and correct tab usage in different windows.

---

### 🧭 Navigation
- Access via: *Main menu* → Alert Type
- Or: Click the Alert Type field on any alert record in Support Receiver, Employee, Vehicle, or Support Location windows.

---

### 🛠️ Functionality
- **Search Key / Name**: Short identifier and display name of the alert type.
- **Alert Type Flags**:
  - *Employee Alert*: Enables for use in Employee alerts (`AbERP_Alert_SR`)
  - *Support Receiver Alert*: Enables for use in Support Receiver alerts (`AbERP_Alert_SR`)
  - *Support Location Alert*: Enables for use in Support Location alerts (`AbERP_Alert`)
  - *Vehicle Alert*: Enables for use in Vehicle alerts (`AbERP_Alert`)
  - *Is Group Session*: Enables use in Group Session alerts

---

### 🎯 Tips
- Tick only the relevant alert type boxes for where the alert should be available—this controls visibility in lookup fields.
- Use consistent naming across both SR and Operational alerts to aid recognition and reporting.
- Alert types should be kept broad and descriptive to support filtering and automation rules.

---

### 📝 Notes
- This window supports both compliance-focused alerts (SR) and operational risk alerts (e.g., service due, bushfire hazard).

---
### Referenced tools

- [[Alerts–Operations]]
- [Alerts-Support Receiver and Employee](Alerts-Support-Receiver-and-Employee.md)

---
(end of note)
