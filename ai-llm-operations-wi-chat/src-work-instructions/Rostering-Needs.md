---
aliases:
  - Rostering-Needs
tags:
  - workinstructions
  - tool
  - rostering
  - client
  - employee
  - validation
---

# 🏷️ Rostering Needs

*Matt Law | Last Updated: 2025-05-02*

This document defines the **Rostering Needs** tool in AbilityERP, used to enforce and match shift, client, and location requirements with employee credentials and characteristics for safer, compliant service delivery.

---

### 📚 Description
The **Rostering Needs** tool enables organisations to define needs for Positions, Rostered Shifts, Support Locations, or Support Receivers. These needs help ensure appropriate employees are rostered by validating against gender, credentials, or staff restrictions, and support automation.

---

### 🧭 Navigation
- Access via: Main menu → Rostering Needs
- Or: Via related tab on the following windows:
  - [[Shift-(Rostered)]]
  - [[(Draft)Position]]
  - [[Support-Receiver-(BP)]]
  - [[Support-Location]]

---

### 🛠️ Functionality
- **Needs Association**: Specifies where the need applies (Position, Rostered Shift, Support Location, or Support Receiver).
- **Need Type**: Options include:
  - **Credential**: e.g., First Aid, Medication Training.
  - **Gender**: e.g., Female for personal care shifts.
  - **Restricted Employees**: Flags certain employees as ineligible for the selected association.
- **Dynamic Fields**: Based on selection, additional fields appear:
  - Credential dropdown (for Credential needs)
  - Gender dropdown (for Gender needs)
  - Restricted Employee selector (if applicable)
- **Contract Term**:  
  - **Ongoing**: No expiry date.  
  - **Fixed**: Requires **Expiry Date**, enforcing time-based checks.
- **Comments**: Records supporting documentation and scheduling for the need.

---

### 🎯 Tips
- Use ongoing contract term for permanent needs (e.g., gender preference); use fixed when the requirement is temporary (e.g., due to current behaviours or medical status).
- Pair this tool with the [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md) to block shifts that do not meet required rostering needs.
- Add clear Comments to explain the purpose of the need (e.g., "Female required for personal care shifts").

---

### 📝 Notes
- This tool is a critical part of AbilityERP’s safeguarding and compliance model.

---

### 🛠️ Related Tools
- [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md)
- [[(Draft)Credential-Assignment]]

---
(end of note)
