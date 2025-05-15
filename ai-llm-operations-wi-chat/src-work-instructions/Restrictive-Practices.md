---
aliases:
  - Restrictive Practices
  - Behaviour Support Tab
tags:
  - workinstructions
  - tool
  - compliance
  - client
---

# 🏷️ Restrictive Practices Tab (Support Receiver)

*Matt Law | Last Updated: 2025-05-07*

This document outlines how to use the **Restrictive Practices** tab within the **[Support-Receiver-(BP)](Support-Receiver-(BP).md)** window in AbilityERP.  
This tab is used to document approved restrictive practices for NDIS participants, including behaviour support medications, physical restraints, and other restrictive strategies. It helps ensure compliance with NDIS reporting and audit standards.

---

### 📚 Description
The **Restrictive Practices** tab allows providers to log restrictive practices in place for a participant, the reason for their use, associated medications or strategies, and linked assessments or behaviour support plans.  
This tab is only accessible under the Support Receiver (BP) window and stores data in the `AbERP_Restrictive_Practices` table.

---

### 🧭 Navigation
- Access via: **Support Receiver (BP)** → *Restrictive Practices* tab
- This tab is **not** accessible as a standalone window.

---

### 🛠️ Functionality

#### Key Fields
- **[Restrictive-Practice-Type](Restrictive-Practice-Type.md)**: Choose from options such as Chemical, Environmental, Physical, etc.
- **Start Date / End Date**: Defines the active date range of the practice.
- **Valid**: Auto-checked based on start/end dates *after* running the [AbERP-Set-Validity-Dates](AbERP-Set-Validity-Dates.md) process (usually scheduled [[Scheduler]]).
- **Frequency**: How often the practice is reviewed (e.g., Routine, PRN).
- **Reason for Restrictive Practice**: Required justification linked to the behaviour of concern.
- **Medication**: If applicable, link to the prescribed medication record. [Medication](Medication.md)
- **Plan to Eliminate Practice**: Strategy for phasing out or reducing restriction.

#### Linked Compliance Fields
- **Risk Assessment**: Indicates whether a supporting risk assessment is completed.
- **Consent & Authorisation**: Records who provided consent, whether it’s attached, and authorisation status and date.
- **References**: Link to Behaviour Support Plan and Risk Assessment IDs. [(DRAFT)Plan-&-Assessment]((DRAFT)Plan-&-Assessment.md)
- **Contract Location** [(Draft)-Master-Location]((Draft)-Master-Location.md): Site where the practice is carried out.

---

### 🎯 Tips
- Ensure **Start Date** and **End Date** are set correctly and that the validity process runs regularly.
- Use clear, audit-ready language when describing the behaviour, rationale, and plan to reduce restrictions.
- Check that consent evidence and assessments are documented and accessible.

---

### 📝 Notes
- The “Valid” checkbox does not update in real-time — run the **AbERP Set Validity Dates** process to refresh it.
- This data may be reviewed during NDIA audits and should be kept current and evidence-based.

---
(end of note)
