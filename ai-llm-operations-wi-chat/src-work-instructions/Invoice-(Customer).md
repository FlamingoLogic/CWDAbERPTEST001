---
aliases:
  - Customer Invoice
  - Sales Invoice
tags:
  - workinstructions
  - tool
  - finance
  - claiming
---

# 🏷️ Invoice (Customer) Window

*Matt Law | Last Updated: 2025-05-07*

This document defines the Invoice (Customer) window functionality, navigation, tips, and related tools within the organisation’s systems and processes.

---

### 📚 Description

The Invoice (Customer) window in AbilityERP manages customer invoices. It allows users to create and track invoices, including header details and line items, with options to copy lines from other invoices, orders, or shipments. Invoices can be linked to service agreements for financial reporting.

---

### 🧭 Navigation

- Access via: Main menu => Invoice (Customer) window

---

### 🛠️ Functionality

- **Header Features**: Define invoice details like Organization, Document No, Date Invoiced, Business Partner (e.g., NDIS), Support Receiver, and Funding Body Number. Set Payment Rule, Payment Term, and Sales Representative.
- **Invoice Line Tab**: Add lines with Product, Quantity, Price, and Claim Type (e.g., Non-Face-to-Face Support Provision). Specify Start Date, End Date, and UOM (e.g., Hour). Link to Project and Activity for reporting.
- **Copy Lines from Invoice Process**: Access via the process toolbar cog to copy lines from another invoice into the current invoice.
- **Copy Lines from Button**: Use the "Copy Lines from" button to copy lines from an Order or Shipment/Receipt, selecting the Business Partner and specific Order or Shipment/Receipt.
- **[(DRAFT)Document-Action]((DRAFT)Document-Action.md)**: Set the invoice status using the Document Action dropdown and post to the GL [(DRAFT)Transaction-General-Ledger-Posting]((DRAFT)Transaction-General-Ledger-Posting.md). 
- **Table**: Invoice (customer) is on the C_Invoice table, same as Invoice (vendors). 
- Note the invoice is the transaction in which the **tax component (GST)** is documented and posted. The tax amount is at the line level and will automatically calculate based on the Product or Charge selected. Further it can be manually updated.  

---

### 🎯 Tips

- Link invoices to a Project in the Reference section to enable financial reporting by service agreement.
- Ensure customer [(DRAFT)Business-Partner]((DRAFT)Business-Partner.md) is completed as much as possible to automate the population of fields when the customer is selected. 
- Set the Claim Type accurately on invoice lines to ensure NDIS compliance during bulk claiming. This will copy from bookings. 
- Keep the Date Invoiced and Account date the same to avoid differences between your Aging reports and your general ledger. The account date will be the date used for the posting. 

---

### 📝 Notes

- Ensure the Date Invoiced matches the billing period for accurate financial reporting.
- The Funding Body Number is required for NDIS invoices to align with compliance requirements.

---
(end of note)
