---
aliases:
  - Queue-Based-Workflow
  - Workflow Queues
tags:
  - workinstructions
  - tool
  - efficiency
  - workflow
  - reporting
---

# 🏷️ Queue-Based Workflow

*Matt Law | Last Updated: {{date}}*

This document outlines how to implement and use queue-based workflows within AbilityERP to help users see exactly what requires action — by role — using filtered windows, saved queries, document flags, and the Home Screen.

---

### 📚 Description
Queue-Based Workflow is a practical pattern for surfacing records that require action from specific roles.  
Rather than relying on separate reports or dashboards, users see a curated “to-do list” directly in their ERP — using filters, flags, and structured views.

This is not a workflow engine. It’s a smart use of native iDempiere features like saved searches, document status indicators, and custom windows to mimic queue behavior.

> **If a user asks “What should I do next?”, a queue is the answer.**

---

### 🧭 Navigation
- Access via: Home Screen => Activity Tile (linked via document status indicator)
- Or: Main menu => Window or View configured for queue filtering

---

### 🛠️ Functionality
- Flags records that need action (e.g., `Unallocated`, `Ready to Claim`, `Missing Receipt`)
- Surfaces them on the Home Screen using:
  - **Saved Filter Queries**
  - **Document Status Indicators**
- Can point to:
  - A **standard window** using a single-table filter
  - A **view-based window** for multi-table data and calculated fields
- Optional features include:
  - Buttons to trigger processes (e.g., Create Request, Allocate Staff)
  - Editable subtabs to resolve the record directly from the queue
  - QuickInfo panels to show compliance or related context

---

### 🎯 Tips
- Start simple — a standard window with a saved filter is often enough
- Add a document status field like `Queue_Status` to drive queue logic
- Design queues per role to minimise clutter and confusion
- Use colour indicators or icons in status fields to improve triage speed
- Document queues consistently to aid AI agents or new staff navigating the system

---

### 🧠 Real-World Examples by Role

| Role               | Queue Example                               | Source               |
|--------------------|---------------------------------------------|----------------------|
| Rostering Team     | “Shifts Missing Staff”                      | View with allocation logic |
| Finance            | “Invoices Missing Receipts”                 | Filtered Invoice window |
| Compliance Officer | “Expired Credentials”                       | Credential view with expiry logic |
| Service Delivery   | “Bookings Not Claimed”                      | Booking view with status |
| Admin / Onboarding | “New Clients Missing Support Plan Upload”   | Request window with doc check |
| HR / Workforce     | “Unassigned Mandatory Training”             | View-based with training joins |

---

### 📝 Notes
- Queue-based workflows are the **fastest and cheapest** method to create task visibility in AbilityERP
- Can be implemented with no development (just flags and filters) or enhanced with views, buttons, and QuickInfo
- Great entry point for process automation or AI agent handoffs

---

### 🚀 Enhancements
- Add row-level action buttons for common tasks (e.g., Mark as Complete)
- Trigger automated request creation based on queue conditions
- Use validation plugins to block records that fail critical checks
- Assign queue ownership to AI agents or bots for triage

---

### 🛠️ Related Tools
- [Advanced Search – Orders](Advanced-Search-Orders.md)
- [In-Window-Reporting](In-Window-Reporting.md)
- [Activities-and-Dashlets](Activities-and-Dashlets.md)
- [Request-Status](Request-Status.md)

---
(end of note)
