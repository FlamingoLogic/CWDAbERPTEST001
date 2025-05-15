---
aliases:
  - Validation Registry
  - Validation Rules Index
tags:
  - workinstructions
  - tool
  - validation
  - compliance
---

# 🏷️ Validation Tests

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the Validation Tests window in AbilityERP — used to catalogue and manage all validation rules implemented across the system for visibility, review, and audit control.

---

## 📚 Description  
The Validation Tests window is used to catalogue and manage all validation rules implemented in the system. It provides a central record of test names, logic summaries, validation levels, and access control, making it easy to review, audit, and coordinate future updates.

---

## 🧭 Navigation  
- Access via: Main menu => Validation Tests window

---

## 🛠️ Functionality  
- Maintain a full list of all validation tests across all tables  
- Tracks key attributes:
  - Validation name and description  
  - Table and window the test applies to  
  - Validation trigger (e.g., document action, manual validate)  
  - Output format (e.g., validation notes syntax)  
  - Validation level: **Info**, **Warn**, or **Fail**  
  - Code/ticket reference (e.g., GitHub or internal dev link)  
  - Access roles responsible for execution or review  

- **Important**: This window does not execute validation logic. It is an information and administration tool only.  
- Provides system-wide visibility across **custom and standard** validation logic.

---

## 🎯 Tips  
- Enter every new validation test into this window after it is developed  
- Keep descriptions precise and aligned with the intended behaviour  
- Use the **Code Link** field to document implementation references or dev tickets  
- Use the **Access Role/Process** field to clarify responsibility and review scope  
- Include the expected validation note output format for clarity and consistency

---

## 📝 Notes  
- Intended for internal use by system analysts, developers, and quality auditors  
- Especially useful during:
  - System audits  
  - Upgrades  
  - Planning for new validation coverage  
- Filter by table name to quickly identify coverage gaps or overlaps (e.g., for `Shift`, `Invoice`, or `Business Partner`)

---

## 🛠️ Related Tools  
- [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md)  
- [Request](Request.md)

---
(end of note)
