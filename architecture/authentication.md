# 🔐 Authentication Architecture

## Overview

Nexus provides secure authentication using traditional login and Web3 wallet authentication.

---

# Authentication Methods

- Email & Password
- Google OAuth (Future)
- GitHub OAuth (Future)
- MetaMask Wallet Login

---

# Security

- JWT Authentication
- Password Hashing (bcrypt)
- Refresh Tokens
- HTTPS
- Rate Limiting

---

# Authentication Flow

User

↓

Login Request

↓

Authentication Service

↓

Verify Credentials

↓

Generate JWT

↓

Return Access Token

---

# Wallet Authentication

User

↓

Connect MetaMask

↓

Sign Message

↓

Verify Signature

↓

Generate JWT

↓

Dashboard

---

# Technologies

| Technology | Purpose |
|------------|---------|
| JWT | Authentication |
| bcrypt | Password Hashing |
| Passport.js | Authentication Strategy |
| MetaMask | Wallet Login |

---

# Goals

- Secure
- Fast
- User Friendly
- Web3 Ready

---

## Status

🟡 Sprint 2 In Progress
