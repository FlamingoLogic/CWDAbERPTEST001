---
aliases:
  - Activities
  - Dashlets
  - Home Screen Workflow
tags:
  - workinstructions
  - tool
  - ui
  - workflow
  - dashboard
  - dataaccess
  - efficiency
  - compliance
---

# 🏷️ Activities and Dashlets

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the Activities and Dashlets feature in AbilityERP — used to guide users to pending work and display actionable tasks from the homescreen.

---

## 📚 Description  
The Activities and Dashlets feature in AbilityERP (AbERP) and iDempiere provides a homescreen interface to display actionable insights and tasks for users. Activities, also referred to as document status indicators, highlight records needing attention (e.g., exemptions and queue-based workflows). Dashlets are customizable sections on the homescreen that group activities. This feature directs users to pending work and allows navigation directly to relevant records.

---

## 🧭 Navigation  
- Access via: Homescreen (default view upon login to AbilityERP).

---

## 🛠️ Functionality  
- Displays activities on the homescreen, grouped into dashlets.

### 📌 Activities (Document Status Indicators)
- Show records needing action:
  - Commonly used for exemptions and queue-based workflows.
  - Direct users to records meeting specific conditions (e.g., unapproved records, pending tasks).
  - Configured in iDempiere via the Document Status setup:  
    *System Admin → General Rules → Document Status*
  - Conditions or flags on tables/windows define which records appear as activities.
  - Can be simplified by adding a tickbox/flag on a window to mark records for activity inclusion — which also enables filtering via search.

### 🧱 Dashlets
- Group activities and metrics into homescreen sections:
  - Multiple dashlets can be configured.
  - Homescreen visibility can be customised per role (e.g., finance roles see finance-related dashlets).
  - Clicking an activity navigates directly to the relevant window and filtered records.

---

## 🎯 Tips  
- Configure the homescreen to show only relevant dashlets per role (e.g., hide finance dashlets for non-finance users).  
- Use tickbox/flag fields to simplify activity logic and support search filters.  
- Regularly review activity conditions to ensure they remain accurate and actionable.  
- Ideally, a user’s entire workload should be visible and accessible via activities.  
- Recent iDempiere versions allow KPIs to appear in activities — however, **Metabase** can also be used for advanced visual reporting.

---

## 📋 Examples  

### Enquiry and Opportunity  
- (Placeholder for future examples)

### Service Planning  
- (Placeholder for future examples)

### Service Delivery  
- (Placeholder for future examples)

### Claiming, Finance and Vendor Management  
- BPs with unapproved bank accounts  
- Unposted documents  
- Postings to a 9 account  
- Unprocessed documents

### Client Management  
- (Placeholder for future examples)

### Employee Management  
- Available Shifts

### Incident Management  
- (Placeholder for future examples)

### Quality & Safeguarding  
- (Placeholder for future examples)

### My Activity  
- My Approvals: Unavailable / Leave

---
(end of note)
