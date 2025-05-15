---
aliases:
  - Record Filtering
  - Table Filters
  - Role-Based Visibility
tags:
  - workinstructions
  - tool
  - configuration
  - sysadmin
  - compliance
---
## 🧷 Dynamic Filter per Table
*Matt Law | Last Updated: 2025-05-01*

**Dynamic Filter per Table** is a feature in AbilityERP that allows you to restrict the records visible in any given table using SQL-based rules. These filters are typically based on the logged-in user’s context (such as their user ID or role) and are applied dynamically at runtime. The feature is commonly used for enforcing compliance, safeguarding data visibility, and tailoring user experiences without duplicating windows or reports.

---

### ✅ What It Does

- Dynamically restricts **which records a user sees** in a window.
    
- Filters can be tied to:
    
    - **Logged-in user ID**: `@#AD_User_ID@`
        
    - **Logged-in user role**: `@#AD_Role_ID@`
        
- Multiple filters on the same table are joined with **AND logic**.
    
- Has **no impact on underlying security** — it simply filters what’s shown in the UI.
    

---

### 🛠 Where to Configure It

- **Navigation**:  
    → `System Admin => Dynamic Filter per Table`  
    → Or: Open any table window, go to the toolbar → `Filter Configuration`
    
- This config is stored per table, not per window, so it can be reused across different views of the same table.
    

---

### 🧪 Examples

#### 1. Show only records linked to the logged-in user

**Use case**: Staff should only see service bookings they are responsible for.

sql

CopyEdit

`C_Order.SalesRep_ID=@#AD_User_ID@`

#### 2. Filter by the user’s location

**Use case**: A user should only see clients who belong to their service location.

sql

CopyEdit

`C_BPartner.C_Location_ID=(SELECT C_Location_ID FROM AD_User WHERE AD_User_ID=@#AD_User_ID@)`

#### 3. Restrict based on role

**Use case**: Only members of the "Compliance Team" role should see safeguarding incidents.

sql

CopyEdit

`R_Request.R_RequestType_ID=(SELECT R_RequestType_ID FROM R_RequestType WHERE Name='Safeguarding') AND @#AD_Role_ID@=(SELECT AD_Role_ID FROM AD_Role WHERE Name='Compliance Team')`

---

### 💡 Best Practice Tips

- Always **test filters in a sandbox** first to confirm logic and avoid hiding critical data by mistake.
    
- Use **role-based filters** to segment views across programs (e.g., Day Options vs SIL).
    
- Pair with **Role Management** to make filtering clean and maintainable.
    

---

### ⚠️ Notes

- This feature is **not available by default** — it requires a **backport from iDempiere v11** to be enabled in AbilityERP.
    
- It only affects **what is visible** in windows — it does not restrict access to reports or processes.
    
- It’s especially useful for windows where visibility needs to be scoped without exposing sensitive client, staff, or finance records.

---

(end of note)