---
aliases:
  - Skip Dates
  - Booking Generator Skip List
tags:
  - workinstructions
  - tool
  - lookup
---

# 🏷️ Skip Dates

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the Skip Dates window — used to define specific dates where bookings should not be generated. It is used exclusively within the Service Booking Generator to exclude public holidays, shutdown periods, or unavailable service days.

---

## 📚 Description  
The **Skip Dates** window is used to maintain named lists of date ranges that should be skipped during automated booking generation. These lists are selected in the [Service Booking Generator](Booking-Generator.md) to prevent bookings from being created on days when services are not expected to run.

---

## 🧭 Navigation  
- Access via: Main menu => Skip Dates

---

## 🛠️ Functionality  

### 🧾 Header (Skip Dates Record)  
- **Client / Organisation**: Standard context fields  
- **Name**: A descriptive label for the group of skip dates (e.g. “Day Options” or “Public Holidays – 2025”)  
- **Description** (optional): Additional context for internal use  
- **Active**: Tick to ensure the record is available for use in the Booking Generator

### 📅 Dates Tab  
- Create one or more date ranges to be skipped  
- Each row includes:
  - **Start Date and time** and **End Date and time**
  - Optional **Description** for that date range (e.g., “Christmas Shutdown”)
  - **Skip Dates** (auto-linked to header)
  - **Active** flag  
- **Any overlap** between a booking line and a skip date range will cause that line to be excluded from generation.

---

## 🎯 Tips  
- Use descriptive names (e.g., “SIL Christmas 2024”) to clearly link skip lists to relevant programs or clients.  
- Always double-check date ranges for accuracy before generating bookings.  
- Inactive skip dates or inactive date rows will not be applied.  
- Skip Dates only *exclude* booking lines — they do not adjust existing bookings.  
- Maintain separate lists for different programs if their shutdown periods vary.  
- Even partial overlap (e.g. one day in a multi-day booking) will result in the **entire booking line being skipped**.

---

## 🛠️ Related Tools  
- [Service Booking Generator](Booking-Generator.md)

---
(end of note)
