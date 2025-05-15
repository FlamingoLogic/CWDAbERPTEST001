---
aliases:
  - Sales Order
  - SO
tags:
  - workinstructions
  - tool
  - claiming
  - client
  - finance
---

# 🏷️ Sales Order

*Matt Law | Last Updated: 2025-05-07*

This document defines the Sales Order functionality, navigation, tips, and related tools within the organisation’s systems and processes.

---

### 📚 Description

Sales Order in AbilityERP is a control document for managing transactions, enabling planning, automation, and validation of sales processes, including shipments and invoices. Note much of this content is also relevant to [Service-Booking](Service-Booking.md)

---

### 🧭 Navigation

- Access via: Main menu => Sales Order window

---

### 🛠️ Functionality

- Displays in-progress and completed transactions from the last 24 hours upon opening.  
- Supports multiple Target Document Types to drive automation (most automations occur upon order completion):  
  - **Binding Offer**: Generates an order document only (quote, binding).  
  - **Non-Binding Offer**: Generates an order document only (quote, non-binding).  
  - **Standard Order**: Creates an order only.  
  - **Warehouse Order**: Generates an order and shipment.  
  - **Credit Order**: Generates an order, shipment, and invoice.  
  - **POS Order**: Generates an order, shipment, invoice, and payment.  
  - **Prepay Order**: Generates an order and invoice, with shipment upon payment.  
- Allows conversion of quotes by changing the Target Document Type (loses quote history) or using the Quote Convert process.  
- Tracks the status of order lines (e.g., one sales order line can have multiple shipment or invoice lines).  
- Uses Date Ordered and Date Promised to manage pricing and scheduling:  
  - **Date Ordered**: Indicates when the order was received; used with price list version dates to determine applicable prices (update Date Ordered to ensure correct pricing).  
  - **Date Promised**: Specifies the expected date to ship the product or provide the service. Can be used as a parameter in the generation of shipments.  
- Supports automation through fields like Delivery Rule and Invoice Rule:  
  - **Delivery Rule**: Dictates when products are shipped:  
    - "After Receipt": Shipped after payment receipt.  
    - "Availability": Shipped when inventory is available.  
    - "Complete Line": Shipped when the full quantity for a line is ready.  
    - "Complete Order": Shipped when the full quantity for all lines is ready.  
    - "Force": Shipment is forced regardless of quantity.  
    - "Manual": Shipment is not automatically generated (requires manual process).  
  - **Invoice Rule**: Dictates when invoices are generated:  
    - "After Delivery": Invoices after individual shipments.  
    - "After Order Delivery": Invoices after the entire order is delivered.  
    - "Customer Schedule After Delivery": Invoices based on customer schedule post-delivery.  
    - "Immediate": Immediately available to invoice upon order completion (shipments have no impact).  

---

### 📝 Notes

- Use **"Prepare"** status to reserve resources without completing the order; **"Complete"** status makes the order available for processes like shipment generation.  
- Voiding an order reverses all related shipments and invoices; use with caution.  
- Closing an order with undelivered quantities moves them to **"Qty Lost Sales"**; review via the **Open Order** report.  
- An order can be reactivated and amended after completion if adjustments are needed.  
- Test Sales Order configurations in a sandbox, as they affect postings and automation.  
- Refrain from modifying the **Delivery Rules** or **Invoice Rules**, as these are foundational lists, and alterations could lead to unforeseen issues. Instead, incorporate custom fields into the order table and either extend an existing process or develop a new one to utilise these fields for tailored workflows.

---
(end of note)
