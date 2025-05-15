---
aliases:
  - Matched Invoices
  - Matching PO Receipt Invoice
tags:
  - workinstructions
  - tool
  - finance
  - purchasing
  - inventory
---

# 🏷️ Matched Invoices Window

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the Matched Invoices Window — used to reconcile [invoice-(vendor)](invoice-(vendor).md)s, [material-receipt](material-receipt.md)s, and [purchase-order](purchase-order.md)s for accurate financial and inventory tracking in AbilityERP.

---

## 📚 Description  
The Matched Invoices Window tool simplifies the reconciliation of invoices, material receipts, and purchase orders by linking related records and managing account offsets. This tool in AbilityERP offsets Not Invoiced Receipt (NIR), the Invoice Expense, and Inventory Clearing (IC) account balances, calculates and posts Invoice Price Variance (IPV) account balances, and updates Product Cost values, ensuring accurate financial tracking and inventory management.

---

## 🧭 Navigation  
- Access via: Main menu => Matched Invoices window.  
- Or: Open directly from **Invoice Vendor** → **Line** subtab → **Matched Receipts** tab.  
- Or: Open directly from **Material Receipt** → **Line** subtab → **Matched Invoices** tab.

---

## 🛠️ Functionality  
- Displays matched invoice records linking:
  - **Invoice (Vendor)** → Line subtab  
  - **Material Receipt** → Line subtab  
  - **Purchase Order** → Line subtab  
- Automatically generates matched invoice records when a Material Receipt or Invoice (Vendor) is completed, provided the **OrderLine** field is populated in either the Material Receipt → Line subtab or Invoice (Vendor) → Line subtab.  
- Supports **manual matching** via the **Matching PO-Receipt-Invoice** form when the **OrderLine** field is empty upon completion.  
- **Manages account offsets**:
  - Expense posting on the matched invoice offsets the invoice
  - Not Invoiced Receipts offset the Material Receipt
  - Invoice’s AP details are left to post
- Updates **Product Cost** values  
- Posts **Invoice Price Variance (IPV)** for cost tracking

---

## 🎯 Tips  
- Regularly review matched invoice records to ensure proper linking between invoices, material receipts, and purchase orders, especially after completing Material Receipts or Invoices (Vendor).  
- Use the **Matching PO-Receipt-Invoice** form to manually create matched invoice records if automatic matching fails due to an empty **OrderLine** field.  
- Verify the **OrderLine** field is populated in the Material Receipt → Line subtab or Invoice (Vendor) → Line subtab before completing documents to enable automatic matching.  
- Monitor the **Period Closed** status to ensure matched invoices are processed in the correct accounting period.

---

## 📝 Notes  
- Manual matching may be required if the **OrderLine** field is not populated, which can occur if purchase orders are not linked during material receipt or invoicing.

---
(end of note)
