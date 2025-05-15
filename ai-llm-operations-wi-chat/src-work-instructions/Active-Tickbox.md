---
aliases:
  - Active Field
  - Soft Delete
tags:
  - workinstructions
  - tool
  - configuration
  - compliance
---

# 🏷️ Active Tickbox

*Matt Law | Last Updated: 2025-05-01*

This document explains the use of the **Active Tickbox** in AbilityERP — a core field used across many windows to control visibility and editability of records without deleting them.

---

## 📚 Description  
The Active Tickbox is designed primarily as a 'soft delete' mechanism for records that should not have been created but cannot be deleted due to linked records or are retained for audit purposes.

---

## 🛠️ Functionality  
- When unticked, it prevents write access to certain fields on the record, effectively locking it from edits while preserving its data.  
- The tickbox can be re-enabled (ticked) if needed to restore write access.

---

## ✅ Recommended Use  
- Use it to mark records for retention without deletion, ensuring historical data remains accessible for audits.  
- Avoid using it to indicate expiration or inactivity (e.g., for vendors no longer used or resigned employees), as this may block necessary interactions like final payments or outstanding invoices.

---

## 🧠 Best Practice  
- Instead, use separate statuses (e.g., [Request-Status](Request-Status.md)) to track expiration or inactivity, which can also enforce read-only access as needed with the processed tickbox linked to a closed status.  
- This approach allows continued interaction with records (e.g., final pay for a resigned employee) without restrictions imposed by an inactive status.

---

## 🧾 Additional Considerations  
- You don't need to deactivate the Active Tickbox on an employee/user to prevent system access; all roles can be removed to disable access.  
- Update info windows or window opening parameters to exclude records based on the status used, if desired.  
- This is a recommended best practice, not a requirement; you may mark a record inactive if no further interaction is intended, but the alternative status method is preferred for flexibility.

---
(end of note)
