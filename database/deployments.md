# 🚀 Deployments Table

The `deployments` table stores every smart contract deployment made through Nexus.

---

## Table Structure

| Column | Data Type | Constraints | Description |
|---------|-----------|-------------|-------------|
| id | UUID | Primary Key | Unique deployment ID |
| contract_id | UUID | Foreign Key → smart_contracts.id | Smart contract deployed |
| network | ENUM | NOT NULL | Ethereum, Polygon, Base, Arbitrum, BNB |
| contract_address | VARCHAR(255) | NOT NULL | Blockchain address |
| transaction_hash | VARCHAR(255) | UNIQUE | Deployment transaction |
| deployed_by | UUID | Foreign Key → users.id | User who deployed |
| gas_used | BIGINT | NULL | Gas consumed |
| deployment_cost | DECIMAL | NULL | Cost of deployment |
| block_number | BIGINT | NULL | Blockchain block number |
| status | ENUM | DEFAULT 'Pending' | Pending, Success, Failed |
| deployed_at | TIMESTAMP | DEFAULT NOW() | Deployment time |

---

## Relationships

- One Smart Contract can have multiple Deployments.
- One User can perform multiple Deployments.

---

## Status

🟢 Planned
