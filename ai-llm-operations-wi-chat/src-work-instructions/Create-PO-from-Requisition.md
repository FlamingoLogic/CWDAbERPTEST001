---
aliases:
  - Create Purchase Order from Requisition
  - Requisition to PO
tags:
  - workinstructions
  - tool
  - purchasing
  - process
---

# 🏷️ Create PO from Requisition

*Matt Law | Last Updated: 2025-05-13*

This document outlines how to use the **Create PO from Requisition** process in iDempiere / AbilityERP. It enables users to convert one or more **Purchase Requisitions** into **Purchase Orders**, based on selected filters and consolidation preferences.

---

## 📚 Description  
This process automates the creation of Purchase Orders from approved Purchase Requisitions, reducing manual data entry and ensuring that procurement flows efficiently into purchasing workflows. It supports filtering by requisition attributes, business rules, and consolidation options.

---

## 🧭 Navigation  
- Access via: **Main Menu** => **Create PO from Requisition**

---

## 🛠️ Functionality  

### 🔍 Filters  
- **Requisition**: Optionally select a specific requisition to convert.
- **Organization**: Filter by organization to restrict data scope.
- **Warehouse**: Filter by warehouse linked to requisition lines.
- **Document Date** / **Date Required**: Narrow by requested or required date range.
- **Priority**: Filter by priority assigned to the requisition.
- **User/Contact**: Filter by the user who created the requisition.
- **Product / Product Category**: Limit to specific items or categories.
- **Charge**: Filter requisition lines by charge (non-product) lines.
- **Business Partner Group**: Filter based on vendor category.
- **Project / Campaign**: Link to specific projects or campaigns if applicable.

### ⚙️ Actions  
- **Consolidate to one Document** (Tickbox):  
  - When enabled, lines from multiple requisitions or vendors are grouped into a single Purchase Order (where vendor and other matching fields align).
  - When unticked, separate orders are created per matching group.

- **Run as Job**:  
  - Executes the process in the background (recommended for large volumes).

---

## 🎯 Tips  
- Always ensure requisitions are approved before running this process.
- Use filters to control scope — especially important if not using the Requisition field.
- Use in tandem with [Requisition Window](Requisition.md) for end-to-end purchasing.
- For services, ensure the requisition is linked to the appropriate **Charge** instead of a Product.

---

## 📝 Notes  
- This is a standard core iDempiere process.
- For custom flows, this can be extended with callouts, process automation, or additional filters.
- Consolidation respects vendor, warehouse, price list, and terms alignment.

---
(end of note)
