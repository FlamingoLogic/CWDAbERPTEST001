---
aliases:
  - Tool-GroupSessions
  - Group-Sessions
  - GroupSession-Reference
tags:
  - workinstructions
  - tool
  - rostering
  - client
  - operations
  - abilityerp
  - claiming
  - planning
---

# 🏷️ Group Sessions

*Matt Law | Last Updated: 2025-05-15*

The **Group Sessions** window is used to document and track operational group events such as day trips, excursions, or other multi-participant sessions. It supports clear communication and planning across teams by capturing key operational details, alerts, and activities. This window is used for **reference only** and does **not form part of the accounting dimensions**.

---

## 📚 Description

Group Sessions provide contextual reference for shifts and bookings, especially for off-site or group-based service delivery. These records can be linked to Service Bookings, Shift (Rostered), and other operational tools to support planning and compliance.

Use cases include:
- Excursions (e.g., zoo visits)
- In-house themed activity days
- Outings with vehicle involvement
- Capacity tracking for shared sessions

---

## 🧭 Navigation

- Access via: **Main Menu → Group Sessions**
- Can be referenced from:
  - [Service Bookings](Service-Booking.md)
  - [Shift (Rostered)](Shift-(Rostered).md)

---

## 🪟 Header Fields

| Field | Description |
|-------|-------------|
| **Name** | Title of the session (e.g., “Day Trip to Zoo”). |
| **Alert** | Displayed prominently above the description for quick attention. |
| **Description** | Detailed session overview (e.g., itinerary, logistics). |
| **Session Specific Accessibility** | Notes about physical access or safety concerns. |
| **[Group-Type](Group-Type.md)** | Category of event (e.g., Day Trip, In-House, Excursion). |
| **Start/End DateTime** | Session timing. |
| **Support Receiver Capacity** | Optional participant cap. |
| **Sales Representative** | Responsible staff member. |
| **Contract Location / Vehicle** | Operational references for planning purposes. |

---

## 📋 Tabs Overview

### ⚠️ Alerts

- Stores safety, weather, transport, or support instructions.
- Refer to: [Alerts–Operations](Alerts–Operations.md)
- Key fields include:
  - **Alert Type**: e.g., Weather, Other
  - **Description / Name**: Shown as banner alert
  - **Show as Alert**: Tick to display prominently
  - **Valid From / To**: Defines alert visibility timeframe
- Can store multiple alerts with priority determined by `Line No`.

### 📝 Activity

- Used for logging updates, preparation notes, or event review.
- Driven by: [Activity-Viewer](Activity-Viewer.md)
- Can log communication, planning tasks, weather prep, etc.
- Typical Activity Types: Task, Appointment

---

## 🔄 Operational Use

- **Does not affect financial records** or allocation logic.
- Purely operational for support team context and planning.
- Can be referenced from:
  - [Service Bookings](Service-Booking.md)
  - [Shift (Rostered)](Shift-(Rostered).md)
- Recommended to create a new record per outing or session for clarity and traceability.

---

## 🎯 Tips

- Use alerts for weather risks, transport notes, or client prep (e.g., "bring lunch").
- Leave `Valid To` blank for standing alerts (e.g., recurring risks).
- Link to a **Vehicle** for excursions to track asset use.
- Keep description detailed for handover purposes across teams.

---

## 🛠️ Related Tools

- [Alerts–Operations](Alerts–Operations.md)
- [Activity-Viewer](Activity-Viewer.md)
- [Service-Booking](Service-Booking.md)
- [Shift-(Rostered)](Shift-(Rostered).md)

---
(end of note)
