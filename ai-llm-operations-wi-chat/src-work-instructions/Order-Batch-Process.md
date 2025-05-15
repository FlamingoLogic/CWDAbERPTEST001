---
aliases:
  - Order Batch
  - Bulk Order Processing
tags:
  - workinstructions
  - tool
  - automation
  - efficiency
  - claiming
---

# 🏷️ Order Batch Process

*Matt Law | Last Updated: 2025-05-13*

This document outlines how to use the Order Batch Process — used to process multiple Orders and Service Bookings in bulk using selected filters and document actions.

---

## 📚 Description  
The Order Batch Process in iDempiere/AbilityERP enables users to process multiple Orders and Service Bookings in bulk, applying selected document actions and filters to manage their statuses efficiently.  
In AbilityERP it includes expanded filtering by Price List, Activity, and Master Location for more targeted processing.

---

## 🧭 Navigation  
- Access via: AbilityERP → **Order Batch Process**

---

## 🛠️ Functionality  
- Processes Orders and Service Bookings in bulk based on selected criteria.

### 🔍 Filters  
- **Target Document Type**: Selects the type of document to process (e.g., Standard Order, Service Booking – Standard).  
- **Document Status**: Filters Orders and Service Bookings by current status (e.g., Draft, In Progress, Completed).  
- **Business Partner**: Filters by a specific Business Partner (Client).  
- **Self-Service**: Option to include/exclude self-service bookings.  
- **Delivered**: Filters by delivery status.  
- **Invoiced**: Filters by invoicing status.  
- **Date Ordered**: Filters by order date range.  
- **Price List**: Filters based on the Price List used in the Order or Booking (new).  
- **Activity**: Filters based on the Activity field on the header (new).  
- **Master Location**: Filters by the Master Location (aka Contract Location) used on the header (new).

> 💡 Activity and Master Location filters are only applied to the **header** of the Order/Booking — line-level data is not used.

### ⚙️ Actions  
- **Document Action**: Applies a selected system action (e.g., Complete, Prepare, Reactivate) to all matching documents.  
- **Run as Job**: Optionally processes in the background (useful for large batches).

---

## 🎯 Tips  
- Always validate with a limited data set in a test environment first.  
- Combine filters like Price List and Document Status for precise bulk updates.  
- Master Location is labelled as “Contract Location” on Service Bookings — both refer to the same reference.  
- Check [Sales Order](Sales-Order.md) and [Service Booking](Service-Booking.md) docs for reference on document actions and statuses.

---
(end of note)
