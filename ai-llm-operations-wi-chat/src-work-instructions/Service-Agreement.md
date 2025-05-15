---
aliases:
  - Service Agreement
  - NDIS Contract
tags:
  - workinstructions
  - tool
  - client
  - compliance
---

# 🏷️ Service Agreement Window

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the Service Agreement window — used to manage NDIS service agreements, support financial tracking, and ensure alignment with participant funding terms.

---

## 📚 Description  
The Service Agreement window manages service agreements for NDIS disability service providers, built on the C_Project table in AbilityERP. It acts as a project, allowing agreements to be referenced in transactions and posted to the general ledger with the project dimension for financial reporting by agreement. Users can track statuses and manage service agreement lines with agreed amounts and service details.

---

## 🧭 Navigation  
- Access via: Main menu => Service Agreement window

---

## 🛠️ Functionality  
- **Core Features**: Create and manage service agreements with details like name, term (fixed or ongoing), and status (linked to [[Request-Status]]).
- **Attachment**: Attach a wet signed agreement as a digital file to the service agreement record.
- **Status Management**: Uses Request-Status (see [[Request-Status]]) with core functionality. Request Status controls the "Processed" tickbox, which triggers built-in behavior like making certain fields non-editable.
- **Agreement Options**: Tickboxes show if claiming is allowed for non-face-to-face supports, high-intensity supports, and short-term cancellations if agreed with the client.

### 📑 Service Agreement Line Tab  
- Define lines with agreed amounts, descriptions, product categories, funding types (e.g., NDIS - National Disability Insurance Scheme), and funding management types (e.g., Portal Managed).
- Supports reporting of bookings and invoiced amounts against service agreement lines.
- Quick Info sidebar displays real-time calculations (e.g., service agreement line planned price vs. invoiced amounts) when opened.

### 📆 Activities and Dashlets  
- Refer to: [Activities-and-Dashlets](Activities-and-Dashlets.md)
- Set up on Finish Date or Review Date to flag agreements needing renewal.
- Leave Review Date blank or tick "Expiry Action" to exclude from DSI if no renewal is needed.

### 📊 Financial Reporting  
- Service agreements can be referenced on transactions (e.g., invoices).
- Since the project is an accounting dimension, it posts to the general ledger, enabling financial reporting by service agreement.

---

## 🎯 Tips  
- Ensure the Review Date is set for agreements needing renewal to avoid missing DSI notifications.
- This window makes good use of **[[Quick-Info]]** — open it to view additional participant details alongside the agreement.

---

## 📝 Notes  
- Users need appropriate role-based access to update Request Status options.

---
(end of note)
