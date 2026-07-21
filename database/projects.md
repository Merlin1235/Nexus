# 📁 Projects Table

The `projects` table stores all development projects created by users.

---

## Table Structure

| Column | Data Type | Constraints | Description |
|---------|-----------|-------------|-------------|
| id | UUID | Primary Key | Unique project ID |
| owner_id | UUID | Foreign Key → users.id | Project owner |
| name | VARCHAR(100) | NOT NULL | Project name |
| slug | VARCHAR(100) | UNIQUE | URL-friendly project name |
| description | TEXT | NULL | Project description |
| blockchain | ENUM | NOT NULL | Ethereum, Polygon, Base, Solana, etc. |
| visibility | ENUM | DEFAULT 'private' | Public or Private |
| status | ENUM | DEFAULT 'draft' | Draft, Active, Archived |
| repository_url | TEXT | NULL | GitHub repository URL |
| created_at | TIMESTAMP | DEFAULT NOW() | Creation date |
| updated_at | TIMESTAMP | DEFAULT NOW() | Last update |

---

## Relationships

- One User can own many Projects.
- One Project can contain many Smart Contracts.
- One Project can have many Deployments.

---

## Status

🟢 Planned
