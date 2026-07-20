# API Design

## Overview

Nexus uses a REST API (Version 1).

Base URL

/api/v1

---

# Authentication

POST /auth/register

Registers a new user.

---

POST /auth/login

Logs a user in.

---

POST /auth/logout

Logs out the current user.

---

GET /auth/profile

Returns the authenticated user's profile.

---

# Projects

GET /projects

Returns all user projects.

---

POST /projects

Creates a new project.

---

GET /projects/{id}

Returns a specific project.

---

PUT /projects/{id}

Updates a project.

---

DELETE /projects/{id}

Deletes a project.

---

# Smart Contracts

GET /contracts

Returns all contracts.

---

POST /contracts

Creates a new contract.

---

GET /contracts/{id}

Returns contract details.

---

PUT /contracts/{id}

Updates contract code.

---

DELETE /contracts/{id}

Deletes a contract.

---

# Deployments

POST /deployments

Deploys a contract.

---

GET /deployments

Returns deployment history.

---

GET /deployments/{id}

Returns deployment details.

---

# Wallet

POST /wallet/connect

Connect wallet.

---

POST /wallet/disconnect

Disconnect wallet.

---

GET /wallet

Returns wallet information.
