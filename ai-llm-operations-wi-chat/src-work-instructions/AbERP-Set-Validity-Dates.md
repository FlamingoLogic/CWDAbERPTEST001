---
aliases:
  - Set Validity Dates
  - Validity Date Update
tags:
  - workinstructions
  - tool
  - process
  - client
  - compliance
---

# 🏷️ Set Validity Dates Process

*Matt Law | Last Updated: 2025-05-07*

This document explains how to run the **Set Validity Dates for Goals, Restrictive Practices, Plan & Assessment** process.  
The process updates the `Valid` checkbox on several key records by comparing the current date to their configured **Start** and **End Dates**.

---

### 📚 Description
This process checks whether each record is currently valid (i.e., today falls within its start and end dates) and updates the `Valid` field accordingly.  
It applies to:

- **[(Draft)Goals]((Draft)Goals.md)**
- **[Restrictive-Practices](Restrictive-Practices.md)**
- **[(DRAFT)Plan-&-Assessment]((DRAFT)Plan-&-Assessment.md)**

This is typically run as a **scheduled job** [Scheduler](Scheduler.md) to keep all validity statuses current.

---

### 🧭 Navigation
- Access via: **Main Menu** → **"AbERP Set Validity Dates"**

---

### 🛠️ Functionality
- **Run as Job**: Tick if scheduling for background execution.
- Click **OK** to run the process.

---

### 🎯 Tips
- Best practice: schedule this to run nightly.
- If validity appears out of sync, re-run this process manually to troubleshoot.

---

### 📝 Notes
- This process updates the `Valid` flag based on **Start Date** and **End Date** for each record type.
- No parameters or filters — it checks all applicable records in the system.

---
(end of note)