---
aliases:
  - Generate Invoices
tags:
  - workinstructions
  - tool
  - finance
  - claiming
---

# 🏷️ Generate Invoices Process

*Matt Law | Last Updated: 2025-05-14*

This document defines the Generate Invoices Process functionality, navigation, tips, and related tools within the organisation’s systems and processes.

---

### 📚 Description

The **Generate Invoices Process** in AbilityERP automates the creation of invoices from open [Sales-Order](Sales-Order.md) and [Service-Booking](Service-Booking.md) records. It respects invoice rules, allows invoice consolidation, and supports large-scale batch processing — with additional filters to improve control, especially for service-based invoicing.

---

### 🧭 Navigation

- Access via: **Main Menu → Generate Invoices**

---

### 🛠️ Current Functionality

- **Core Features**:
  - Generate invoices from eligible completed orders.
  - Apply Document Action (e.g. Prepare, Complete) after generation.
  - Consolidate invoices for the same business partner when invoice rules and bill-to location allow.
  - Filter by Order, Business Partner, Invoice Partner, or Activity.

- **Standard Parameters**:
  - **Organization**: Required
  - **Date Invoiced**: Used to date the generated invoices.
  - **Minimum Amount**: Skips orders under this amount.
  - **Run as Job**: Processes in the background.
  - **Consolidate to One Document**: Combines orders with same bill-to into one invoice.

- **Note on Activity Filter**:  
  Activity filtering will currently include an order even if only one line has the selected activity. This behaviour is being corrected (see enhancements below).

- **Selection Logic**:  
  Eligible records are drawn from `RV_Order_Open` — which filters for completed orders not yet fully invoiced, based on invoice rule logic (e.g., "After Delivery", "Immediate").

---

### 🆕 Upcoming Enhancements *(Coming May–June)*

> These changes will improve NDIS claiming safeguards and line-level control for bookings.

#### ✅ New Parameters

| Parameter               | Type                        | Default           | Purpose                                                                 |
|------------------------|-----------------------------|-------------------|-------------------------------------------------------------------------|
| **Ready to Claim**     | Dropdown (Yes / No / Ignore)| Yes               | Only invoice lines where `Ready to Claim = TRUE`.                       |
| **Exclude Manual Hold**| Checkbox                    | TRUE              | Exclude lines where `Manual Hold = TRUE`. Prevents billing of blocked records. |
| **Price List**         | Dropdown                    | Blank             | Filter by Price List on Order Header.                                  |
| **Master Location**    | Info Window Lookup          | Blank             | Filter by Master Location on Order Header.                             |
| **Start Date**         | Date                        | Blank             | Filter where **Booking Line End Date ≥ Start Date**.                   |
| **End Date**           | Date                        | Blank             | Filter where **Booking Line End Date ≤ End Date**.                     |
| **Activity**           | Dropdown                    | Blank             | Will filter by Order Header Activity only (bug fix).                   |

#### 🔁 Behaviour Improvements

- **All filters apply using AND logic.**
- **Date filtering** uses **Booking Line End Date** (not `DatePromised`).
- **Ready to Claim** and **Manual Hold** are **line-level controls** and take effect before invoicing.
- **Bug fix**: Activity filter will no longer include orders where only one line has the matching activity — it will match `C_Order.C_Activity_ID` only.

#### ⚠️ Popup Warnings

- If `Ready to Claim = Ignore`:
  > "Warning: You are generating invoices without filtering on Ready to Claim. Are you sure you want to continue?"

- If `Exclude Manual Hold = FALSE` and matching records exist:
  > "Warning: You have chosen to include booking lines that are manually held. This may result in invoices being generated for services marked as non-claimable by staff. Are you sure you want to continue?"

---

### 🎯 Tips

- Use **Ready to Claim = Yes** and **Exclude Manual Hold = TRUE** for routine invoicing.
- Start with **Document Action = Prepare** to allow review before posting.
- Filter by **Price List**, **Master Location**, or **Activity** to manage structured runs.
- To support claiming setup, see [[Service-Booking]] and [[Booking-Validation-Preparation]]

---

### 📝 Notes

- Related fields:
  - `AbERP_ReadyToClaim` (Booking Line)
  - `AbERP_ManualHold` (Booking Line)
- These changes are part of the broader compliance and claiming improvement roadmap.
- Ticket ref: `Zammad 901354` / `Logilite: 1012731` (Activity filter fix)

---
(end of note)
