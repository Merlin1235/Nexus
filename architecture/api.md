# 🔌 API Architecture

## Overview

The Nexus API enables communication between the frontend, backend, blockchain services, and AI module.

---

# API Principles

- RESTful Design
- JSON Responses
- JWT Authentication
- Versioning (v1)
- Secure Endpoints

---

# Authentication Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /api/v1/auth/register | Register a new user |
| POST | /api/v1/auth/login | User login |
| POST | /api/v1/auth/logout | Logout |
| GET | /api/v1/auth/profile | Get current user |

---

# Project Endpoints

| Method | Endpoint |
|---------|-----------|
| GET | /api/v1/projects |
| POST | /api/v1/projects |
| PUT | /api/v1/projects/:id |
| DELETE | /api/v1/projects/:id |

---

# Smart Contract Endpoints

| Method | Endpoint |
|---------|-----------|
| GET | /api/v1/contracts |
| POST | /api/v1/contracts |
| POST | /api/v1/contracts/compile |
| POST | /api/v1/contracts/deploy |

---

# AI Endpoints

| Method | Endpoint |
|---------|-----------|
| POST | /api/v1/ai/chat |
| POST | /api/v1/ai/explain |
| POST | /api/v1/ai/generate |

---

# Deployment Endpoints

| Method | Endpoint |
|---------|-----------|
| GET | /api/v1/deployments |
| POST | /api/v1/deployments |

---

# API Response

Success

```json
{
  "success": true,
  "message": "Operation completed successfully."
}
```

Error

```json
{
  "success": false,
  "message": "Unauthorized."
}
```

---

# Goals

- Secure
- Consistent
- Easy to Use
- Well Documented
Frontend

↓

API Gateway

↓

Controllers

↓

Services

↓

Database / Blockchain / AI

↓

Response

---

## Status

🟡 Sprint 2 In Progress
