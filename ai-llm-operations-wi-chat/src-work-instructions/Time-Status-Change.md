---
aliases:
  - Booking Status Update
tags:
  - workinstructions
  - tool
  - process
  - claiming
---

# 🏷️ Time Status Change

*Matt Law | Last Updated: 2025-05-07*

This document defines the Time Status Change process functionality, navigation, tips, and related tools within the organisation’s systems and processes.

---

### 📚 Description

Time Status Change in AbilityERP updates the status of booking lines based on their End Date and Time relative to the current time, enabling further automations like invoicing.

---

### 🧭 Navigation

- Access via: Main menu => Time Status Change window

---

### 🛠️ Functionality

- Select a specific booking using the **Document No** field, or leave blank to process all applicable bookings  
- Set the **Date** field to define the reference date for status updates (defaults to the current date)  
- Check **Is Change Status Lines** to update the status of individual booking lines (e.g., from "Scheduled" to "In Progress" to "Finished")  
- Optionally check **Run as Job** to process the status updates in the background  
- Executes the process to update booking line statuses when the End Date and Time has passed  

---

### 📝 Notes

- Ensure **Is Change Status Lines** is checked to update individual booking lines; otherwise, only the header status may be affected  
- This process would typically be attached to a [Scheduler](Scheduler.md) to run automatically  
- Test the Time Status Change process in a sandbox to confirm its impact on related transactions and automations  

---
(end of note)
