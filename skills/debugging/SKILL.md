---
name: تشخيص الأخطاء البرمجية وإصلاحها
description: تشخيص الأخطاء البرمجية وإصلاحها: خطأ برمجي، استثناء، تتبع المكدس، تعطل، تجمد، خطأ متقطع، نتيجة خاطئة. debug debugging bug bugs error errors exception stack trace traceback crash crashes fix broken typeerror undefined null خطأ أخطاء الخطأ ايرور إيرور يتعطل يعلق معطل إصلاح اصلاح
version: 1.0.0
category: coding
---
Use this when code fails, throws, hangs or gives a wrong result.
1. Facts before theories: the exact error text and stack trace, the input that triggers it, expected versus actual result, what changed recently (code, dependency, data, environment) and whether it fails always or only sometimes.
2. Read the stack trace from the first frame in the project's own code. The failing line is often where a bad value is used, not where it was created; trace the value backwards.
3. Reproduce with the smallest input that still fails. If it is intermittent, suspect timing, shared state, caching, ordering, time zones or an external service.
4. Test one hypothesis at a time with a cheap check: log the actual value, set a breakpoint, add an assertion, or write a unit test that fails for the right reason. Change one variable per experiment.
5. Bisect when the cause is unclear: halve the input, the code path or the commit range (git bisect) until the cause is isolated.
6. Symptom shortcuts: undefined or null means data is missing or arrives late; works only locally means config, versions, paths or environment variables differ; worked yesterday means a dependency, data or deploy change; slowness usually means I/O in a loop or a missing index.
7. Fix the cause, not the symptom: no blanket try/catch and no silent defaults that hide the failure. Add a test that would have caught it.
8. Explain the root cause in one or two sentences, then the fix, then how to verify it.
When evidence is missing, ask once for the exact error text and the surrounding code.
