---
name: مراجعة الكود وتحسينه
description: مراجعة الكود البرمجي وتحسينه: أخطاء منطقية، حالات حدية، ثغرات، أداء، وضوح، تسمية، تكرار، اختبارات، إعادة هيكلة. code review reviewer pull request PR diff refactor refactoring clean readability maintainability راجع مراجعه الكود كود الشيفرة البرمجية تحسين هيكلة
version: 1.0.0
category: coding
---
Use this when reviewing or improving code, a diff or a pull request.
1. Establish intent first: what the change must do, its inputs, outputs and callers. Judge the code against that intent, not personal taste.
2. Review in this order and report blockers early:
   - Correctness: empty, null/undefined, zero, negative, very large, duplicate and unicode/RTL inputs; time zones and daylight saving; off-by-one; error paths; races between concurrent requests.
   - Security: untrusted input reaching SQL, shell, HTML or file paths; missing authorization checks; credentials committed in code.
   - Data safety: destructive migrations, unscoped deletes, retries that are not idempotent.
   - Performance: N+1 queries, work inside loops that belongs outside, blocking I/O on hot paths, unbounded memory.
   - Clarity: names that say what things are, functions with one job, duplication, dead code.
   - Tests: are the new behaviour and the motivating bug covered?
3. Write each finding as: location, the concrete failure (this input gives this wrong result), severity (blocker / should fix / optional) and the smallest fix.
4. Do not rewrite working code into a preferred style. Style remarks come last and are optional.
5. Refactoring keeps behaviour identical: one change at a time, guarded by existing tests or a characterization test written first.
6. Look outside the diff: callers, public APIs, config, docs and migrations the change touches.
7. If a judgement needs code you cannot see, name what is missing instead of guessing.
Answer shape: one-line verdict, findings grouped by severity, corrected code only where it fixes a blocker.
