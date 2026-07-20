# Database Design

## Overview

Nexus uses PostgreSQL as the primary database.

The database stores:

- Users
- Projects
- Smart Contracts
- Deployments
- Wallets
- Activity Logs

---

# Entity Relationship Diagram

User
│
├── Projects
│
├── Wallets
│
└── Activity Logs

Project
│
├── Smart Contracts
│
└── Deployments

---

# Tables

## Users

Stores user accounts.

Fields

- id
- username
- email
- password_hash
- avatar
- created_at
- updated_at

---

## Projects

Stores blockchain projects.

Fields

- id
- user_id
- project_name
- description
- blockchain
- created_at
- updated_at

---

## Smart Contracts

Stores Solidity contracts.

Fields

- id
- project_id
- contract_name
- source_code
- compiler_version
- abi
- bytecode

---

## Deployments

Stores deployment history.

Fields

- id
- contract_id
- network
- contract_address
- transaction_hash
- gas_used
- deployed_at

---

## Wallets

Stores connected wallets.

Fields

- id
- user_id
- wallet_address
- provider
- connected_at

---

## Activity Logs

Stores user activity.

Fields

- id
- user_id
- action
- timestamp
