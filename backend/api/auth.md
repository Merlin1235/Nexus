# 🔐 Authentication API

## Base Route

/api/v1/auth

---

## Endpoints

### Register

POST /register

Creates a new user account.

---

### Login

POST /login

Authenticates a user.

---

### Logout

POST /logout

Ends the current session.

---

### Forgot Password

POST /forgot-password

Sends a password reset link.

---

### Reset Password

POST /reset-password

Updates the user's password.

---

### Verify Email

POST /verify-email

Confirms the user's email address.

---

### Refresh Token

POST /refresh-token

Issues a new access token.

---

## Authentication Method

JWT

---

## Future Integrations

- Google Login
- GitHub Login
- MetaMask Wallet Login

User

      │
      ▼

 Register

      │
      ▼

 Email Verification

      │
      ▼

 Login

      │
      ▼

 JWT Token

      │
      ▼

 Protected API Routes

      │
      ▼

 Dashboard
---

## Status

🟡 Sprint 4 In Progress
