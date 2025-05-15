---
aliases:
  - Request Category Config
  - Request Category Setup
tags:
  - workinstructions
  - tool
  - request
  - lookup
---

# 🏷️ Request Category

*Matt Law | Last Updated: 2025-05-01*

The **Request Category** tool in AbilityERP defines what a request relates to (e.g., Claiming Enquiry), supporting structured reporting and user notifications. It is distinct from [Request-Type](Request-Type.md), which controls request behavior and workflow.

---

## 📚 Description

Request Categories provide a high-level classification for requests. They are used to:
- Support filtering and reporting
- Trigger user notifications
- Avoid overloading [Request-Type](Request-Type.md) with multiple purposes

---

## 🧭 Navigation

- Access via: **Main menu => Request Category** window  
- Or: **Open directly from the Request window** via the **Request Category** field

---

## 🛠️ Functionality

- Define categories like “Claiming Enquiry,” “Quality Issue,” or “Safeguarding Review”
- Assign categories to requests to support visibility and grouping
- Enable optional **email notifications** for specific categories
- Supports **Activities-and-Dashlets** for in-system alerts and tracking

---

## 💡 Tips

- Use short, descriptive names (e.g., `CFV - Claiming Enquiry`)
- Keep category focused — avoid repeating what is already referenced in the request (e.g., incident, employee)
- Use categories for reporting needs, not for workflow logic (that’s for [Request-Type](Request-Type.md))
- Test email triggers in sandbox environments before production use

---

## ⚠️ Notes

- Email notifications are optional and best suited for users not regularly in AbilityERP
- For active users, use **[Activities-and-Dashlets](Activities-and-Dashlets.md)** for more effective task visibility

---
(end of note)
