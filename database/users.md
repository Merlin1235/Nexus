# 👤 Users Table

The `users` table stores all registered users of the Nexus platform.

---

## Table Structure

| Column | Data Type | Constraints | Description |
|---------|-----------|-------------|-------------|
| id | UUID | Primary Key | Unique user identifier |
| full_name | VARCHAR(100) | NOT NULL | Full name |
| username | VARCHAR(50) | UNIQUE | Username |
| email | VARCHAR(255) | UNIQUE | User email |
| password_hash | TEXT | NOT NULL | Encrypted password |
| profile_image | TEXT | NULL | Profile picture URL |
| role | ENUM | DEFAULT 'user' | User role |
| is_verified | BOOLEAN | DEFAULT FALSE | Email verification status |
| created_at | TIMESTAMP | DEFAULT NOW() | Account creation date |
| updated_at | TIMESTAMP | DEFAULT NOW() | Last update |

---

## Relationships

A user can have:

- Multiple Projects
- Multiple Wallets
- Multiple AI Chats
- Multiple Notifications

---

## Status

🟢 Planned
