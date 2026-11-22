---
name: أداء المواقع والتطبيقات
description: أداء المواقع وسرعة التحميل: Core Web Vitals، LCP، INP، CLS، حجم الحزم، ضغط صور، التخزين المؤقت، CDN، بطء الخادم. performance speed slow lighthouse pagespeed vitals lcp inp cls ttfb bundle lazy loading cdn compression سرعة السرعة بطء بطيء بطيئة الأداء أداء تسريع التحميل
version: 1.0.0
category: coding
---
Use this to make a website or web app load and respond faster.
1. Measure before changing: Lighthouse or PageSpeed Insights for lab data, field data (Chrome UX Report or real-user monitoring) for the truth. Targets at the 75th percentile: LCP ≤ 2.5 s, INP ≤ 200 ms, CLS ≤ 0.1, TTFB under about 0.8 s.
2. LCP (largest content): serve the hero image as AVIF or WebP at its displayed size, preload it and never lazy-load it, inline critical CSS, remove render-blocking scripts, cut server time with caching.
3. INP (responsiveness): ship less JavaScript, split long tasks over 50 ms, defer third-party scripts, keep input handlers light, debounce expensive listeners.
4. CLS (layout shift): width and height or aspect-ratio on images, video and embeds; reserved space for late content; font-display: swap with matched fallback metrics.
5. JavaScript weight: analyze the bundle, drop unused libraries, import only the functions used, split code by route, load non-critical widgets on interaction.
6. Network: HTTP/2 or HTTP/3, Brotli or gzip, a CDN for static files with long cache lifetimes and hashed file names, short caching for HTML.
7. Images and fonts: responsive srcset, lazy loading below the fold, subset fonts, at most two families with few weights.
8. Server: indexes, query caching, no N+1 calls, streaming or pagination for large responses.
Answer shape: the measured bottleneck first, then fixes ordered by gain and effort, then how to re-measure.
