# 🗄️ Nexus Database Schema

## Database

PostgreSQL

---

# Users

| Field | Type |
|-------|------|
| id | UUID |
| full_name | String |
| email | String |
| password | String (hashed) |
| role | Enum |
| created_at | Timestamp |

---

# Projects

| Field | Type |
|-------|------|
| id | UUID |
| name | String |
| description | Text |
| owner_id | UUID |
| status | Enum |
| created_at | Timestamp |

---

# Smart Contracts

| Field | Type |
|-------|------|
| id | UUID |
| project_id | UUID |
| contract_name | String |
| network | String |
| address | String |
| deployed_at | Timestamp |

---

# AI Requests

| Field | Type |
|-------|------|
| id | UUID |
| user_id | UUID |
| prompt | Text |
| response | Text |
| created_at | Timestamp |

---

# Deployments

| Field | Type |
|-------|------|
| id | UUID |
| project_id | UUID |
| environment | String |
| status | Enum |
| deployed_at | Timestamp |

---

## Relationships

User
 └── Projects

Project
 ├── Smart Contracts
 └── Deployments

User
 └── AI Requests

 Users
   │
   ├──────────► Projects
   │                 │
   │                 ├────────► Smart Contracts
   │                 │
   │                 └────────► Deployments
   │
   └──────────► AI Requests

---

## Status

🟡 Sprint 4 In Progress
