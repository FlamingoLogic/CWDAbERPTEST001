---
aliases:
  - Partner Relation
  - BP Association
tags:
  - workinstructions
  - tool
  - finance
---

# 🏷️ Partner Relation

*Matt Law | Last Updated: 2025-05-07*

This document outlines the functionality and use of the **Partner Relation** window in AbilityERP (iDempiere core window). It allows users to create and manage relationships between Business Partners, such as identifying a plan manager, funding body, or related entity with specific addressing requirements.

---

### 📚 Description
The **Partner Relation** window is used to define a named relationship between two Business Partners.  
This is commonly used in NDIS scenarios where a **participant is linked to a plan manager**, or an **funding body**, with address flags such as "Invoice To".

---

### 🧭 Navigation
- Access via: **Main Menu** → **Partner Relation** (or search "partner" to find it).

---

### 🛠️ Functionality
- Define a custom name for the relationship (e.g., "Amelia's Plan Manager").
- Select the **primary Business Partner** (e.g., Amelia Martin).
- Use the **Proxy section** to link this to a **Related Partner** (e.g., Security Health Plan Manager).
- Set address purposes:
  - **Ship Address**
  - **Pay-From Address**
  - **Invoice Address**
  - **Remit-To Address**
- Specify a **Related Partner Location** (e.g., ADELAIDE).
- Optionally specify a **Partner Location** on the main group.

---

### 🎯 Tips
- Use clear and consistent naming in the *Name* field to reflect the relationship (e.g., "[Participant Name]’s Plan Manager").
- Only tick **Pay-From** or **Invoice** address if that partner is responsible for payment.
- If the related partner handles multiple participants, ensure each relation is created with a distinct name.

---

### 📝 Notes
- Relationships created here may be used in reporting, invoice generation, and routing logic.
- This window updates the `C_BP_Relation` table.
- Avoid duplicating entries unless intentional (e.g., multiple addresses).

---
(end of note)
