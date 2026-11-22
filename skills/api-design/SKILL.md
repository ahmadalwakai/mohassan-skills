---
name: واجهات API وREST
description: هندسة واجهات API: REST، المسارات، أفعال HTTP، رموز الحالة، رسائل الأخطاء، الترقيم، الإصدارات، OpenAPI، GraphQL، webhooks. api apis rest restful http endpoint endpoints status json openapi swagger graphql webhook webhooks pagination versioning idempotency الواجهات البرمجية واجهة برمجية
version: 1.0.0
category: coding
---
Use this when designing or reviewing an HTTP API.
1. Resources are plural nouns (/bookings, /bookings/{id}); methods are the verbs. GET reads and is safe, POST creates, PUT replaces, PATCH updates part, DELETE removes. PUT and DELETE are idempotent; accept an Idempotency-Key header on POST when clients retry.
2. Status codes: 200 OK, 201 Created with a Location header, 204 No Content, 400 malformed, 401 not authenticated, 403 not allowed, 404 not found, 409 state conflict, 422 validation failed, 429 rate limited with Retry-After, 500 server fault, 503 temporarily unavailable.
3. One error body everywhere, for example {"error": {"code": "BOOKING_FULL", "message": "...", "details": []}}. Codes are stable and machine-readable; messages are for people.
4. Paginate lists from the start: cursors for large or changing data, limit and offset only for small lists; filtering and sorting through query parameters; a maximum page size.
5. Evolve without breaking: add fields, never rename or repurpose them. When a break is unavoidable, version in the path (/v2) or a header and keep the old version for a stated period.
6. Conventions: ISO 8601 timestamps in UTC, money as integer minor units with a currency code, one casing style for fields.
7. Security: authenticate every private route, check that the record belongs to the caller, validate input, rate-limit.
8. Document every endpoint, schema, error and example in OpenAPI.
9. Webhooks: sign the payload, include an event id for deduplication, retry with backoff, and expect receivers to answer 2xx quickly.
Answer shape: an endpoint table (method, path, purpose, status codes), then example request and response JSON.
