---
aliases:
  - Address Master
  - Global Address Register
tags:
  - workinstructions
  - tool
  - admin
  - operations
---

# 🏷️ Location

*Matt Law | Last Updated: 2025-05-09*

This document defines the Location window functionality, navigation, tips, and related tools within the organisation’s systems and processes. This is a core iDempiere window tied to the `C_Location` table.

---

### 📚 Description

The **Location** window in AbilityERP (iDempiere core) stores all unique postal address records used system-wide. These are deduplicated reference records used in Business Partner Locations, Warehouses, Organizations, Master Locations, and more.

When an address is entered via another window (e.g., the Locations tab on a Business Partner), the system checks for a match and reuses the existing location if one is found — avoiding duplication.

---

### 🧭 Navigation

- Access via: `Main menu => Location`
- Typically used by Admin or System roles only.

---

### 🛠️ Functionality

- Stores unique address records including:
  - **Address 1–5**
  - **City, ZIP, Region, Country**
  - Optional: **Additional Zip**, **Additional Region**, **Result**, **Comments**
- Used as a reference in:
  - **Business Partner → Locations tab**
  - **Warehouse**
  - **Organization**
  - **Master Location** and **Support Location** indirectly via `C_BPartner_Location`
- Address records are **de-duplicated automatically**. The system will reuse an existing `C_Location` if all core fields match.
- The **Valid** checkbox and **Address Validation** button can optionally be integrated with external postal validation services (not enabled by default).
- Manual edits should be done cautiously, as updates affect every reference to that location.

---

### 🎯 Tips

- Do **not** create new addresses here manually unless required for data correction or testing.
- When entering an address via the Business Partner → Locations tab, the system handles creation and reuse of `C_Location` records automatically.
- Editing this window directly changes the address everywhere it is used.
- Use the **Result** or **Comments** field to document issues or clarification (e.g., PO box-only address, pending verification).

---

### 📝 Notes

- Table: `C_Location` (core iDempiere)
- This window only holds the **physical address** — it does not include any business logic like "Is Support Address" or "Remit-To Address" which live in the `C_BPartner_Location` table.
- All functional address relationships (billing, shipping, home, etc.) are defined in the **Locations tab** of Business Partner, and those records reference this table.
- If address validation integration is enabled, the **Address Validation** button may trigger an external API to verify or format the address.

---

### 🛠️ Related Tools

- [Locations-Tab](Locations-Tab.md)
- [Master-Location](Master-Location.md)
- [Support-Location](Support-Location.md)

---
(end of note)
