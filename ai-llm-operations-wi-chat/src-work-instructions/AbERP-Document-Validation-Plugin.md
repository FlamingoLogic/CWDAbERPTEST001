---
aliases:
  - Document Validation Plugin
  - AbERP Validation
tags:
  - workinstructions
  - tool
  - validation
  - compliance
  - plugin
---

# 🏷️ AbERP-Document-Validation Plugin

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the AbERP Document Validation Plugin — a configurable code-based validation system that enforces business rules, prevents unapproved changes, and supports quality control workflows across AbilityERP.

---

## 📚 Description  
The AbERP Validation Plugin enables configurable, code-driven validation of records in AbilityERP. It supports multi-level messaging (`Info`, `Warn`, `Fail`), enforces business logic via test scripts, and records outcomes through a dedicated Document Validation window and subtab. It is used to prevent unapproved changes, prompt corrective actions, or signal key information before a document progresses.

---

## 🧭 Navigation  
- Access via: Main menu => AbERP Document Validation window  
- Also appears as: **Validation** tab on windows where plugin is enabled (e.g., Order, Invoice, Shift)  
- Triggered by: Validate button on the window, document action, or scheduled callout

---

## 🛠️ Functionality  
- Executes one or more validation tests written in code (typically Java)  
- Tied to specific tables and optionally triggered by:
  - Document actions  
  - Validate buttons  
  - Scheduled processes (e.g. nightly callout)  

- Creates:
  - A **Document Validation** header record logging overall status
  - One or more **Validation Line** records, each representing a triggered test

### 🎛️ Validation Result Mechanics  
- Each line shows the result of an individual validation test  
- Levels include:
  - **Info**: Informational only
  - **Warn**: May be overridden with approval
  - **Fail**: Prevents document progression unless resolved or overridden

- Validation behavior:
  - **Fail present**: Cannot approve
  - **Only Warns/Infos**: May be approved via `Validation Approved` checkbox
  - **Only Infos**: Auto-passes validation

- Validation is approved at the **header level**  
- **Validation Notes** format:
  - `Level 0 line 0` — Header-level message  
  - `^^ Level 1 [Tab Name] line [#]` — Line-level message (e.g., Sales Order Line 10)

---

## 🎯 Tips  
- Add the `Validation` tab to all windows where this plugin is active  
- Track all implemented tests in the [Validation-Tests](Validation-Tests.md) informational window  
- Ensure `Validate` button is visible if no document action is available  
- Use these fields:
  - `Validated` checkbox: read-only status indicator
  - `Validation Fail` checkbox: blocks workflow if validation fails
  - `Validation Override` checkbox: authorises bypassing failure (only for exceptional cases)  
- Pair with the **Requests** module when approvals are required for `Warn` level outcomes  
- Re-run validations on change or nightly to maintain system integrity

---

## 🧠 Quality Integration  
This plugin supports structural quality control:

- Each validation test can trace back to a real issue or improvement (e.g., CAR/PAR)
- Examples:
  - A **Corrective Action Request (CAR)** may trigger a new validation test for bank account change approval
  - A **Preventative Action Request (PAR)** may result in a reminder or warning if safety rules are at risk

This ensures validation is both **auditable** and **preventative**, enhancing quality assurance for internal use and external audits.

---

## 📝 Ticket Template – Request a New Validation Test

```markdown
### Validation Test Request

- **Window**: [e.g., Business Partner]
- **Table**: [e.g., C_BPartner]
- **Does the window already have validation?**: [Yes/No]
- **Does the table already have validation?**: [Yes/No + explain if needed]
- **Test Name**: [e.g., Bank Account Change]
- **Purpose**: [e.g., Detect if bank account changes were not approved]
- **Validation Trigger**: [Validate button / Document Action (specify) / Scheduled callout]
- **Validation Level**: [Info / Warn / Fail]
- **Validation Logic**:
  - [Plain English description of the rule]
  - [What tables/fields need to be checked]
- **Expected Output (Validation Notes)**:
  - [e.g., Level 0 line 0 – Bank account change not approved. (Fail)]
