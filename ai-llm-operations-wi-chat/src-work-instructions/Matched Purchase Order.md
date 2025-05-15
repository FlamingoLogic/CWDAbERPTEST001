---
aliases:
  - Matched Purchase Orders
  - Match PO
tags:
  - workinstructions
  - tool
  - finance
  - purchasing
  - inventory
---

# 🏷️ Matched Purchase Orders Window

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the Matched Purchase Orders Window — used to align [purchase-order](purchase-order.md)s and [Material-Receipt](Material-Receipt.md)s, manage cost tracking, and ensure accurate commitment accounting in AbilityERP.

---

## 📚 Description  
The Matched Purchase Orders Window tool simplifies the alignment of purchase orders and material receipts by linking related records and managing cost and quantity updates. This tool in AbilityERP updates [Purchase-Order](Purchase-Order.md) → Line subtab quantities, adjusts Product Cost records for certain costing methods, posts Purchase Price Variance (PPV) account balances, and relieves commitment accounting balances created by the Purchase Order.

---

## 🧭 Navigation  
- Access via: Main menu => Matched Purchase Orders window.  
- Or: Open directly from **Purchase Order** → Line subtab → **Matching** tab.  
- Or: Open directly from **Material Receipt** → Line subtab → **Matched POs** tab.  
- Or: Open directly from **Invoice (Vendor)** → Line subtab → **Matched POs** tab.

---

## 🛠️ Functionality  
- Links **Material Receipt** → Line subtab records to **Purchase Order** → Line subtab records.  
- Automatically generates a matched purchase order record when a Material Receipt is completed, provided the **Order** field in the Material Receipt → Line subtab is populated.  
- Supports **manual matching** via the **Matching PO-Receipt-Invoice** form if the **OrderLine** field is empty upon completion.  
- Updates:
  - **Purchase Order** → Line → Quantity field details  
  - **Product Cost** records for costing methods like **Standard Costing** or **Moving Average**  
- Posts **Purchase Price Variance (PPV)** to the PPV account if the PO price differs from the product’s cost price  
  - Example: DR Purchase Price Variance $XX, CR Inventory Account $XX  
- Relieves **commitment accounting balances** created by the Purchase Order  
- No accounting entry is created:
  - If there is no variance between PO price and product cost  
  - If a **Charge** is used instead of a Product

---

## 🎯 Tips  
- Use **Charges** instead of Products for expenses that don’t require inventory tracking to prevent Match PO document creation and simplify expense posting.  
- Ensure the **Order** field in the Material Receipt → Line subtab is populated before completing the Material Receipt to enable automatic matching.  
- Review matched purchase order records periodically to track variances and understand cost impacts, especially for costing methods like Standard Costing or Moving Average.  
- Use the **Matching PO-Receipt-Invoice** form to manually create matched purchase order records if automatic matching fails due to an empty **OrderLine** field.  
- Monitor PPV postings in the [Unposted Documents Window](Unposted-Documents.md).

---

## 📝 Notes  
- Match PO records are not generated for **Charges**.

---
(end of note)
