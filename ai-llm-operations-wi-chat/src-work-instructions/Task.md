---
aliases:
  - Task Function
tags:
  - tool
  - sysadmin
  - automation
  - efficiency
---

# 🛠️ Tool: Task Function

*Adam Sawtell | Last Updated: 2025-05-01*

Automates background jobs in iDempiere, including Java processes, SQL scripts, and server-side shell scripts. Used for recurring actions such as integrations, report generation, data updates, and maintenance.

---

## 📚 Description  
The Task Function tool enables background automation of both internal and external actions within iDempiere/AbilityERP, supporting Java classes, SQL scripts, and external server commands (e.g., `.sh`, `.py`).

---

## 🧭 Navigation  
- **Menu**: `System Admin => General Rules => Security & Rules => Task`

---

## ⚙️ Functionality  
- Executes Java processes or class-based tasks.  
- Runs custom SQL logic directly against the database.  
- Triggers external scripts hosted on the application server.  
- Works in conjunction with the [Scheduler](Scheduler.md) window to define timing and frequency.  
- Execution results are logged in the **Scheduler Log** window.

---

## 💡 Tips  
- Use class `ScriptTask` to trigger server-side scripts like Bash or Python.  
- Ensure external scripts are executable (e.g., `chmod +x yourscript.sh`).  
- Test each job in a development environment before deployment.  
- Check Scheduler Logs after each execution to verify success or capture errors.  
- Use clear task names and descriptions for long-term maintenance clarity.

---

## 📝 Notes  
- Tasks are commonly used for:  
  - Nightly integration routines  
  - Scheduled report generation  
  - Daily cleanup or recalculation jobs  
- Each task is linked to a schedule and can be enabled/disabled independently.

---
