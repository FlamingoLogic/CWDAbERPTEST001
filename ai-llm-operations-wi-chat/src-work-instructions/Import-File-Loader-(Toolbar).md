---
aliases:
  - CSV Import
  - File Upload Tool
  - Toolbar Importer
tags:
  - workinstructions
  - tool
  - import
  - configuration
  - efficiency
  - ui
---

# 🏷️ Import File Loader (Toolbar)

*Matt Law | Last Updated: 2025-05-01*

The **Import File Loader** is a toolbar tool that enables bulk import of CSV-formatted data into any window in iDempiere/AbilityERP. It supports header and line-level imports and is used widely for setup, updates, and mass entry of transactional or master data.

---

## 📚 Description

This tool allows data import via CSV files directly from any window’s toolbar. You can insert new records, update existing ones, or merge depending on your needs. Unlike standard import windows, this tool does not use a temporary staging table.

---

## 🧭 Navigation

- Open any window
- Click the **Import File Loader** icon in the toolbar

---

## 🛠️ Functionality

- Accepts **CSV files** with **hardcoded values only**
- Three import modes:
  - **Insert** – Adds new records; fails if duplicates exist
  - **Update** – Updates existing records; fails if a matching header is not found
  - **Merge** – Combines insert + update logic
- Imports header and tab records in one file using column naming conventions
- Relies on field-level mapping using column headers
- No staging or pre-validation screen; records are written directly

---

## 🔧 Tips

- If a file fails to upload, it is often **not saved as CSV** — check formatting
- **Leave the file open** before upload; some systems reformat on reopen
- Import in **standard view**, not grid toggle
- Start with **one row** to confirm format and avoid bulk errors
- Date format: `yyyy-mm-dd`
- DateTime format: `yyyy-mm-dd hh:mm:ss`
- Assess the **log file** post-import to check for row-level errors or confirmations
- You can import **only the fields you need** — not every field is required
- To get column names:
  - Use the **Export** option from the same window, select **CSV single line**
- Use `TableName_ID[Value]` or `TableName_ID[Name]` for foreign key lookups
- For line tab imports, use `/K` to identify the parent header (e.g., `DocumentNo/K`)

---

## 🧪 Common Use Cases

- Import **journal lines** into the [GL Journal](GL-Journal.md) window  
- Load or update **product prices** in price lists  
- Load **bookings**: header first, then booking lines  
- Import data during **initial implementation or mass updates**

---

## ⚠️ Limitations

- No review screen — no import staging table  
- Cannot simultaneously import header and lines in a single row  
- For advanced needs or pre-review, use a standard import window like [Import-GL-Journal](Import-GL-Journal.md)

---

## 📄 Examples

### ✅ Service Booking – Header

| AD_Org_ID[Name] | C_DocTypeTarget_ID[Name] | DocumentNo | C_BPartner_ID[Value] | SalesRep_ID[Name] |
|------------------|--------------------------|------------|-----------------------|--------------------|
| Bern SILI        | Service Booking - Standard | 101 SIL Weekly | Bern                  | Rose Dash         |

### ✅ Service Booking – Lines (Linked to Header)

| C_Order_ID[DocumentNo] | C_OrderLine_M_Product_ID[Value] | C_OrderLine_Description | C_OrderLine_StartDate | C_OrderLine_EndDate | C_OrderLine_QtyEntered | C_OrderLine_PriceEntered |
|------------------------|-------------------------------|--------------------------|------------------------|----------------------|--------------------------|---------------------------|
| 101 SIL Weekly         | SIL WEEKLY                    |                          | 2025-05-01             | 2025-05-01           | 1.0                      | 53.00                     |

### ✅ Price List Import

| M_PriceList_Version_ID[Name] | M_Product_ID[Value] | PriceList |
|------------------------------|---------------------|-----------|
| NDIS 2024-2025               | ASS_SELF_STD_WKNIGHT | 75.82     |

---

## 💬 FAQ

**Q: What's the best way to get the format needed for import?**  
A: Use the **Export** option on the window toolbar (CSV single line) to download a file with correct column headers — including tabs. Modify and re-import.

---
(end of note)
