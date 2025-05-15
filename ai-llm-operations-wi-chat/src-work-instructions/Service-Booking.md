---
aliases:
  - Service-Booking
  - Tool-ServiceBooking
  - Core-Booking
tags:
  - abilityerp
  - tool
  - workinstructions
  - claiming
  - client
  - finance
---

# 🏷️ Service Booking

*Matt Law | Last Updated: 2025-05-14*

This document defines the **Service Booking** functionality in AbilityERP, including both current behaviour and confirmed upcoming enhancements. Service Bookings are central to managing scheduled supports and controlling the validation-to-claiming process for NDIS services. Service booking is on the same table as Sales Order `C_Order` and much of the content in [Sales-Order](Sales-Order.md) is relevant.

---

### 📚 Description

The **Service Booking** tool allows scheduling, quoting, validating, and tracking of planned services for each Support Receiver. It plays a key role in transitioning from plan to delivery, compliance, and eventual claiming.

---

### 🧭 Navigation

- Access via: **Main Menu → Service Booking**

---

### 🛠️ Functionality

#### ✅ Current Behaviour

- Opens filtered to show in-progress and completed bookings from the past 24 hours.
- Supports three Target [Document-Type](Document-Type.md)s:
  - **Service Booking - Standard** → Active booking
  - **Service Booking - Binding Offer** → Quote (binding)
  - **Service Booking - Non-Binding Offer** → Quote (non-binding)
- Quotes can be converted:
  - Either by changing Target Document Type (not recommended — loses history)
  - Or by using the **Quote Convert** process (recommended)

##### ⏱️ Date Fields

- **Date Ordered**: Sets pricing based on price list version; should reflect the intended price date.
- **Date Promised**: Typically set to match the last booking line's end date. Not used in bookings/services often. It is typically used as a parameter in the generation of shipments from sales orders. 

##### 🧮 Quantity Handling

- **Use Time-Based Quantity**:
  - When ticked, calculates quantity based on Start and End time.
  - When unticked, allows manual entry of quantity.
- **Use Day and Week Multiplier**:
  - For quotes/price estimates ("Binding Offer" or "Non-Binding Offer"), when not using the booking generator, use "Day and Week Multiplier" to calculate amounts based on the number of days and weeks.

##### 🔁 Time Status

- Booking line **Time Status** updates using [Time-Status-Change](Time-Status-Change.md) process. This process can be scheduled. 
  - Moves lines from *Scheduled* to *Finished* after End Date/Time passes.

##### 📦 Product Related Fields

- **UPC/EAN**: This field represents the **NDIS Support Item Code** (also referred to as **UPC** — Unique Product Code). It should be populated to align bookings to NDIS product rules and exports.
- **[Claim-Type](Claim-Type.md)**: Optional field providing additional detail on the type of claim (e.g. *Cancellation*}. Must be used for NDIS claims where relevant. 

##### 🧹 Reserved Quantity Removal (Critical Behaviour)

- To delete a **whole booking**:
  - Reactivate → change Target Doc Type to *Non-Binding Offer* → Delete.
- To delete **individual lines**:
  - Set **Quantity = 0** and leave it unchanged.

---

#### 🆕 Upcoming Enhancements *(Ticketed)*

> 📌 From: **Service-Booking-Line-Enhancements**  
> Planned: May–June 2025 release

##### 📋 New Fields — Booking Line Level

| Field | Purpose |
|-------|---------|
| **Validated** | Flags that post-delivery checks (e.g. shift/timesheet) have passed. |
| **Manual Hold** | Prevents claiming even if the line is otherwise valid. |
| **Not Delivered** | Used for Program of Support no-shows. |
| **Ready to Claim** | Final flag for invoice/export eligibility. |
| **Start Day** | Derived from Start Date (read-only); used for reporting or validation. |
| **End Day** | Derived from End Date (read-only); used for reporting or validation. |

**Line Placement Summary**:
- **Validated**, **Manual Hold**, **Ready to Claim** → in **Status** section
- **Not Delivered** → under **Quantities**
- **Start/End Day** → to the right of **Start Date / End Date** in **Quantities**

> Note: Start/End Day mirrors layout from the Rostered Shift window.

---

##### 📋 New Field — Booking Header Level

| Field | Purpose |
|-------|---------|
| **Ready to Claim Rule** | Controls how and when `Ready to Claim` is auto-ticked. |

**Dropdown Options**:
- **Auto on Time Finish**
- **Manual Tick**
- **Auto when Finished + Validated**

**Header Placement**:
- After **Target Document Type**

---

##### 🛠️ Fixes Included

- Copying a line now correctly copies Quantity.
- Updating time will no longer clear Quantity if **Use Time-Based Quantity** is unticked.

---

### 🎯 Tips

- Always check **Date Ordered** for correct pricing.
- Use **Quote Convert** to retain quote linkage when converting.
- For quoting: use Day/Week Multiplier for quick estimates.
- Leave *Use Time-Based Quantity* unticked for manual workflows.
- Start Day / End Day fields support logic for reporting, rostering, and claiming.
- Manual Hold is useful for compliance checks but will block invoice generation if flagged and configured that way.
- Set Claim Type on lines requiring cancellation, transport, or other special claiming logic for NDIS.

---

### 📝 Notes

- Use **Prepare** status to reserve without completing.
- **Void** reverses all transactions — use with caution.
- A booking can be reactivated post-completion if amendment is needed.
- [Generate-Invoices](Generate-Invoices.md) process will be enhanced to respect **Ready to Claim** and **Manual Hold** flags on the booking line.
- NDIS product code = UPC/EAN = Required for most exports.

---

### 🚀 Optional Enhancements (Coming Soon)

- Compare bookings against shift-based [Allocation-Records](Allocation-Records.md)
- Use [Advanced-Search-Orders](Advanced-Search-Orders.md) for validation exception reports
- Queue-based workflows for auto-checking claim readiness
- Configurable Ready to Claim Rule logic in [Booking-Generator](Booking-Generator.md) outputs

---
(end of note)
