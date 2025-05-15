---
aliases:
  - Support Location
tags:
  - workinstructions
  - tool
  - SIL
  - dayoptions
  - operations
---

# 🏷️ Support Location

*Matt Law | Last Updated: 2025-05-02*

The **Support Location** tool is designed to manage physical service locations in AbilityERP, particularly for SIL homes, Day Options, and other community programs. It centralises details such as address, access info, alerts, capacity, and rostering needs—making it a core component for compliance, staff scheduling, and safeguarding.

---

### 📚 Description

The Support Location window captures structured data about any physical care location. It links to alerts, activities, rooms, and credential requirements. This enables downstream rostering, documentation, and quality assurance workflows.

---

### 🧭 Navigation

- Access via: `Main Menu => Support Location`  
- *Zoom to* from other windows where referenced. 

---

### 🛠️ Functionality

#### Header Fields
- **Partner Location**: Business Partner associated with the site.
- **Support Location Type**: E.g., SIL, Day Options, Respite.
- **[[NDIS-Region]]**: Regions as defined by the NDIA.
- **Occupant Type**: Typically Adult or Child.
- **Location Address / Region**: For geographic context and reporting.
- **Employee Responsible**: Allocated staff for oversight.
- **External Weblinks**: For site-specific documents or portals.
- **Alert**: High-priority safety or utility information.
- **Bushfire Danger Area**: Checkbox for compliance workflows.

#### Access & Property
- **Key Box Access / Alarm Code**: For staff access logistics.
- **Access Details**: Plain English instructions.
- **Accessibility Features / Wheelchair Access**: Supports compliance and rostering.
- **Property Type / Tenancy Type / Property Manager**

#### Capacity
- **Identify Rooms**: Tickbox triggers room-level tracking.
- **Capacity**: Number of clients the property supports.
- **Additional Capacity Information**: Narrative context.

---

### 📂 Tabs

#### **Rooms**
- Captures room-specific data, including [[Room-Use]] (e.g., Client Bedroom, Staff Bedroom) and occupant history. 

#### **[Alerts](Alerts–Operations.md)**
- Define location-specific alerts (e.g., asbestos risk) and optionally display on header window.

#### **[Activity](Activity-Viewer)**
- Logs activities (e.g., events, inspections, tasks completed, meetings) tied to this location using Activity Viewer infrastructure.

#### **[[Rostering-Needs]]**
- Set required credentials, gender requirements, or restrictions for staff working at this location.
- Enables validation at the shift level during roster allocation.
  
---

### ✅ Tips

- Use the **"Identify Rooms"** tickbox to enable room tracking.
- Create **alerts** for each known hazard and tick “Show As Alert” for onscreen visibility.
- Populate **rostering needs** early to activate validation rules in shift allocation.
- Use **Activity tab** for events (e.g., maintenance).

---

### 🔗 Related Tools

- [[Support-Receiver-(BP)]]
- [[Master-Location]]
- [Locations-Tab](Locations-Tab.md)
- [[(Draft)Support-location-room-view]]

---
(end of note)