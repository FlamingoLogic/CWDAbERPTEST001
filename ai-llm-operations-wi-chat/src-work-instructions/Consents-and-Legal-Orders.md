---
aliases:
  - Consents
  - Legal Orders
  - Consent and Legal Documentation
tags:
  - workinstructions
  - tool
  - client
  - compliance
---

# 🏷️ Consents and Legal Orders (Tab)

*Matt Law | Last Updated: 2025-05-07*

This document outlines how to use the **Consents and Legal Orders** tab in AbilityERP.  
This tab is used to capture and track signed consent forms and legal documentation relevant to a support receiver (client / participant).

---

### 📚 Description
The **Consents and Legal Orders** tab allows users to log key consent and legal documents, including authority to share images or personal information, guardianship orders, and related compliance documentation.  
Documents recorded here can be shown as an alert and help ensure all relevant authorisations are in place.

---

### 🧭 Navigation
- Access via: **[Support-Receiver-(BP)](Support-Receiver-(BP).md)** → *Consents and Legal Orders* tab  
- This tab is not accessible as a standalone window.

---

### 🛠️ Functionality

#### Key Fields
- **[Document-Type](Document-Type.md)**: E.g., Consent, Guardianship, Court Order.
- **[Consent-Type](Consent-Type.md)**: Dropdown of common options (e.g., Consent to share images).
- **Order Number**: Optional external reference.
- **Valid From / Valid To**: Define the document’s active period.
- **Review Date**: Internal prompt to review status of document.
- **Is Document Attached? / Executed?**: Record compliance status.
- **Show As Alert**: When set to *Yes*, this document will appear as an alert on the [Support-Receiver-(BP)](Support-Receiver-(BP).md).
- **Document Provided By**: Free text entry for who signed or provided it.
- **Reference Section**:
  - **Document Developer**: Who created or uploaded the record.
  - **Appointed Partner**: If applicable (e.g., appointed guardian or advocate).

---

### 🎯 Tips
- Always set **Review Date** to ensure the document is revalidated before expiry.
- Use **Show As Alert = Yes** for critical consents (e.g., no-photo consents or legal orders).

---

### 📝 Notes
- Table: `AbERP_Consent_Legal`

---
(end of note)
