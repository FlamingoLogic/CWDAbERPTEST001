---
aliases:
  - Support Receiver Locations
  - BP Location Tab
  - Participant Address Tab
tags:
  - workinstructions
  - tool
  - operations
  - client
---

# 🏷️ Locations Tab

*Matt Law | Last Updated: 2025-05-07*

This document describes the **Locations** tab used to manage addresses for a Support Receiver or general Business Partner in AbilityERP. It is part of the `C_BPartner_Location` table and is accessible under **Business Partner** windows.

---

### 📚 Description
The **Locations** tab allows you to define one or more addresses for a Business Partner. Each address can have multiple purposes, such as billing, invoicing, support delivery, or home address.  
You can also link a **Master Location** [Master-Location](Master-Location.md) (also referred to as a **Contract Location**) to reuse a central address record across multiple business partners or support receivers.

---

### 🧭 Navigation
- Access via:
  - **[Support-Receiver-(BP)](Support-Receiver-(BP).md)** → *Locations tab*
  - [(DRAFT)Business-Partner]((DRAFT)Business-Partner.md) → *Locations tab*
  - **[Employee](Employee.md)** → *Locations tab*
- This tab is not accessible as a standalone window.

---

### 🛠️ Functionality

#### Core Fields
- **Address***: The primary address field (mandatory).
- **Name***: A label for the address (e.g., “Home”, “SIL Site A”).
- **Contract Location**: (Optional) Link to a central address (Master Location) to reuse existing locations.
- **Description**: Internal notes or identifiers.

#### Address Flags (can select multiple)
- **Pay-From Address**: Used when this address should be used for payment.
- **Invoice Address**: Used for billing purposes.
- **Remit-To Address**: Used for receiving remittance advice.
- **Support Address**:  Used for rostering and operational delivery (e.g., SIL homes).
- **Home Address**: Identifies the BP's primary residence.
- **Master Location Submitted**: Indicates the location has been proposed as a reusable master.
- **Rooms Exist**: Indicates if rooms are enabled on a support location.

#### Contact Details (optional)
- **Phone / 2nd Phone / Fax** fields can be included for site-specific contact info.

---

### 🚀 Submitting a Master Location

If a location should be added to the central master list (also called Contract Locations), follow these steps:

1. **Create the location** as usual under any Business Partner.
2. Tick the **Submit to Master List** checkbox.
3. Click the **AbERP Submit Master Location** button that appears below.
4. The system will replicate the address into the `AbERP Master Location` business partner’s record for reuse across the system.

> Note: it is good practice to check the [Master Location](Master-Location.md) window before submitting.

---

### 🎯 Tips
- Use **Master Location** to standardise frequently used addresses across clients or services.
- Always flag the correct **Support Address** or **Home Address** — these drive rostering and service logic.
- Keep the **Name** field clear and consistent (e.g., “Unit 2 SIL – Prospect”).

---

### 📝 Notes
- This tab stores records in the `C_BPartner_Location` table.
- - This tab stores data in `C_BPartner_Location`, which holds the purpose, flags, and contact details tied to a Business Partner.
- The underlying address (entered via the **Address** field) references a unique record in the `C_Location` table. The system automatically creates or reuses an existing location record based on exact match logic.
- The **Master Location Submitted** checkbox and **AbERP Submit Master Location** button are AbilityERP-specific extensions used to promote an address into the reusable master list.


---

### 🛠️ Related Tools
- [Master-Location](Master-Location.md)
- [Support-Location](Support-Location.md)

---
(end of note)
