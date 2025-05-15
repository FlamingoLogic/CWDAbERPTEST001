---
aliases:
  - Scheduler
  - Scheduled Process Runner
tags:
  - workinstructions
  - tool
  - automation
  - reporting
  - efficiency
---

# 🏷️ Scheduler

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the Scheduler in AbilityERP — used to automate execution of processes and reports based on defined timing and parameter rules.

---

## 📚 Description  
The Scheduler tool in AbilityERP automates the execution of processes and reports, using default parameters, variables, and scheduling options to enhance efficiency and consistency.

---

## 🧭 Navigation  
- Access via: AbilityERP => Scheduler window.

---

## 🛠️ Functionality  
- Schedule any process or report to run with default parameters, including variables (e.g., `@#Date@`).
- Set up header details, then configure parameters via the process icon, mirroring manual process execution.
- Add variables at the line level for flexible parameter defaults.
- Define schedules (e.g., daily, weekly) or use custom "Cron Scheduling Patterns".
- Configure email or notice notifications for users, including report attachments. Notices are good for requiring acknowledgement.
- You can use Document Status Indicators (DSIs) to track different notices.

---

## 🎯 Tips  
- Use the process icon in the header to set up parameters as they appear in manual runs, then save as lines.
- Add variables like `@#Date@` at the line level for dynamic scheduling (e.g., monthly reports).
- Configure a mail template and recipients for notifications, ensuring the supervisor’s email is set for sending.
- Access advanced schedule options under System => Schedule to add custom frequencies.

---

## 🛠️ Related Tools  
- [Recurring Run](Recurring-Run.md)

---
(end of note)
