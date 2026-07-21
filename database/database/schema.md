# 🗄️ Nexus Database Schema

## Overview

The Nexus database is designed using PostgreSQL and follows relational database best practices.

---

## Database Tables

| Table | Status |
|--------|--------|
| Users | 🟢 Planned |
| Wallets | 🟢 Planned |
| Projects | 🟢 Planned |
| Smart Contracts | 🟢 Planned |
| Deployments | 🟢 Planned |
| Transactions | 🟢 Planned |
| AI Chats | 🟢 Planned |
| Notifications | 🟢 Planned |
| Activity Logs | 🟢 Planned |

---

## Relationships

- One User → Many Projects
- One User → Many Wallets
- One Project → Many Smart Contracts
- One Smart Contract → Many Deployments
- One User → Many AI Chats
- One User → Many Notifications

---

## Database Engine

- PostgreSQL
- UUID Primary Keys
- Prisma ORM (planned)

---

**Version:** v1.0
