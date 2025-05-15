---
aliases:
  - Medication Lookup
  - Medication List
tags:
  - workinstructions
  - tool
  - lookup
---

# 🏷️ Medication

*Matt Law | Last Updated: 2025-05-07*

This document outlines the use of the **Medication** window in AbilityERP.  
It provides a simple lookup list of medications, primarily used in the **[Restrictive-Practices](Restrictive-Practices.md)** tab, but may also support other modules where medication references are required.

---

### 📚 Description
The **Medication** window stores a static list of available medications for selection.  
This list supports standardisation and audit-readiness when documenting chemical restraints or health-related entries across the system.

---

### 🧭 Navigation
- Access via: **Main Menu** → type **"Medication"** in the search bar
- Used as a lookup field in:  
  - **Restrictive Practices Tab** (Support Receiver)

---

### 🛠️ Functionality

#### Fields
- **Search Key**: Short code or label for system use (e.g., "RISPER").
- **Name**: Full medication name (e.g., "Risperidone").
- **Description**: Optional notes for clarification.
- **Active**: Only active records appear in lookup fields.

---

### 🎯 Tips
- Avoid duplication — use clear, consistent naming conventions.

---

### 📝 Notes
- Table: `AbERP_Medication`
- This list is managed centrally and referenced, not linked to stock or prescribing systems.

---
(end of note)
