---
aliases:
  - Purchase Order
  - PO
tags:
  - workinstructions
  - tool
  - purchasing
---

# 🏷️ Purchase Order

*Matt Law | Last Updated: 2025-05-10*

This document defines the Purchase Order window functionality, navigation, and configuration in AbilityERP. It includes both core iDempiere behavior and AbERP-specific enhancements.

---

### 📚 Description

The **Purchase Order** window is used to manage and track purchases from suppliers. It sits between **Requisition** and **Material Receipt** in the typical purchasing flow. While not mandatory, it is a commonly used purchasing document in AbilityERP and can be used with or without a preceding Requisition.

AbERP has added support for extra fields including **Vehicle** and **Master Location**, as well as optional validation and approval logic using the [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md).

---

### 🧭 Navigation

- Access via: `Main Menu => Purchase Order`

---

### 🛠️ Functionality

#### Header Fields
- **Document No / Document Type**: Automatically generated for Purchase Orders.
- **Date Ordered / Date Promised**: Tracks when the order was placed and when delivery is expected.
- **Business Partner**: Supplier for this order.
- **Invoice Partner / Location**: Defaults from the Business Partner but may be adjusted.
- **Payment Term / Rule**: Defines payment logic (e.g., on credit, cash).
- **Currency / Price List**: Defaults based on the BP and Org setup.

#### Reference Fields (AbERP additions)
- **Master Location**: For linking purchases to a central site for reporting or allocation.
- **Vehicle**: Useful for fleet-based expense tracking or delivery-specific items.
- **Project / Activity**: Enables cost attribution for service or capital projects.

#### PO Line Tab
- Add one or more lines with either a **Product** or a **Charge**.
- Can include:
  - **UOM** (e.g., Hour, Each)
  - **Quantity / Price / Tax**
  - **Delivered Quantity / Invoiced Quantity**
- Optional: Use **Master Location**, **Activity**, and **Vehicle** fields at the line level for granular tracking.

---

### ✅ Tips

- You **do not need to use Requisition** — Purchase Orders can be created directly.
- Approval processes and $ limits are often managed via the [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md). You can configure validation to block, warn, or inform based on business logic.
- Use **Master Location** and **Activity** for internal cost tracking.
- To check origin, refer to the **Referenced Order** field to trace back to a Requisition.

---

### 📝 Notes

- This window posts to the `C_Order` table (shared with Sales Orders).
- The **Target Document Type** should be `Purchase Order` — others (e.g., `POS Order`) are intended for customer-facing sales.
- Once marked as **Completed**, the order can be matched to receipts and invoices.
- Document status moves from `Drafted` → `Completed` → `Closed` or `Voided`.
- Line-level delivery and invoicing status do not affect header status — use reporting to track fulfillment.
- Integration with Requisition is optional. To generate POs from Requisitions, use the **Create PO from Requisition** process (separate menu item).

---

### 🛠️ Related Tools

- [Requisition](Requisition.md)
- [Material Receipt](Material-Receipt.md)
- [Invoice-(Vendor)](Invoice-(Vendor).md)
- [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md)

---
(end of note)
