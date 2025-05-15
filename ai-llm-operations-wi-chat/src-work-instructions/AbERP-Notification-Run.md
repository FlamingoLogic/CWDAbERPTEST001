---
aliases: 
tags:
  - workinstructions
  - tool
  - plugin
  - claiming
  - purchasing
---

# 🏷️ AbERP Notification Run

*Flamingo Logic | Last Updated: 2025-05-08*

This document defines the Notification Run Tool (NRT) plugin's functionality, setup, tips, and related tools for bulk communications in AbilityERP.

---

### 📚 Description
The Notification Run Tool simplifies stakeholder communication by enabling bulk delivery of emails (or optionally print) with personalised attachments and dynamic content pulled directly from AbilityERP.

It supports use cases like invoice delivery, vendor remittances, payment notifications, and general announcements — all using real-time data, with logged output in the document management system (DMS).

---

### 🧭 Navigation
- Access via: Main Menu → **AbERP Notification Run**
- Related process windows include:
  - `Run Notification Header` (to send communications)
  - `Invoice Notification Run Line` (for customer invoices)
  - `Payment Selection Notification Run Line` (for vendor payments)

---

### 🛠️ Functionality

#### Header Setup
- Create a new record in the **AbERP Notification Run** window.
- Select:
  - Info Window (must have “Show in Notification Run” = ✅)
  - Mail Template (tokens allowed)
  - Print Format (used as default if none defined at line level)

#### Step 1 – Create Notification Lines
- Click **“Create From”**:
  - Opens the linked Info Window in a popup.
  - Filter and select records (e.g., unpaid invoices).
  - Records populate the **Notification Line** tab.

#### Step 2 – Review & Send
- Optionally set line-level print format.
- Mark the header record as **Approved** (required to enable send).
- Click **“Run Notification Header”** to:
  - Email records if Notification Type = Email
  - Print and consolidate into a single PDF if Notification Type = Print
  - Attach outputs to the DMS and Notification Run record

---

### 🎯 Tips
- **Business Partner Setup** must include:
  - Notification Type = Email or Print
  - Valid contact marked as **Invoice Contact = Y**
  - “Send Email” = Y
- Print formats must match the document type and be tested
- Test with a small sample first (e.g. 1–2 BPs)
- BCC users can be configured using the **Notification BCC** field

---

### 📝 Notes
- Plugins required:
  - `com.logilite.crm.notification`
  - `com.logilite.template.velocity`
  - DMS plugin suite
- Info windows must:
  - Be marked as “Show in Notification Run”
  - Include a custom process (e.g. `InvoiceNotificationRun`)
- Predefined attachments (e.g. terms & conditions) can be uploaded in **DMS Explorer** with content type: `Notification Email Attachment`

---

### 🚀 Enhancements
- Optional development by Flamingo Logic:
  - SMS delivery integration
  - Auto-run via scheduler
---
(end of note)
