---
aliases:
  - Advanced Search View
  - Flattened Search Window
tags:
  - workinstructions
  - tool
  - reporting
  - efficiency
  - dataaccess
---

# 🏷️ Advanced Search

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use Advanced Search in AbilityERP — a method for enabling search across both header and tab data via flattened views.

---

## ⚠️ IMPORTANT NOTE  
Once we have backported advanced search features from a newer version of iDempiere or upgraded, there is no longer a need to create flattened views solely for the purpose of advanced search (ability to search on tab details). Note there are definitely good reasons to still use views or standard windows for purposes like [Queue-based-workflow](Queue-based-workflow.md). Relevant iDempiere Jira tickets are 3760 and 4087.

---

## 📚 Description  
Advanced Search involves creating a view that flattens a header window and tab structure into a single view exposed within a window, enabling standard window features like search to be applied to the combined dataset.

---

## 🧭 Navigation  
- Access via: Main menu => Custom Window (where the flattened view is configured).  
- Or: Open via an activity on the home screen.

---

## 🛠️ Functionality  
- Creates a flattened view by combining header and tab data (e.g., merging headers with lines).  
- Exposes the view as a searchable window, allowing queries across all fields (e.g., search by tab details like line items).  
- Requires table and window setup, therefore a developer is usually required for initial setup, though it's a simple task.

---

## 🎯 Tips  
- Use advanced search only if backported features or upgrades are not yet available.  
- Test the flattened view in a sandbox to ensure all header and tab data is correctly merged.  
- Document the view configuration in the Application Dictionary for future reference.  
- Consider [Queue-based-workflow](Queue-based-workflow.md) as a broader alternative use case for views.

---
(end of note)
