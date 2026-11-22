---
name: تطبيقات React و Next.js
description: واجهات React وتطبيقات Next.js: المكونات، الحالة، hooks، useEffect، التوجيه، العرض من الخادم، جلب البيانات، أخطاء hydration. react reactjs nextjs next jsx tsx component components hooks useeffect usestate usememo server components app router ssr hydration vercel رياكت ريأكت نكست نيكست مكون مكونات
version: 1.0.0
category: coding
---
Use this for React components and Next.js applications.
1. Components are small, pure functions of props and state. Lift state only as high as needed and derive values during render instead of duplicating them in state.
2. useEffect synchronizes with external systems (subscriptions, timers, non-React widgets). It is not for computing values or reacting to events. List every value it uses as a dependency; break loops by moving logic into event handlers, stabilizing inputs, or deleting the effect. Clean up subscriptions and abort fetches in the cleanup. Strict Mode runs effects twice in development on purpose.
3. Data: in the Next.js App Router fetch on the server (Server Components, route handlers, server actions); mark Client Components with "use client" only where interaction is needed. On the client prefer TanStack Query or SWR over hand-written fetch effects.
4. Lists need stable keys from data ids, never array indexes when items can reorder.
5. Forms: validate on the client for feedback and always again on the server.
6. Performance: measure with the React Profiler and Lighthouse, then split code with dynamic import, use next/image and next/font, keep heavy libraries off the client, and memoize only measured hot spots.
7. Hydration errors mean server and client rendered different output (dates, random values, window checks); render those after mount.
8. Accessibility: semantic elements, labelled inputs, keyboard support for custom widgets.
Answer shape: the cause in a sentence, then complete files with their paths.
