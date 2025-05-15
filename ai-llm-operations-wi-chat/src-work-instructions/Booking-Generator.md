---
aliases:
  - Booking Generator
  - Recurring Service Booking Tool
tags:
  - workinstructions
  - tool
  - client
  - claiming
  - growth
  - onboarding
---

# 🏷️ Booking Generator

*Matt Law | Last Updated: 2025-05-07*

This document outlines how to use the Service Booking Generator — a tool that automates the creation of recurring Service Bookings based on defined patterns and skip dates.

---

## 📚 Description  
The Service Booking Generator automates the creation of [Service-Booking](Service-Booking.md) records (headers and lines) in AbilityERP based on recurring service patterns. It supports alternating weekly schedules (e.g., Week 1 vs. Week 2), skip dates, and monthly breakdowns. This tool streamlines long-term booking creation, reducing manual effort and errors.

---

## 🧭 Navigation  
- Access via: Main menu → **Booking Generator** window

---

## 🛠️ Functionality  

- **Core Features**:  
  Define booking parameters in the **Booking Generator** header, including Organization, Business Partner (Client), Invoice Partner, Start Date, End Date, and Target Document Type:
  - `Service Booking – Standard`
  - `Service Booking – Binding Offer`
  - `Service Booking – Non-Binding Offer`

### 📅 Service Pattern Tab  
- Set up recurring delivery patterns using Start Day, End Day, Start Time, End Time, Product, Claim Type, and Quantity.
- Supports alternating weeks (Week 1 vs. Week 2) or consistent weekly setups.

### ⛔ Skip Dates  
- Select a named Skip Date list to exclude dates when services should not be generated.

### ⚙️ Generate Bookings  
- Triggered via the **Generate Bookings** header button
- Uses the Service Pattern tab and selected Skip Dates
- Booking generation differs by **Target Document Type**:

#### ▪ Standard
- Creates one **detailed Service Booking per calendar month**
- Lines reflect each day or block of service, ready for actual delivery
- No summarisation logic applies

#### ▪ Binding Offer
- Creates **a single detailed Service Booking** with a line for each individual date
- Booking mirrors the standard output in terms of line detail but consolidates into one booking
- Intended for quote use, retaining detail by service date

#### ▪ Non-Binding Offer
- Creates **a single summarised Service Booking**
- Summarises lines by Booking Generator line (i.e. the Service Pattern Line)
- Rounds total quantities and rates at the summarised level
- Total amount may slightly differ from Binding or Standard output due to rounding — which occurs after summarisation rather than at the individual line level

- Skips any Service Pattern Line whose calculated dates fall **outside the generator's Start/End Dates**

### 🗓️ Booking Assignment & Dates
- Lines are assigned to months based on **End Date**
- **Date Ordered** is set to the start of the month (or Generator Start Date for the first month)
- **Date Promised** is set to the end of the month (or Generator End Date for the last month)
- **Booking Line – Date Promised** is set to the line’s **End Date**

### 🔗 Clickthrough Fields
- Service Bookings are stamped with a **read-only reference** back to the Booking Generator
- Booking Lines are also stamped with the **Service Pattern Line**.

### 📋 Copy Process  
- Use the **Copy Service Pattern Lines** toolbar process to copy lines from another Booking Generator
- Only active lines are copied
- Speeds up setup when bookings share similar structures across clients or programs

---

## 🎯 Tips  
- Test alternating weekly patterns in a sandbox to verify correct week alignment.
- If Week 1 and Week 2 are identical, simply repeat Week 1.
- Use the Skip Dates tab to avoid generating bookings during known unavailable periods (e.g., public holidays).
- For offer bookings, review the summarised lines to ensure daily service representation is correct.
- When re-running the generation process, update the Start Date to avoid regenerating past bookings.
- Only Service Bookings are generated — existing bookings are not updated.
- For offer bookings, add the **day and time range** (Start Day, Start Time – End Time) to each line's **description** so key details are retained in the summary, as individual times are not on the lines on offers.

---

## 📝 Notes  
- Public holiday product substitution, alternative generation modes (e.g. weekly or fortnightly grouping), and integration with Service Agreements are planned for future versions.

---
(end of note)
