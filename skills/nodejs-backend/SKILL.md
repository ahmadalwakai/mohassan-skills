---
name: خوادم Node.js والواجهات الخلفية
description: الخوادم والواجهات الخلفية بـ Node.js: Express، Fastify، المسارات، التحقق من المدخلات، الطوابير، السجلات، الإيقاف الآمن، النشر. node nodejs backend server servers express fastify nestjs middleware routes endpoints queue worker workers logging سيرفر سيرفرات الخادم خادم الخوادم باك اند الباك إند باكند نود
version: 1.0.0
category: coding
---
Use this for Node.js servers, APIs and background workers.
1. Run a maintained LTS release of Node. Use a framework with schema validation (Fastify with JSON schema, or Express with zod or joi) and validate every body, query and header at the edge; reject unknown fields.
2. Layers: route handler (HTTP only) → service (business rules) → data access (queries). Thin handlers let services be tested without HTTP.
3. Configuration comes from environment variables, read and validated once at startup; fail fast when a required value is missing. Credentials stay out of the repository.
4. One error handler maps known errors to status codes and logs unknown ones with a request id. Clients never receive stack traces.
5. Async safety: await every promise, put timeouts on outgoing HTTP calls, cap concurrency, and handle SIGTERM for a graceful shutdown that finishes in-flight requests.
6. Database: a connection pool, parameterized queries or a query builder, transactions for multi-step writes, migrations kept in version control.
7. Slow work (emails, images, reports) goes to a queue and a worker, not the request path. Jobs must be idempotent so retries are safe.
8. Operations: structured JSON logs, a health endpoint, and latency and error-rate metrics.
9. Security basics: rate limiting, CORS limited to known origins, security headers, regular dependency audits.
Answer shape: folder layout when relevant, the code, then how to run and test it.
