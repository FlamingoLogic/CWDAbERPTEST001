---
aliases:
  - Request Source Group
  - Template Request Origin
tags:
  - workinstructions
  - tool
  - request
  - lookup
---

# 🏷️ Request Group

*Matt Law | Last Updated: 2025-05-01*

The **Request Group** tool in AbilityERP is used to classify the **origin** of a request—especially useful for templated or automated requests created by the [Request-Template-Plugin](Request-Template-Plugin.md).

---

## 📚 Description

Request Groups help identify where a request came from (e.g., Scheduled Daily, Originated from Customer). This enables better reporting, filtering, and visibility, particularly in environments with high automation.

---

## 🧭 Navigation

- Access via: **Main menu => Request Group** window  
- Or: Open directly from the **[Request](Request.md)** window via the **Request Group** field click-through

---

## 🛠️ Functionality

- Define and maintain **request origin labels** (e.g., Scheduled Daily, Referral Intake)
- Request Groups are **auto-populated** from the [Request-Template-Plugin](Request-Template-Plugin.md) and are **read-only** on the resulting request
- Optional: Assign **email notifications** to users when requests are created with specific groups (rarely used)

---

## 💡 Tips

- Use clear, descriptive names (e.g., “Originated from Customer”, “Auto Generated via Intake Form”)
- Create **separate templates** with different request groups to distinguish request origins in reports
- Use request groups for **insight**, not logic—workflow rules should still live in [Request-Type](Request-Type.md) or [Request-Status](Request-Status.md)

---

## ⚠️ Notes

- **Email notifications** for request groups are optional and rarely used in practice
- Ignore the **Change Notice** and **BOM Formula** fields—these are deprecated legacy fields and not required

---
(end of note)
