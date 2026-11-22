---
name: قواعد البيانات SQL
description: قواعد بيانات SQL: الجداول، العلاقات، الفهارس، الاستعلامات البطيئة، JOIN، التطبيع، الترحيل، المعاملات، PostgreSQL، MySQL. sql database databases postgres postgresql mysql sqlite query queries index indexes join joins schema tables migration migrations transaction explain orm قاعدة قواعد جداول الجداول استعلام الاستعلام استعلامات فهرس فهارس
version: 1.0.0
category: coding
---
Use this for schema work, SQL queries and database performance.
1. Schema: one table per entity, a surrogate primary key, foreign keys with ON DELETE chosen on purpose, NOT NULL by default, CHECK and UNIQUE constraints for business rules, timestamps with time zone. Normalize first (no repeated groups, no data that depends on part of a key); denormalize only for a measured read need.
2. Types: integer minor units or NUMERIC for money (never float), text with constraints instead of short varchar limits, enums or lookup tables for states, JSON columns only for genuinely schemaless data.
3. Slow query routine: run EXPLAIN (ANALYZE, BUFFERS) on the real query and data size, find sequential scans on large tables, add an index on the filter and join columns (composite order: equality, then range, then sort), and re-measure. Avoid functions on indexed columns in WHERE, SELECT *, and OFFSET pagination on big tables (use keyset pagination).
4. N+1: fetch related rows with a JOIN or a single IN query instead of one query per row.
5. Integrity: wrap multi-step writes in a transaction, choose the isolation level on purpose, and use SELECT ... FOR UPDATE or an atomic UPDATE for counters and stock.
6. Safety: always parameterized queries; never build SQL from user text. Run the WHERE clause of an UPDATE or DELETE as a SELECT first, inside a transaction.
7. Migrations are versioned, reversible when possible, and backward compatible during deploys: add a column, backfill, switch reads, then drop.
Answer shape: the schema or query, the indexes it needs, and why it is correct and fast.
