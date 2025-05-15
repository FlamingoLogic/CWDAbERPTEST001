---
aliases:
  - REST API
  - iDempiere REST API
tags:
  - tool
  - integration
  - sysadmin
  - workinstructions
---

# 🛠️ Tool: iDempiere REST API

*Matt Law | Last Updated: 2025-05-01*

Facilitates data movement between iDempiere and external systems over HTTP, enabling integrations like exporting timesheets or importing payroll journals via RESTful endpoints and Swagger UI.

---

## 📚 Description  
The REST API in iDempiere allows external systems to interact with internal ERP data using standard HTTP verbs. It supports both data-level operations (CRUD) and execution of server-side processes, making it a powerful tool for integration and automation.

---

## 🧭 Navigation  
- Access via:  
  - **Swagger UI**: `https://[your-idempiere-host]/swagger/`  
  - **API Endpoint Root**: `https://[your-idempiere-host]/api/v1/`

---

## ⚙️ Functionality  
- **Authentication**:  
  - Use `/api/v1/auth/tokens` to request a Bearer token.  
  - Token expires after ~1 hour. Refresh via `/api/v1/auth/refresh`.

- **Models Endpoint** (`/api/v1/models/`):  
  - Full CRUD for database records.  
  - Example:  
    - `GET /api/v1/models/hr_timesheet?$filter=Processed eq 'Y'`  
    - `POST /api/v1/models/gl_journal`

- **Processes Endpoint** (`/api/v1/processes/`):  
  - Triggers server-side processes.  
  - Example:  
    - `PUT /api/v1/processes/timesheet-export` to run the timesheet export.

- **Swagger UI**:  
  - Browse and test endpoints.  
  - View field requirements and try out requests.  
  - Auto-generate API client code.

---

## 💡 Tips  
- Use Swagger UI before coding to prototype integration calls.  
- Add `$filter` in GET requests for specific results (e.g., Processed = 'Y').  
- Secure endpoints using **WebService Role** and Bearer tokens.  
- For recurring exports, call scheduled processes via the `/processes/` endpoint.

---

## 📝 Notes  
- **iDempiere v11+** is required for native REST API support.  
- For AbilityERP users, backporting may be necessary—contact Flamingo Logic Support.  
- Swagger UI is built-in and accessible for testing endpoints.  
- Useful links:  
  - [GitHub – bxservice/idempiere-rest](https://github.com/bxservice/idempiere-rest)  
  - [Understanding REST API – iDempiere Blog](https://idempiere.org/blog/2025/03/27/understanding-rest-api-and-its-importance-in-idempiere-development/?v=1)

---
(end of note)
