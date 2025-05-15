---
aliases:
  - Request Template Plugin
tags:
  - workinstructions
  - tool
  - plugin
  - automation
  - efficiency
  - compliance
  - request
---

# 🏷️ Request Template Plugin

*Matt Law | Last Updated: 2025-04-30*

This document defines the **Request Template Plugin** in AbilityERP—its functionality, navigation, automation logic, and use in supporting structured, consistent workflows for organisational tasks and approvals.

---

### 📚 Description

The Request Template Plugin enables templating of requests by adding a "Template" tickbox to the Request table. It supports automation, consistent request creation, role/status logic, and document binding (e.g. to invoices or bookings). This is particularly useful for common processes such as credential expiry alerts, shift changes, or approval workflows.

---

### 🧭 Navigation

- Access via: **AbilityERP => Request (all)** window  
- Filter using the **Template** tickbox

---

### 🛠️ Functionality

- Enable request templates by ticking the **Template** checkbox on a Request
- Reveals two additional tabs when active:
  - **Request Document Action Mapping**  
  - **Request Status User/Role Mapping**
- Allows linking a request to a document and automating action based on request status
- Trigger request creation using:
  - **Button** (e.g., “Create Request from Template” on Sales Order)
  - **Scheduled process** (e.g., credential expiry check)

---

### ⚙️ Automation Considerations

> ⚠️ **Creating a template does not trigger requests automatically.**

To automate request creation, a **custom process** is required.

**A typical process must:**
- Identify records meeting a condition (e.g., expired credentials)
- Retrieve and populate required fields (e.g., Business Partner, Activity, Category)
- Create a request using the correct template
- Optionally assign user/role and set the request group

For **scheduled automation**, the process must be:
- Attached to a [Scheduler](Scheduler.md) entry  
- Configured for frequency (e.g., daily, weekly)

🛠️ **Key Notes:**
- Templates define request logic and structure—not record triggers  
- All dynamic triggers (button-based, document-based, or timed) require a custom process  
- Reference records (e.g., a participant or invoice) must be populated by the custom process

---

### 📝 Field Details

- **Template Tickbox**: Marks a request as a template  
- **Request Document Action Mapping**: Maps request status changes to document actions (e.g., approve Sales Order)  
- **Request Status User/Role Mapping**: Assigns roles or users by request status  

---

### 🎯 Tips

- Use templating for repeatable tasks (e.g., missing shift note, overdue review)
- Hide templates from standard windows—use templating windows only
- Use [Templating](Templating.md) logic for doc types or tickbox-based filtering
- Combine with [Request-Group](Request-Group.md) for better origin tracking  
- Configure cron jobs for weekday-only schedules if needed
- Bind to transactional windows like:
  - [Sales Order](Sales-Order.md)
  - [Invoice (Customer)](Invoice-(Customer).md)

---

### 🔧 Related Tools

- [Templating](Templating.md)  
- [Request](Request.md)  
- [Request-Group](Request-Group.md)  
- [Scheduler](Scheduler.md)  
