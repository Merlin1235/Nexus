# 📜 Smart Contracts Table

The `smart_contracts` table stores blockchain smart contracts associated with a project.

---

## Table Structure

| Column | Data Type | Constraints | Description |
|---------|-----------|-------------|-------------|
| id | UUID | Primary Key | Unique contract ID |
| project_id | UUID | Foreign Key → projects.id | Parent project |
| name | VARCHAR(100) | NOT NULL | Contract name |
| contract_type | ENUM | NOT NULL | ERC20, ERC721, ERC1155, Custom |
| language | ENUM | DEFAULT 'Solidity' | Programming language |
| compiler_version | VARCHAR(20) | NOT NULL | Solidity compiler version |
| source_code | TEXT | NOT NULL | Smart contract source code |
| abi | JSON | NULL | Contract ABI |
| bytecode | TEXT | NULL | Compiled bytecode |
| contract_address | VARCHAR(255) | NULL | Blockchain contract address |
| deployment_status | ENUM | DEFAULT 'Draft' | Draft, Compiled, Deployed |
| created_at | TIMESTAMP | DEFAULT NOW() | Creation date |
| updated_at | TIMESTAMP | DEFAULT NOW() | Last update |

---

## Relationships

- One Project can contain multiple Smart Contracts.
- One Smart Contract can have multiple Deployments.

---

## Status

🟢 Planned
