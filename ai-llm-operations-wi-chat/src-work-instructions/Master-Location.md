---
aliases:
  - Contract Location
  - Master Location View
tags:
  - workinstructions
  - tool
  - operations
---

# 🏷️ Master Location

*Matt Law | Last Updated: 2025-05-07*

This document defines the Master Location view functionality, navigation, tips, and related tools within the organisation’s systems and processes.

---

### 📚 Description

The **Master Location** (also referred to as **Contract Location**) is a view-only window in AbilityERP that consolidates core location data used across multiple business partners and transactions. This prevents duplication and enables dimensional reporting in the general ledger. Master Locations can optionally be linked to a [Support Location](Support-Location.md) for operational and service delivery detail.

---

### 🧭 Navigation

- Access via: `Main menu => Master Location`
- Note: The Master Location window is based on a database **view** (`AbERP_MasterLocation`) and is **read-only**.

---

### 🛠️ Functionality

- Displays all registered master locations across the system.
- Key fields include:
  - **Business Partner**: Always set to `AbERP Master Location`
  - **Partner Location** and **Name**
  - **Full Address**: Including City, Region, and Country
  - **Occupancy Type** (e.g., Adult)
  - **Support Location Type**
  - **Contract Location**: Internal reference ID
- The data is pulled from the **Locations tab** on the `AbERP Master Location` business partner.  
  See: [Locations-Tab](Locations-Tab.md)

---

### 🎯 Tips

- **You do not create or submit a master location directly** in the `AbERP Master Location` window.
  - Instead, create a new **location** on any business partner (e.g., a support receiver), and tick **"Submit to Master List"**.  Then when ready click the submit **AbERP Submit Master Location** button. 
  - This flags the location for submission, and the system will replicate it under the `AbERP Master Location` business partner.

- Use Master Locations in:
  - The **Locations tab** of other Business Partners to avoid duplication
  - Transactional documents for **reporting** and **GL dimension posting**
- Not all Master Locations require a [Support Location](Support-Location.md), but a Support Location can reference an existing Master Location if additional operational fields are required.

---

### 📝 Notes

- This window is **view-only**; updates must be made by submitting from another Business Partner using the **Submit to Master List** checkbox.
- When Master Locations are referenced in transactional records, they enable **standardised reporting** and **GL segmentation** by physical service location.
- Maintain clear naming conventions and check for existing records before submitting.

---

### 🛠️ Related Tools

- [Locations-Tab](Locations-Tab.md)
- [Support-Location](Support-Location.md)

---
(end of note)
