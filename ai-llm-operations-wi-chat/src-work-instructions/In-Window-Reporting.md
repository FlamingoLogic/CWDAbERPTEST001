---
aliases:
  - In-Window Reporting
  - View-Based Reporting
tags:
  - workinstructions
  - tool
  - reporting
  - dataaccess
  - ui
  - customisation
---

# 🏷️ In-Window Reporting

*Matt Law | Last Updated: 2025-05-01*

Also called View-Based Reporting Window. This document outlines how In-Window Reporting works within AbilityERP using read-only views exposed in a window, with optional editable tabs, action buttons, and full window toolbar support.

---

### 📚 Description
In-Window Reporting uses a database view — often joining multiple tables and including calculated fields — exposed via a standard iDempiere window.  
This enables powerful reporting with toolbar options, drill-downs, saved queries, status indicators, and editable subtabs.

---

### 🧭 Navigation
- Access via: Main menu => [Window Name where the view is configured]
- Or: Link from dashboards, activities, or queue-based workflow screens

---

### 🛠️ Functionality
- Read-only main window based on a SQL view combining multiple tables
- Includes calculated fields (e.g., totals, durations, counts)
- Supports:
  - Standard toolbar features (search, saved filters, export, etc.)
  - Click-throughs to original records (via `Record_ID`)
  - Buttons to trigger defined processes per row (e.g., Allocate, Create Request)
  - Editable subtabs linked to the selected row (via foreign key)
  - Visual indicators (e.g., coloured `DocStatus`, status flags)
  - Zoom Across to related records (e.g., to Business Partner, Invoice, etc.)

---

### 🎯 Tips
- Use status indicators or QuickInfo panels to highlight required actions
- Add prepared filters to improve load time and avoid overwhelming users
- Document the view logic and join conditions in the Application Dictionary
- Include `AD_Org_ID`, `AD_Client_ID`, and `Record_ID` in the view for filtering and drilldown
- Restrict access using Role => Window Access if sensitive information is included
- Use indexed columns and date/status filters to optimise performance

---

### 📝 Optional: Notes
- A well-built view can replace static BI reports while allowing real-time, actionable interaction
- Consider combining multiple document types using `CASE` logic in the SQL (e.g., unified transaction reporting)
- Views do not support direct edits — use subtabs or buttons for updates
- Zoom Across and click-throughs only work if `Record_ID` and appropriate references are present

---

### 🚀 Optional: Enhancements
- Add row-level action buttons (e.g., Send Reminder, Approve, Create Task)
- Add AI-assisted QuickInfo or suggestion panels based on business rules
- Introduce parameter-based filtering for context-driven views (e.g., by program, region, or timeframe)
- Support queue-based workflows with flags that determine visibility

---

### 🛠️ Optional: Related Tools
- [Advanced Search](Advanced-Search.md)
- [Queue-based-workflow](Queue-based-workflow.md)
- [[Quick-Info]]


---
(end of note)
