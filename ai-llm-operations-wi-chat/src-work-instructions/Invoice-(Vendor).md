---
aliases:
  - Vendor Invoice
  - AP Invoice
tags:
  - workinstructions
  - tool
  - purchasing
---

# 🏷️ Invoice (Vendor)

*Matt Law | Last Updated: 2025-05-09*

This document defines the **Invoice (Vendor)** window functionality, navigation, tips, and related tools within the organisation’s systems and processes. This window is based on iDempiere’s `C_Invoice` table and has minor enhancements in AbilityERP (e.g. additional reference fields like Vehicle and Contract Location).

---

### 📚 Description

The **Invoice (Vendor)** window is used to record and process supplier invoices. It can be populated manually or by linking to upstream purchasing documents such as Purchase Orders or Material Receipts. Posting the invoice creates financial entries in the general ledger and optionally links to payments.

---

### 🧭 Navigation

- Access via: `Main menu => Invoice (Vendor)`

---

### 🛠️ Functionality

#### Header
- **Date Invoiced / Account Date**: Controls timing of financial posting.
- **Business Partner / Partner Location**: Supplier details.
- **Currency, Payment Term, Price List, Payment Rule**: Finance and payment logic.
- **Reference Fields**: Includes `Contract Location`, `Vehicle`, `Activity`, `Project`, and `Group Sessions` (AbilityERP extensions).

#### Lines
- Add detail by **Product** or **Charge**.
- Set **Quantity**, **UOM**, **Price**, and **Tax**.
- Reference upstream lines (e.g., **Purchase Order Line**, **Receipt Line**) for matching and auditability.
- Auto-calculates **Line Amount** and **Tax Amount** based on selections.

#### Tabs
- **Invoice Line** – Main invoice items.
- **Landed Costs / Allocation / Matching Tabs** – Advanced reconciliation, typically only used by finance or admins.
- **Matched POs** and **Matched Receipts** – Links to upstream documents (if used).

---

### 🔁 Key Processes (Toolbar)

1. **Create Lines From**
   - Populates the invoice based on selected Purchase Orders or Material Receipts.
   - Opens a dialog to filter by Business Partner and documents.
   - ![View](processed_vendor_invoice_docs/invoice_vendor_create_lines_from.png)

2. **Copy Lines**
   - Copies lines from another invoice.
   - Useful for repeated supplier charges.

3. **Generate Receipt from Invoice**
   - Creates a material receipt entry for the vendor invoice (used when receiving is tracked after invoicing).

---

### 🎯 Tips

- Use **Create Lines From** when you have linked Purchase Orders or Receipts — it ensures accurate posting and avoids retyping.
- Enter both **Date Invoiced** and **Account Date** correctly to ensure they align with the correct accounting period.
- Link **Contract Location**, **Activity**, and **Project** fields where applicable for improved reporting.
- If you need to validate approvals or business rules, use the [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md).

---

### 📝 Notes

- Table: `C_Invoice`
    
- This window is used for entering and managing supplier invoices, including matching to purchase orders and receipts.
    
- Unlike Payments or Bank Statement lines, **this is the only purchasing document in iDempiere that posts tax**.
    
    > 🔔 **Important**: If you need to post tax (e.g., for GST/VAT), you must enter an invoice — you cannot post tax directly from a Payment or Bank Statement line to an expense.
    
- Matched Purchase Orders and Receipts will appear automatically if invoice lines were generated via the _Create Lines From_ process or matched manually.
    
- Line-level posting is based on the **Account Date**, not the Invoice Date.
    
- All amounts and tax calculations follow the selected **Price List**, **Currency**, and **Tax Category**.

---

### 🛠️ Related Tools

- [Purchase-Order](Purchase-Order.md)
- [Material-Receipt](Material-Receipt.md)
- [AbERP-Document-Validation-Plugin](AbERP-Document-Validation-Plugin.md)

---
(end of note)
