---
aliases:
  - Unposted Documents
  - GL Posting Monitor
tags:
  - workinstructions
  - tool
  - finance
  - compliance
---

# 🏷️ Unposted Documents

*Matt Law | Last Updated: 2025-05-01*

This document outlines how to use the Unposted Documents window — a tool for identifying documents that have not yet posted to the general ledger, helping maintain financial accuracy and compliance.

---

## 📚 Description  
The Unposted Documents Window tool simplifies monitoring of documents that have not yet posted to the general ledger by displaying records with pending or failed postings. Importantly you can filter on records that have been processed but did not post. This tool in AbilityERP helps users identify and resolve unposted documents, ensuring financial accuracy and compliance, especially since some documents process and post in the background. The unposted document window ensures these are actively monitored.

---

## 🧭 Navigation  
- Access via: Main menu => Unposted Documents window.

---

## 🛠️ Functionality  
- Displays a list of unposted documents with key details (e.g., Document No, Document Date, Account Date, Document Status, Posting Status).  
- Allows filtering (e.g., `C_Payment` for payment transactions).  
- Includes a **Record ID** button to navigate directly to the specific unposted document for review or action.  
- Supports filtering for documents that are processed but recorded a posting error, using the **Posting Status** field.  
- Posting statuses include:  
  - Deferred  
  - Invalid Account  
  - Not Balanced  
  - Not Convertible (no rate)  
  - Not Posted  
  - Period Closed  
  - Post Prepared  
  - Posted  
  - Posting Error  
- Supports integration with Document Status Indicators (DSIs) to highlight unposted documents by posting status and accounting period (e.g., current month, prior periods).

---

## 🎯 Tips  
- Monitor this window at least weekly to catch unposted documents early — do not wait until month-end, as frequent checks help address issues proactively.  
- Set up DSIs via [Activities-and-Dashlets](Activities-and-Dashlets.md) on the homescreen to filter unposted documents by posting status and accounting period (e.g., one DSI for "Posting Error" in the current month, another for "Deferred" in prior periods).  
- Focus on the **Posting Error** status to identify documents that processed but failed to post, and resolve these promptly to avoid financial discrepancies.  
- Use the **Record ID** button to quickly navigate to and address unposted documents.  
- Ensure all postings are complete before closing an accounting period to maintain accurate financial records.  
- Regularly review DSIs to keep them relevant for your organization’s accounting cycles.

---

## 📝 Notes  
- Unposted documents in closed accounting periods may require manual intervention or re-opening of the period — consult with the finance team before proceeding.  
- DSIs should be configured by a System Admin to ensure accurate filtering of unposted documents.

---
(end of note)
