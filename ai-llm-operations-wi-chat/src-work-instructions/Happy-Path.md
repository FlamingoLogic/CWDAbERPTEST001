---
aliases:
  - Happy-Path
tags:
  - abilityerp
  - claiming
  - onboarding
  - happypath
  - core
---

# 🛣️ Happy Path: Disability Service Provider

*Matt Law | Last Updated: 2025-05-15*

This is the primary, recommended workflow for disability service providers in AbilityERP. It is designed to prioritise efficiency, compliance, and data accessibility — while still allowing for customisation by client.

---

## 🔁 Core Flow: Enquiry to Claiming

### 1. Intake & Planning

- Create [[Enquiry]]  
- Convert to [[Support-Receiver-(BP)]] and [[Service-Opportunity]]
- Complete key details: [[BP-Association]], Legal Orders, Plans, Goals  
- Confirm resourcing, including available staff

### 2. Service Booking & Agreement

- Create price estimate: [[Service-Booking]]  
  → Use [[Booking-Generator]] if appropriate
- Draft [[Service-Agreement]] and send for client approval
- Upload signed agreement
- Update [[Support-Receiver-(BP)]] to *Receiving Support* and Agreement to *Executed*

### 3. Operational Setup

- Review or set up [[Support-Location]]
- Review or set up [[Vehicle]]
- Add to or create [[Shift-(Rostered)-Template]] as needed
- Raise [[Purchase-Order]] for rent, PPE
- Process incoming [[Invoice-(Vendor)]]
- **Create standard bookings for claiming** (monthly blocks)  
  → Use [[Booking-Generator]]  

- 📆 **Client-Specific Frequencies**  
  - **Claiming Frequency**: (e.g., Weekly, Monthly)  
  - **Timesheet Approval Frequency**: (e.g., Fortnightly)  
  - **Payroll Frequency**: (e.g., Fortnightly)

---

## 🕒 Rostering & Delivery

- Use [AbERP-Generate-Rostered-Shifts](AbERP-Generate-Rostered-Shifts.md)
  → After save event on rostered shift Auto-removes unavailable/on-leave staff and creates leave assignments. 
- Fill unassigned shifts via [[Shift-(Rostered)-Employee-View]]
- Support Worker reviews shifts in [[My-Shifts]]
- During shift:
  - View [[Support-Reciever-(BP)-Mobile]]
  - Complete [[Request]], log case notes and goal progress

---

## ✅ Validation & Claiming

- **Overnight process auto-updates** [[Service-Booking]] lines:
  - `Time Status` → based on shift/timesheet
  - `Validated` → based on validation plugin logic
  - `Ready to Claim` → based on rule or manual tick

- [[Service-Booking]] validation can occur:
  - On Doc Action (completion)
  - On Validated checkbox (line-level review)

- Optional comparison to [[Allocation-Records]] to confirm service was delivered  
  → Especially useful for shared support scenarios

- Review booking line gaps via [[Advanced-Search-Orders]] saved queries or DSIs
- Generate invoices via [[Generate-invoices]]:
  - Filter by `Ready to Claim`, activity, location, date range
- Upload NDIS claims with [[Export-NDIS-Invoice-Data]]
- Complete and email invoices via [[Invoice-(Customer)]]

---

## 🧾 Payroll & Financials

- Generate timesheets from shifts via [AbERP-Generate-Timesheets](AbERP-Generate-Timesheets.md)
- Approve timesheets in [[Timesheet-Approval]]
- Export from [[(DRAFT)AbERP-Timesheet-Export]] for payroll processing
- Import to payroll system, complete payroll run
- Upload timesheet references to [[(DRAFT)Timesheet-External-Manager]]
- Post payroll journal via [[GL-Journal]]
- End-of-month payroll journals: [[Manage-Salaries-and-Wages-in-AbilityERP]]

---

## 📊 Oversight & Reporting

- Review delivery volumes via [[(PROPOSED)-Service-Delivery-Summary-View]]
- Analyse spend in [[Service-Agreement-Line-View]]
- Run financial reports via [[(DRAFT)Financial-Report]]
- Review case notes in [[Activity-Viewer]]
- Use [[(DRAFT)-MetaBase]] for advanced analytics

---

## 📌 Notes for NDIA Audit Evidence

NDIA may request:

- Support plans, case notes, goals
- Timesheets and rosters
- Evidence of 1:1 vs 1:3 decisions
- Invoices and Service Agreements
- Travel and mileage logs
- Confirmation participant agreed to services
- Description and outcomes of supports

Maintain traceable, timestamped data across bookings, shifts, and invoices for each support receiver.


---
(end of note)
