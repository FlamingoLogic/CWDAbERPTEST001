---
aliases:
  - Activity Viewer
  - Activity Tab
tags:
  - workinstructions
  - tool
  - client
  - employee
  - operations
  - growth
  - compliance
  - rostering
---

# 🏷️ Activity Viewer

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the Activity Viewer window in AbilityERP — a core tool for creating, viewing, and managing activities such as case notes, goal updates, and contact logs.

---

## 📚 Description  
The Activity Viewer window in AbilityERP (and core iDempiere) manages activities related to various entities, stored in the `C_ContactActivity` table. Each activity tab is associated with a specific window and has unique Activity Types tailored to that context. This tool allows users to view, create, and manage activities, with a specific process on the Support Receiver (BP) window for recurring activities. Activity Viewer is a well-used function, with key tasks including adding Support Receiver case notes and goal progress updates.

---

## 🧭 Navigation  
- Access via: Main menu => Activity Viewer  
- Or: Open directly from activity tabs on related windows (listed below)

---

## 🛠️ Functionality  
- Displays activities from the `C_ContactActivity` table across multiple activity tabs  
- Supports creating, viewing, and editing activities with tab-specific Activity Types  
- Activity tabs are available on the following windows, each with unique Activity Types:
  - [(DRAFT)Business-Partner]((DRAFT)Business-Partner.md) window  
  - [Employee](Employee.md) window  
  - [Support-Location](Support-Location.md) window  
  - [Support-Receiver-(BP)](Support-Receiver-(BP).md) window — includes the AbERP Recur Lines process (see below)  
  - [Service-Opportunity](Service-Opportunity.md) window  
  - Contact window  
  - [Shift-(Rostered)](Shift-(Rostered).md) window  
  - [(DRAFT)Plan-&-Assessment]((DRAFT)Plan-&-Assessment.md) → Support Plan → Goals  
  - [(Draft)Incident-Report]((Draft)Incident-Report.md) *(note: these activities don't show on the Activity Viewer)*  
- Note Activities can also be created on and will show on the [[(Draft)Calendar]]
- Key fields include Activity Type, Start Date, and End Date

---

### 🔁 AbERP Recur Lines Process *(Support Receiver (BP) Window Only)*  
- Accessed via the process toolbar icon on the Support Receiver (BP) window activity tab  
- Allows recurring an activity up to a specified End Date with a pattern (Daily, Weekly, Monthly)  
- **Parameters**:
  - **Starts On**  
  - **Ends On**: Set the end date for the recurrence  
  - **Recurrence Pattern**: Select Daily, Weekly, or Monthly  
- Activities created via this process are stamped with a field identifying the recur instance, enabling easy lookup or deletion

---

## 🎯 Tips  
- Use the **recur instance** field to bulk-delete activities if a recurrence needs to be undone

---
(end of note)
