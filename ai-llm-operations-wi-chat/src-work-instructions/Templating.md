---
aliases:
  - Templating
  - Template Documents
tags:
  - workinstructions
  - tool
  - automation
  - configuration
  - efficiency
---

# 🏷️ Templating

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use Templating in AbilityERP — a configuration approach that enables efficient creation and reuse of templates for various transaction types, supporting automation, consistency, and data accessibility.

---

## 📚 Description  
Templating is a common configuration to enable efficient creation and management of templates for orders, invoices, requests, and other transaction documents, enhancing automation, consistency, and data accessibility. Templates can be used extensively and isolated in dedicated windows to prevent accidental updates within the core windows.

---

## 🛠️ Functionality  
- Create and manage templates for transaction documents (e.g., AP Invoice Template, Sales Order Template, Request templates).
- Copy templates via a process triggered by a button, scheduler or other event.
- Can also extend doc action process to perform a specific action on a specific user created [Target-Document-Type](Target-Document-Type.md).
- You don’t need to use templates when you simply want to repeat a standard order, invoice, journal, or payment — [Recurring](Recurring.md) is all you need for that. Templates are better suited for cases where extra functionality is required, like managing a subscription, beyond just a basic invoice.

---

## 🗂️ Field Details  
- **Doc Action Records**: Specify a specific template doc type for transactions (e.g., "AP Invoice Template") to identify templates and set behavior.  
- **Non Doc Action Records**: Create an *isTemplate* tickbox field to identify templates.  
- **Template Data**: Store predefined fields (e.g., order lines, invoice amounts, request details) for reuse.  
- **Trigger Event**: Attach copy processes to buttons, schedulers or extend doc action for automation.  
- Create a specific [Target-Document-Type](Target-Document-Type.md) for a template. You can also add fields to this window / table — for example, what the [Target-Document-Type](Target-Document-Type.md) should be once the template is used/copied. Then the document action process can be extended to switch the target doc type on the template to the one required on the actual transaction.

---

## 🎯 Tips  
- Do not allow templates to appear in standard windows (e.g., AP Invoice, Sales Order) to prevent errors — use dedicated Templating Tools windows.  
- Use document type (e.g., "AP Invoice Template") to mark templates, restricting completion via role access (no role permitted to complete template doc types).  
- Trigger template copying via a button (e.g., "Copy Template") or [Scheduler](Scheduler.md) for automated workflows.  
- Generally it is best practice to use the [request template plugin](Request-Template-Plugin.md).

---
(end of note)
