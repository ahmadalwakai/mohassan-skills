---
name: اختبارات الكود والبرمجيات
description: الاختبارات البرمجية: اختبارات الوحدة، التكامل، الطرفية e2e، التغطية، المحاكاة، الاختبارات المتقلبة، TDD. testing test tests unit integration e2e jest vitest pytest playwright cypress mock mocks coverage tdd flaky qa اختبار اختبارات الاختبار الاختبارات وحدة تكامل
version: 1.0.0
category: coding
---
Use this when writing, choosing or fixing automated tests.
1. Test behaviour, not implementation: given an input and state, assert the observable result. A refactor that keeps behaviour should not break tests.
2. Shape: many fast unit tests for logic, fewer integration tests for real boundaries (database, HTTP, queues), a handful of end-to-end tests for the critical journeys (sign-up, checkout, the main task).
3. Each test: one behaviour, a name that states it ("rejects an expired coupon"), arrange-act-assert layout, no logic or loops in the test body.
4. Cover the edges where bugs live: empty, one, many, maximum, invalid, duplicate, unicode text, time zone boundaries, concurrent calls, and every error path the code promises to handle.
5. Mock only what you do not own or cannot run fast (payment providers, email, clock, randomness). Prefer a real database in integration tests (containers or embedded engines) over mocks of the query layer.
6. Flaky tests are bugs: replace sleeps with waiting for a condition, isolate shared state, fix time with a fake clock, seed randomness.
7. End-to-end with Playwright or Cypress: select elements by role or label, wait on visible outcomes, keep test data independent per test.
8. Coverage is a map of untested code, not a goal. A bug fix always comes with a test that failed before the fix.
Answer shape: the test file with imports, the command to run it, and what each test protects.
