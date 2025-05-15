---
aliases:
  - Request Workflow Status
  - Request Lifecycle
tags:
  - workinstructions
  - tool
  - request
  - workflow
  - lookup
  - efficiency
  - compliance
  - automation
  - configuration
---

# 🏷️ Request Status

*Matt Law | Last Updated: 2025-05-01*

The **Request Status** tool in AbilityERP defines the lifecycle stages of a request. It allows structured workflows—such as Action Sets or Approval Sets—to be built into requests, enabling automation, access control, and reporting across your organisation.

---

## 📚 Description

Request Statuses group into categories (e.g., "Action Set") and define how a request progresses from open to closed. Statuses are assigned to [Request-Type](Request-Type.md) configurations and drive both automation and user access within AbilityERP.

---

## 🧭 Navigation

- Access via: **Main menu => Request Status** window  
- Or: From the **[Request](Request.md)** window via the **Status** field click-through

---

## 🛠️ Functionality

- Create **status categories** (e.g., Action Set, Approval Set)
- Control behavior using flags:
  - **Open Status** – Editable and active
  - **Closed Status** – Read-only, no longer displayed in [Request](Request.md)
  - **Final Close** – Triggers processed tickbox and locks record
  - **Open and Close** or **Neither** – For optional or transitional stages
- Use **Sequence** to define status order within the workflow
- **Timeout in Days** can automate movement to the next status (e.g., escalate after 5 days)
- Assign a **Default** status for newly created requests
- Assign statuses to windows beyond the core Request window to **customise workflows**, e.g., for [Corrective Action Requests](Best-Practices-for-Using-Requests-in-Quality-and-Safeguarding.md)

---

## 💡 Tips

- Use clear, short **Search Keys** for easier filtering and automation
- Test **Timeout in Days** transitions in a sandbox before enabling in production
- Add the **Request-Type**, **Request-Status**, and **Processed** fields to windows where you want embedded request logic (very common)

---

## ⚠️ Notes

- Requests with **Closed Status** are only visible in [Request-(all)](Request-(all).md)
- **Web Can Update** field applies only to webstore use cases and should be ignored in standard implementations

---
(end of note)
