---
aliases:
  - Tool-Employee
  - Employee
tags:
  - abilityerp
  - tool
  - workinstructions
  - employee
---

# 🏷️ Employee Window

*Matt Law | Last Updated: 2025-05-15*

This document defines the **Employee** window in AbilityERP. It allows for the management of employee records, credentials, validation status, and related contact/activity/location information. Built on the Business Partner (BP) table, the Employee window provides a consolidated view of staff data.

---

## 📚 Description

The **Employee** window manages employee records within AbilityERP, built on the Business Partner (BP) table. It includes multiple tabs for detailed management.

---

## 🧭 Navigation

- Access via: **ERP → Employee window**

---

## 🛠️ Functionality

- View and edit employee details in the main tab, including personal (e.g., Name, Gender), employment (e.g., Position, Supervisor), status, and view audit information.
- Switch to the **Contact** tab for managing communication details, such as Email Address, Phone, Password, and Comments.
- Use the **Activity** tab to add and view activities related to the employee, such as phone calls, emails, and meetings.
- Access the **Location** tab to add and view locations associated with the employee.
- Manage credentials in the **Credentials** tab — view, edit, and add qualifications or certifications for the employee.
- Check the **Validation** tab to identify any validation issues. If the employee is unvalidated (tickbox not ticked in the header), it indicates issues like missing required credentials for their position.
- See [Active-Tickbox](Active-Tickbox.md) for management of employee statuses.

---

## ✅ Key Actions

| Action | Steps |
|--------|-------|
| **Create a new employee** | ERP → Employee window → New Record |
| **Update employee details** | ERP → Employee window → Edit fields (e.g., Name, Position, Email Address) |
| **Manage contact details** | ERP → Employee window → Contact tab → Edit fields (e.g., Title, Description) |
| **Log activities** | ERP → Employee window → Activity tab → Add New Activity (e.g., Phone Call, Email, Meeting) |
| **Add or edit locations** | ERP → Employee window → Location tab → Add/Edit Location |
| **Manage credentials** | ERP → Employee window → Credentials tab → Add/Edit Credentials |
| **Check validation status** | ERP → Employee window → Validation tab → Review Issues |
| **Save changes** | ERP → Employee window → Save button |

---

## 📝 Notes

- **Note on Data Duplication**:  
  Some fields in this window (e.g., Name, Position, Supervisor) are duplicated from the User table and also appear in the Business Partner (BP) table. When you enter data in the Employee window, it updates the corresponding User table fields, which become read-only when accessing the User window directly for employees.

- **Employee Definition**:  
  An employee is identified by the **Employee** checkbox in the BP table.

- **Contact Restriction**:  
  Only one contact/user per employee is allowed. For family members or related parties, use the **BP Associations** function.

- **Validation Plugin**:  
  The Validation tab links to the [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md) for detailed issue resolution and management, as validation is a larger topic.

---
(end of note)
