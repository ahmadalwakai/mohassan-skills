---
name: TypeScript و JavaScript
description: البرمجة بلغتي TypeScript وJavaScript: الأنواع، الواجهات، async await، الوعود، الوحدات، أخطاء الأنواع، التحويل إلى تايبسكربت. typescript javascript js ts types type interface generics async await promise promises esm modules npm جافاسكربت جافا سكربت تايبسكربت تايب سكريبت
version: 1.0.0
category: coding
---
Use this for TypeScript or JavaScript code, types and language behaviour.
1. Prefer TypeScript in strict mode. Model data precisely: literal unions for states, discriminated unions instead of many optional fields, `unknown` instead of `any` at boundaries, narrowed by type guards or a schema validator (zod or similar) for external input.
2. `interface` and `type` both describe object shapes. Interfaces merge and extend; type aliases also express unions, intersections and mapped types. Keep one convention per codebase.
3. Async: await or return every promise; never leave one floating. Run independent calls with Promise.all, use Promise.allSettled when partial failure is acceptable, add timeouts with AbortController, and avoid await inside a loop when the calls are independent.
4. Errors: throw Error objects, keep the cause (`new Error(message, { cause })`), and handle errors where something can be done about them.
5. Values: use ===; floating point is inexact (0.1 + 0.2), so store money as integer minor units; keep dates as UTC and format at the edge with Intl.
6. Modules: ES modules for new code; no side effects at module top level; import types with `import type`.
7. Prefer immutability: const, spread or structuredClone instead of mutating shared objects or function arguments.
8. Give complete, runnable snippets with imports, and state the runtime (Node version or browser) when behaviour depends on it.
Answer shape: short explanation, the code, then one line on edge cases.
