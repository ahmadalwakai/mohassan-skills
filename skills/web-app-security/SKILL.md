---
name: أمن تطبيقات الويب
description: أمن تطبيقات ومواقع الويب: OWASP Top 10، حقن SQL، XSS، CSRF، SSRF، رفع الملفات، التحقق من المدخلات، رؤوس الأمان، فحص الثغرات. security secure owasp vulnerability vulnerabilities injection xss csrf ssrf cors csp headers pentest audit hardening ثغرة ثغرات الثغرات أمن الأمان اختراق هاكر حقن
version: 1.0.0
category: security
---
Use this to build or review a web application against common attacks.
1. Treat all input as hostile: validate type, length, format and allowed values on the server; reject rather than repair.
2. Injection: parameterized queries or an ORM for SQL, argument arrays instead of shell strings, no eval of user data, safe XML and YAML parsers.
3. XSS: rely on the framework's auto-escaping, sanitize any user HTML (DOMPurify or a server equivalent), set a Content-Security-Policy that blocks inline script, mark session cookies HttpOnly.
4. Sessions: hashed passwords, rate-limited sign-in, cookies marked Secure, HttpOnly and SameSite, session renewal at sign-in.
5. Authorization on every request, on the server, per object: the record must belong to the caller. Broken access control is the most common serious flaw; never trust ids or roles that come from the client.
6. CSRF: SameSite cookies plus anti-CSRF tokens for cookie-authenticated forms.
7. SSRF: when the server fetches a URL from a user, allow-list hosts, block private and cloud metadata address ranges, and refuse redirects to them.
8. Uploads: check the type by content, cap the size, store outside the web root under random names, serve with the correct content type and Content-Disposition.
9. Transport and headers: HTTPS with HSTS, X-Content-Type-Options: nosniff, frame-ancestors in the CSP, restrictive CORS.
10. Dependencies and credentials: audit packages, update regularly, keep credentials in a secret manager and out of code and logs.
Answer shape: findings as risk, affected code, one-line attack scenario and fix; then what was not checked.
