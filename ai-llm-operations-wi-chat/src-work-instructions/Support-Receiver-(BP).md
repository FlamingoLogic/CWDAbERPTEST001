---
aliases:
  - Support Receiver
  - Client Record
  - Participant
tags:
  - workinstructions
  - tool
  - client
---

# 🏷️ Support Receiver (BP)

*Matt Law | Last Updated: 2025-05-07*

This document outlines how to use the **Support Receiver** window in AbilityERP — the central record for managing NDIS clients / participants / support receivers.  
It extends the core `C_BPartner` table and includes demographic, funding, disability, consent, alert, and relational data essential for service delivery and compliance.

---

### 📚 Description
The **Support Receiver (BP)** window is the primary location for entering and maintaining participant information. It feeds into related tools like Service Agreements, Service Bookings, Invoicing, and Reporting.  
This window consolidates identifying data, alerts, funding details, and cultural or disability information.

---

### 🧭 Navigation
- Access via: **Main Menu** → **Support Receiver (BP)**
- Or: Zoom from related records.

---

### 🛠️ Functionality

#### Core Header Fields
- **Name / Preferred Name / Status**: Core identifiers used across the system.
- **Risk Alerts & Consent Alerts**: Displayed in red for critical context. See [[Alerts-Support-Receiver-and-Employee|Alerts-SR]]
- **Demographics**: Includes DOB, Gender, Cultural Affiliation, Disability, ATSI status, and LGBTQIA+ (optional).
- **Funding & Services**: Key funding body, number, transition dates, and services being delivered.
- **Contact Info**: Email, phone, address (via linked Partner Location).
- **Living Arrangements & Decision-Making**: For planning and safeguarding.
- **Status** uses [[Request-Status]]. 

#### Key Tabs (each with separate tool docs)
- **Alerts** – Shows risk and consent alerts. See [Alerts-Support-Receiver-and-Employee](Alerts-Support-Receiver-and-Employee.md).
- **Activity** – Track interactions and updates. See [Activity Viewer](activity-viewer.md).
- **BP Associations** – View or add partner relations. See [BP-Association](BP-Association.md).
- **Locations** – Track multiple addresses. See [Locations-Tab](Locations-Tab.md).
- **Requests** – Create and view requests for action or approval. See [Request](request.md).
- **Restrictive Practices** – Record restrictive practices for NDIS compliance. See [Restrictive Practices](restrictive-practices.md).
- **Consents and Legal Orders** – Manage legal and consent documentation. See [Consents and Legal Orders](Consents-and-Legal-Orders.md).
- **Plan & Assessment** – Manage service plan and assessments. See [DRAFT)-Plan-&-Assessment]((DRAFT)Plan-&-Assessment.md).
- **Rostering Needs** – Define rostering criteria. See [Rostering-Needs](Rostering-Needs.md).

---

### 🎯 Tips
- Keep alerts and consent up-to-date.
- Only use “Active receiving support” when the client is engaged in current services.
- Use clear Search Key prefixes for quick lookup (e.g., “Bern” for Bernadette).
- Use 'Zoom across' toolbar option to access Service Agreements and other critical tools directly.

---

### 📝 Notes
- This window uses the standard `C_BPartner` table with additional logic and fields tailored for disability support.
- Records here link to all client-facing modules. 


---
(end of note)
