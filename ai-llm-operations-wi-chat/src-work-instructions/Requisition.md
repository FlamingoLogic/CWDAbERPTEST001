---
aliases:
  - Purchase Request
  - Procurement Queue
tags:
  - workinstructions
  - tool
  - purchasing
---

# 🏷️ Requisition

*Matt Law | Last Updated: 2025-05-09*

This document defines the **Requisition** window functionality in AbilityERP. It supports internal purchase requests and enables the purchasing team to manage procurement priorities, review open requisitions, and convert them into purchase orders.

---

### 📚 Description

The **Requisition** window in AbilityERP is a procurement communication and control tool. It allows users to request products or services while giving the purchasing team a centralised workflow to review and process requests.

Requisitions can be created:
- Manually by users
- Automatically by the system (e.g., via replenishment)

---

### 🧭 Navigation

- Access via: `Main Menu => Requisition`

---

### 🛠️ Functionality

#### Header Fields

- **Document Type**: Typically set to *Purchase Requisition*.
- **User/Contact**: Person initiating the request (also receives any system notifications).
- **Price List / Priority / Organization / Warehouse**
- **Date Required**: When the goods or services are needed.
- **Document Date**: Entry date for the requisition.
- **Approved**: Optional checkbox used for approval workflows if configured.
- **Total Lines**: Auto-calculated from line items.
- **Document Status / Document Action**: Controls processing status.
- **Master Location** *(custom)*: Optional dimension for reporting/logistics.
- **Vehicle** *(custom)*: Optional field to indicate association with a specific vehicle.

#### Line Tab: Requisition Line

Each line represents an individual item or service being requested.

- **Product** or **Charge**: Either can be used depending on the nature of the request.
- **Quantity**: Required field.
- **UOM**: Unit of measure (e.g., EA, HR, Box).
- **Business Partner**: Optional; can be left blank for purchasing team to complete.
- **Price / Line Amount**: Can be estimated or final.
- **Description**: Useful for free-text requests where product is unknown.
- **Purchase Order Line**: Populated once a PO is generated.

> Note: You can enter only the quantity and a description if you don't know the full product detail — the purchasing team can finalise it.

---

### 📂 Tabs

- **Purchase Orders**: Displays any Purchase Orders linked to this requisition line.

---

### 🎯 Tips

- You do **not** have to use Requisition. It is an **optional** step in the purchasing workflow.  
  Use it when you want purchasing separation, approval logic, or central visibility over requests.
- A Requisition is considered **open** if:
  - The document status is **Completed**, and  
  - Any **line is not yet linked to a Purchase Order Line**
- Use the **Open Requisitions** report to track outstanding requests.
- Use **Priority** to communicate urgency to the purchasing team.
- Requisitions do **not** consider existing stock levels — they are request-driven only.
- You can create lines with minimal input (e.g., just quantity and description); the purchasing team can finalise the details.


---

### 📝 Notes

- Table: `M_Requisition` (header), `M_RequisitionLine` (lines)
- POs are typically generated using the **Create PO from Requisition** process (separate window).
- Common document flow: Requisition → Purchase Order → Material Receipt → Invoice → Payment.

---

### Notes on Open Requisitions

A **requisition line** is considered **open** when:

- It **does not have a linked Purchase Order Line** (i.e. the `Purchase Order Line` field is blank),  
    **and**
    
- The **parent Requisition document has a status of "Completed"**
    

Only lines that meet **both conditions** will appear in open requisition reports or be eligible for purchase order generation via the _Create PO from Requisition_ process.

> ⚠️ Drafted or In Progress requisitions are **not included**, even if their lines are otherwise open.

---

### 🛠️ Related Tools

- [Purchase Order](Purchase-Order.md)
- [Create-PO-from-Requisition](Create-PO-from-Requisition.md)

---
(end of note)
