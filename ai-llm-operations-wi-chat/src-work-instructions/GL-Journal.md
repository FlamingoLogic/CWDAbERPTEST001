---
aliases:
  - GL Journal
  - General Ledger Entry
tags:
  - workinstructions
  - tool
  - finance
---

# 🏷️ GL Journal Window

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the GL Journal window in AbilityERP to manually create, edit, and post journal entries to the General Ledger.

---

## 📚 Description  
The GL Journal window in iDempiere / AbilityERP allows users to create, edit, and post manual journal entries for the General Ledger.

---

## 🧭 Navigation  
- Access via: Main Menu => GL Journal

---

## 🛠️ Functionality  
- Create a new journal batch, journal, and journal lines.  
- Copy existing journals and their details to streamline entry.  
- Edit journal header and line details.  
- Post journals to update the General Ledger.

---

## 🗂️ Field Details  

### 🧾 Header (GL Journal Window)  
- **Batch Document No**: Identifier for the journal batch (optional; defaults if blank).  
- **Document No**: Unique identifier for the journal (defaults if blank).  
- **Document Date**: Date of the journal document; updates Accounting Date unless overridden.  
- **Accounting Date**: Date the journal affects the ledger; syncs with Document Date by default.  
- **Period**: Accounting period (e.g., Feb-2025).  
- **Currency**: Currency of the journal (e.g., USD).  
- **Control Amount**: Optional total to validate debit/credit balance (set to 0 to skip).  
- **Total Debit**: Sum of debit amounts (read-only).  
- **Total Credit**: Sum of credit amounts (read-only).  
- **GL Category**: Category for reporting (e.g., Manual).

### 🧾 Lines (Line Subtab)  
- **Line No**: Sequence number for journal lines (auto-increments).  
- **Account**: GL account for the line (e.g., Loan Interest).  
- **Source Debit**: Debit amount for the line.  
- **Source Credit**: Credit amount for the line.

---

## 🎯 Tips  
- **Copy Processes**:  
  - Use the "Copy" button on the toolbar to duplicate the current journal header: Click Copy on the toolbar to create a new journal.  
  - Use "Copy Details" to copy lines: In the GL Journal window, click the cog icon on the toolbar => Select "Copy Details" process => Choose the journal to copy lines from.

- **Date Sync**: Updating Document Date in the header adjusts Accounting Date unless Accounting Date is manually set.  
- **Minimal Entry**: Focus on required fields (Document Date, Account, Amounts) for efficiency.  
- **Reporting Fields**: On the Line tab, set Business Partner and Activity for better reporting and analysis.  
- **Accruing Income**: It is almost always more effective to use journaling to manage accrued income rather than complicating the invoicing process to avoid it.  
- **Description Caution**: Do not include the month in the journal description; it will copy over and require manual updates.  
- **Posting**: Use the "Post" action in the GL Journal window after entering details.

- **Customisation**:  
  - For certain repetitive journals, it could be advantageous to develop a customization that streamlines the process. One approach would involve creating a process that extracts AbERP data and displays it in a temporary window or table for review, representing potential journal lines. Users could then modify this data by adding, removing, or editing entries as needed. A subsequent process could transfer the finalized data into the journal of your choice as line items. Depending on the complexity, this customization might require 10–20 development hours. Note that a separate journal window and process already exist for fixed assets.

  - An alternative, and potentially more efficient, starting point could be leveraging the [AbERP-Postgres-Export-Copy-Command](AbERP-Postgres-Export-Copy-Command.md). By utilizing the SQL field to generate the required CSV file, you can achieve highly flexible results with minimal limitations, thanks to SQL’s capabilities. The CSV can then be imported into the Journal lines. This method could deliver approximately 95% of the functionality provided by the more intricate process-based approach with less resources.

---
(end of note)
