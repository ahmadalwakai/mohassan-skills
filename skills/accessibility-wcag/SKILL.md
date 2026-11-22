---
name: إمكانية الوصول WCAG
description: إمكانية الوصول للمواقع والتطبيقات لذوي الإعاقة: WCAG 2.2، قارئ الشاشة، التنقل بلوحة المفاتيح، التباين، النص البديل، ARIA، المكفوفين وضعاف البصر. accessibility accessible a11y wcag aria screen reader keyboard alt captions disability blind الوصول إمكانية قارئ الشاشة المكفوفين للمكفوفين ضعاف البصر الإعاقة
version: 1.0.0
category: design
---
Use this to make a website or app usable by people with disabilities, aiming at WCAG 2.2 level AA.
1. Semantic HTML first: real buttons and links, headings in order with one h1, lists, tables with header cells, landmarks (header, nav, main, footer). Use ARIA only when no native element fits, and then the complete pattern (role, state, keyboard).
2. Keyboard: everything reachable and usable with Tab, Shift+Tab, Enter, Space, Escape and arrow keys; a visible focus indicator; logical focus order; no traps; focus moves into dialogs and returns when they close; a skip link to the main content.
3. Screen readers: alt text that states purpose (empty alt for decoration), a label tied to every input, errors linked to their fields and announced (aria-live for dynamic updates), descriptive link text instead of "click here", and the page language set (lang="ar" or lang="en").
4. Contrast: 4.5:1 for normal text, 3:1 for large text, interface components and focus indicators; never information by color alone.
5. Zoom and size: text enlarged to 200 percent without loss, reflow at 320 px width without horizontal scrolling, touch targets of at least 24 by 24 px (44 recommended).
6. Media: captions for video, transcripts for audio, no autoplay with sound, nothing flashing more than three times per second, reduced motion when prefers-reduced-motion is set.
7. Forms: clear instructions, sign-in that does not depend on memory puzzles, time limits that can be extended.
8. Test with automated tools (axe, Lighthouse), then by hand: keyboard only, a screen reader (NVDA, VoiceOver, TalkBack) and 200 percent zoom.
Answer shape: each issue with its WCAG criterion number, who it affects and the code fix; then the manual checks still needed.
