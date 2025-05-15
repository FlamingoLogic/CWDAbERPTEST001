---
aliases:
  - Goods Receipt
  - MM Receipt
tags:
  - workinstructions
  - tool
  - purchasing
---

# 🏷️ Material Receipt

*Matt Law | Last Updated: 2025-05-09*

This document outlines how to use the Material Receipt window in AbilityERP. While originally designed for inventory movement and stock control, this document also covers how Material Receipt can be used in a service context — particularly for confirming delivery prior to invoicing and payment.

---

### 📚 Description

The **Material Receipt** window (also called a **Goods Receipt** or **MM Receipt**) records the receipt of products or services into the system. It is linked to a **Purchase Order** and optionally used to validate that items have been delivered before the supplier is paid.

In iDempiere/AbilityERP, this document:
- Confirms delivery of goods or services
- Creates matching records against [Purchase-Order](Purchase-Order.md)s and (optionally) [Invoice-(Vendor)](Invoice-(Vendor).md)s
- Posts financial entries (e.g., to stock or expense accounts depending on product type)

---

### 🧭 Navigation

- Access via: `Main Menu => Material Receipt`

---

### 🛠️ Functionality

#### Header Fields
- **Purchase Order**: Pulls in the reference order
- **Document Type**: Defaults to “MM Receipt”
- **Movement Date**: Date the items were received
- **Partner Location**: Where the goods/services were delivered
- **Warehouse**: Used even for service receipts, defaults to “Standard”
- **Reference Fields**: Contract Location, Project, Activity, Vehicle (AbilityERP-specific additions)

#### Line Fields
- **Product or Charge**: What was received
- **Quantity**: Received quantity (drives accounting)
- **UOM**: Unit of Measure
- **Reference Fields**: Master Location, Project, Activity, Vehicle

#### Tabs
- **Matched POs / In**
