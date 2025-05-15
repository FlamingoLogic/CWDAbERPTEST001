---
aliases:
  - Tool-ClaimType
  - Claim-Type-Setup
tags:
  - workinstructions
  - tool
  - claiming
  - ndis
  - abilityerp
  - lookup
---

# 🏷️ Claim Type

*Matt Law | Last Updated: 2025-05-15*

This tool is used to maintain **Claim Types** in AbilityERP. Claim Types are referenced on **Service Bookings** and **Invoices** and are particularly important for NDIS-related service claiming. Each type reflects a specific circumstance under which a claim is made (e.g., Cancellation, Non-Face-to-Face Support, Travel).

---

### 📚 Description
The **Claim Type** tool is a lookup window used to define and manage categories for claiming in line with NDIA rules. These are not pricing items but classifications that affect how and when a claim can be made.

---

### 🧭 Navigation
- Access via: **Main Menu => Claim Type window**
- Or: Clickthrough field on the **Claim Type** field in a [Service-Booking](Service-Booking.md) or **[Invoice-(Customer)](Invoice-(Customer).md)**

---

### 🛠️ Functionality
- Maintains valid Claim Types for use on Bookings and Invoices
- Includes:
  - **Search Key** (short code)
  - **Name** (label)
  - **Description** (use case or NDIA rule reference)
  - **Active flag**
- Example types include:
  - `CANC` – Cancellation (Short Notice)
  - `NF2F` – Non-Face-to-Face Support
  - `TRAN` – Travel
  - `THLT` – Telehealth
  - `IRSS` – Irregular SIL Support
  - `UATD` – Unable to Deliver
  - `REPW` – NDIA Required Report (tracking only, not claimable)

---

### 🎯 Tips
- **Leave blank** for standard claims — only set when needed under NDIS rules.
- Ensure Claim Types match current NDIA claiming guidelines.
- Use descriptions to guide users (e.g., CANC = Short Notice Cancellation).
- Do **not** delete old types — deactivate instead.

---

### 📝 Notes
- This field is required for some NDIS claim lines.

---
(end of note)
