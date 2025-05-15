---
aliases:
  - Request Outcome
  - Resolution Code
tags:
  - workinstructions
  - tool
  - request
  - workflow
  - lookup
---

# 🏷️ Request Resolution

*Matt Law | Last Updated: 2025-05-01*

The **Request Resolution** tool in AbilityERP defines clear outcomes for requests (e.g., Approved, Declined) when status alone (like Closed) does not capture the result. It enhances clarity in reporting and process closure.

---

## 📚 Description

Use this tool to add resolution outcomes that complement a request’s [Request-Status](Request-Status.md), offering better auditability and accuracy in workflows.

---

## 🧭 Navigation

- Access via: **Main menu => Request Resolution** window  
- Or: Open from the **[Request](Request.md)** window via the **Request Resolution** field

---

## 🛠️ Functionality

- Define specific outcomes like “Approved,” “Declined,” or “Needs Follow-up”
- Used as a **lookup field** on the Request window, allowing users to tag a resolution in addition to setting a status
- Often tied logically to request types (e.g., “Corrective Action” requests may use resolutions like “Fix Implemented”)

---

## 💡 Tips

- Use concise and self-explanatory resolution names for easy filtering and reporting
- Common examples: `Approved`, `Declined`, `Escalated`, `Implemented`

---

## ⚠️ Notes

- Ensure resolutions are aligned with the [Request-Status](Request-Status.md) flows used in the associated [Request-Type](Request-Type.md)
- It is common to create a link table between [Request-Type](Request-Type.md) and Request Resolution for logical grouping and control

---
(end of note)
