---
aliases:
  - Request Type
tags:
  - workinstructions
  - tool
  - request
  - automation
  - efficiency
  - lookup
---

# 🏷️ Request Type

*Matt Law | Last Updated: 2025-05-01*

The **Request Type** tool in AbilityERP defines the behaviour, categorisation, and access control for different kinds of requests—such as approvals, actions, or compliance checks. Each type links to a set of statuses and access roles, forming the foundation of your organisation’s request workflow system.

---

## 📚 Description

Request Types control how requests behave, who can access them, and what their lifecycle looks like. They are tightly linked to [Request-Status](Request-Status.md) sets and support layered configuration for categories, roles, windows, and notifications.

---

## 🧭 Navigation

- Access via: **Main menu => Request Type** window

---

## 🛠️ Functionality

### 🔹 Header Configuration

- **Name**: Label for the type (e.g., Action, Approval)
- **Request Status**: Links to a [Request-Status](Request-Status.md) category that defines the lifecycle
- **Confidentiality**: Internal (default) or external-facing for portal usage (e.g., Partner Confidential)
- **Behaviour Flags**:
  - Email When Due
  - Is Service Agreement
  - Is Rostered Shift
  - Other context-specific flags to restrict use to a specific window
- **Update Notification**: Add users to receive email alerts if email notifications are enabled

### 🔹 Tabs

- **Category Link Tab**: Adds allowable [Request-Category](Request-Category.md) entries for this type
- **Role Access Tab**: Controls who can create or interact with requests of this type

---

## 🎯 Tips

- Start with broad types like “Action” and “Approval”; grow as specific workflows emerge
- Always assign a [Request-Status](Request-Status.md) to structure the request lifecycle
- Use **“Is...”** flags (e.g., Is Service Agreement) to bind request types to relevant windows
- Keep Confidentiality as “Internal” unless using portals or integrations
- Test email alerts in sandbox before enabling live notifications

---

## ⚠️ Notes

- Role Access tab ensures request security and segregation of duties
- The Request Type + Status + Category structure underpins automation, workflows, and reporting
- It is common to create a [Linked-Tables](Linked-Tables.md) relationship between **Request Type** and [Request-Resolution](Request-Resolution.md) to control allowed outcomes

---
(end of note)
