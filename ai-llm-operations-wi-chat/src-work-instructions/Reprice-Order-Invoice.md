---
aliases:
  - Reprice
  - Price Update Process
tags:
  - workinstructions
  - tool
  - efficiency
  - claiming
---

# 🏷️ Reprice Order/Invoice Process

*Matt Law | Last Updated: 2025-05-13*

This document outlines how to use the **Reprice Order/Invoice Process** in AbilityERP — including both individual record repricing and the new **bulk update** capability for draft/in-progress orders and service bookings.

---

## 📚 Description  
This tool updates order or invoice line prices based on the latest applicable **Price List Version** (matched against the Date Ordered). It ensures accurate pricing when price list changes occur after draft or in-progress documents are created.

The process now also supports **bulk repricing** of all applicable Orders/Bookings (not invoices) by selecting a **Price List** and **Target Document Type**.

---

## 🧭 Navigation  
- Access via: **AbilityERP** → **Reprice Order/Invoice**

---

## 🛠️ Functionality  

### 🔄 Individual Reprice  
- Select either:
  - **Order** – to reprice a single Order or Service Booking, **or**
  - **Invoice** – to reprice a single Invoice  
- Reprices line items using the Price List Version valid at the **Date Ordered**.  
- Only works for **Draft** or **In Progress** records.

### 🧾 Bulk Reprice  
- Leave **Order** and **Invoice** fields blank.  
- Select:
  - **Order Price List** (mandatory)
  - **Order Target Document Type** (optional but recommended)
- Reprices **all Draft / In Progress orders and bookings** that match selected criteria.

> ⚠️ **Caution**: The bulk update will update all **Draft / In Progress Orders** for the Price List and Document Type selected.  
> It does **not** update invoices. Ensure you've checked affected records.

---

## 🎯 Tips  
- For Service Bookings, treat them the same as orders — they are included in this process.
- To reprice completed records, **reactivate them first** using the [Order Batch Process](Order-Batch-Process.md).
- Use a **sandbox** to test before running on production.
- Use reporting tools (views or saved filters) to pre-identify what will be affected by a bulk reprice.

---
(end of note)
