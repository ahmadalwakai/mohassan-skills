---
name: هندسة البرمجيات والمعمارية
description: معمارية البرمجيات: تقسيم النظام، الطبقات، الوحدات، microservices أو monolith، قابلية التوسع، الأحداث، الطوابير، التخزين المؤقت، القرارات التقنية. architecture architect software monolith microservices modular modules layers scalability scalable ddd hexagonal events queues caching adr المعمارية معمارية هندسة البرمجيات الأنظمة التوسع طبقات
version: 1.0.0
category: coding
---
Use this for structuring a system, choosing components or reviewing an architecture.
1. Start from the requirements that shape structure: users and load (requests per second, data size, growth), latency targets, consistency needs, team size, budget, and what must never fail. Write them down before drawing boxes.
2. Default to a modular monolith: one deployable with strict module boundaries, where each module owns its data and exposes a small interface. Split into services only for a concrete reason: independent scaling, a separate team, a different runtime or failure isolation. Microservices add network failures, versioning and operational cost.
3. Layers inside a module: interface (HTTP, UI) → application (use cases) → domain (rules) → infrastructure (database, external APIs). Dependencies point inward; business rules do not import frameworks.
4. Data: one source of truth per fact; every copy is a cache with an owner and an expiry. Transactions inside a service, events or the outbox pattern across services.
5. Scaling order: measure, fix queries and indexes, cache hot reads, move slow work to queues, scale stateless app servers horizontally, and only then partition data.
6. Reliability: timeouts, retries with backoff and jitter, idempotent handlers, circuit breakers for flaky dependencies, graceful degradation when a dependency is down.
7. Observability from day one: structured logs with request ids, metrics, traces, and alerts on user-facing symptoms rather than raw CPU.
8. Record significant decisions as short ADRs: context, options considered, decision, consequences.
Answer shape: a text component diagram, the main data flows, the trade-offs chosen and what would trigger revisiting them.
