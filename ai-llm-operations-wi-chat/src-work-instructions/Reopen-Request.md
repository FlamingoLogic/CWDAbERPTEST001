---
aliases:
  - Reopen Closed Request
  - Request Reopen Tool
tags:
  - workinstructions
  - tool
  - request
  - process
---

# 🏷️ Reopen Request

*Matt Law | Last Updated: 2025-05-01*

The **Reopen Request** tool in AbilityERP allows users to reopen a previously closed [Request](Request.md) record for further editing, processing, or reassignment.

---

## 📚 Description

This tool is used when a request has been marked as closed but needs to be amended or reprocessed. Reopening restores the request to an editable state and resumes workflow actions.

---

## 🧭 Navigation

- Access via: Main menu => **Reopen Request** window

---

## 🛠️ Functionality

- Select the closed request using the **Request** field.
- Optionally tick **Run as Job** to process in the background (asynchronous execution).
- Executes the process to:
  - Change the request status from closed to active
  - Allow amendments or further workflow steps

---

## ⚠️ Notes

- The request **must be in a closed state** (as per its [Request-Status](Request-Status.md)) to be eligible for reopening.
- Consider whether reopening impacts downstream reporting or compliance tracking—use audit notes if needed.

---
(end of note)
