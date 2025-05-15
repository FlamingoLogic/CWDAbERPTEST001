---
aliases:
  - NDIS Export
tags:
  - workinstructions
  - tool
  - finance
  - claiming
---

# 🏷️ Export NDIS Invoice Data

*Matt Law | Last Updated: 2025-05-07*

This document defines the Export NDIS Invoice Data functionality, navigation, tips, and related tools within the organisation’s systems and processes.

---

### 📚 Description

Exports invoice data from AbilityERP in a format compatible with the NDIS portal for claiming, using the AbERP Postgres Export Copy Command. Generates a CSV file with NDIS-specific columns like Support Number, Claim Type, and Unit Price, based on a custom SQL query.

---

### 🧭 Navigation

- Access via: Main menu => Export NDIS Invoice Data

---

### 🛠️ Functionality

- Exports invoice data within a specified date range and document status for NDIS claiming.
- Parameters:
  - **Date From**: Start date for the invoice data range (e.g., `SupportsDeliveredFrom` in the export).
  - **Date To**: End date for the invoice data range (e.g., `SupportsDeliveredTo` in the export).
  - **Doc Status**: Dropdown to filter invoices by document status (e.g., "Drafted").
  - **Run as Job**: Checkbox to run the export in the background for larger datasets.
- Output: Generates a CSV file with columns:
  - `RegistrationNumber`, `NDISNumber`, `SupportsDeliveredFrom`, `SupportsDeliveredTo`, `SupportNumber`, `ClaimReference`, `Quantity`, `Hours`, `UnitPrice`, `GSTCode`, `AuthorisedBy`, `ParticipantApproved`, `InKindFundingProgram`, `ClaimType`, `CancellationReason`, `ABN of Support Provider`.
- Uses the [AbERP-Postgres-Export-Copy-Command](AbERP-Postgres-Export-Copy-Command.md) with a predefined SQL query.

---

### 🎯 Tips

- Verify the date range aligns with NDIS claiming periods before uploading to the portal.

---

### 📝 Notes

- The export is designed for NDIS portal uploads; ensure all required fields (e.g., `SupportNumber`, `ClaimType`) are populated correctly.
- Custom SQL query is defined in the [AbERP-Postgres-Export-Copy-Command](AbERP-Postgres-Export-Copy-Command.md); contact support to modify the query if needed.

---
(end of note)
