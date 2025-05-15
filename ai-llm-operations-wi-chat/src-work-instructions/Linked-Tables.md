---
aliases:
  - Linked Tables
tags:
  - sysadmin
  - tool
  - application-dictionary
  - dataaccess
---

# 🛠️ Linked Tables

*Adam Sawtell | Last Updated: 2025-05-01*

Manages relationships between iDempiere entities using junction tables, enabling bidirectional access in window tabs (e.g., linking users and roles).

---

## 📚 Description  
Linked Tables are managed via junction tables (e.g., `AD_User_Roles`) and displayed in tab format on related windows. This enables users to view and edit many-to-many relationships, such as assigning multiple roles to a user or multiple users to a role.

---

## 🧭 Navigation  
- **Main menu** → **System Admin**  
  - → **User** window → *Role* tab  
  - → **Role** window → *User* tab

---

## ⚙️ Functionality  
- Establishes many-to-many links using a junction table:
  - Example: `AD_User_Roles` links `AD_User` and `AD_Role`.
- UI tabs display linked records using filters:
  - In **User** window → Role tab shows roles for the user.
  - In **Role** window → User tab shows users with that role.
- Adding/removing a link updates the junction table (`AD_User_Roles`) without modifying the primary tables.
- Tab filters use SQL syntax like:  
  `AD_User_ID = @AD_User_ID@` or `AD_Role_ID = @AD_Role_ID@`

---

## 💡 Tips  
- Use Application Dictionary → **Tab** to inspect or adjust link filters.  
- When troubleshooting display issues, ensure tab SQL filters reference the correct parent column.  
- Always use junction tables for many-to-many relationships to avoid data duplication.  
- Test in a sandbox: deleting a junction record removes the relationship only—parent records remain unaffected.

---

## 📝 Notes  
- No development is required to manage linked tables—configuration is done via the Application Dictionary.  
- This is a key method for managing relationships across users, roles, templates, and custom request workflows.

