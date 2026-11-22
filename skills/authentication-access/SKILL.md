---
name: كلمات المرور والمصادقة والصلاحيات
description: تسجيل الدخول والمصادقة والصلاحيات: تخزين آمن لكلمات المرور، الجلسات، JWT، OAuth، التحقق بخطوتين، الأدوار، استعادة الحساب. authentication auth login signin signup session sessions jwt oauth oidc sso 2fa mfa passkeys hashing bcrypt argon2 roles rbac permissions تسجيل الدخول المصادقة الصلاحيات صلاحيات الجلسات كلمات المرور
version: 1.0.0
category: security
---
Use this for sign-in, sessions, tokens and permission design.
1. Passwords: hash with Argon2id (or bcrypt with cost 12 or more, or scrypt); the salt is per password and built into the algorithm; never store them reversibly. Allow long passphrases (64 characters or more), check new ones against breached-password lists, and avoid forced periodic changes.
2. Sign-in protection: rate limits and growing delays per account and per IP, one generic error message ("email or password is incorrect"), two-factor sign-in with authenticator apps or passkeys in preference to SMS.
3. Web sessions: server-side sessions or signed tokens in cookies marked Secure, HttpOnly and SameSite; a new session id at sign-in; idle expiry; sign-out from all devices.
4. JWT: lifetimes of minutes, refresh tokens that rotate and can be revoked; verify signature, issuer, audience and expiry; reject the "none" algorithm; prefer cookies over localStorage for browser apps.
5. OAuth and OpenID Connect: authorization code flow with PKCE, a checked state parameter, minimal scopes.
6. Authorization: deny by default; check permissions on the server for every request and every object; model roles (RBAC) or attributes (ABAC) in one place instead of scattered checks.
7. Recovery is part of security: single-use, short-lived reset links; a notice to the owner on every account change; re-authentication before sensitive actions such as an email or payout change.
8. Log authentication events, never the secrets themselves.
Answer shape: the recommended design, then code for the critical parts (hashing, session or token checks).
