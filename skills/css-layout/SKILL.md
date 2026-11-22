---
name: تنسيق CSS والصفحات المتجاوبة
description: تنسيق الصفحات بـ CSS: Flexbox، Grid، توسيط العناصر، التجاوب مع الجوال، media queries، Tailwind، المسافات، الطبقات، الحركة. css css3 flexbox flex grid layout responsive media queries container tailwind sass scss center centering zindex animation تنسيق متجاوب متجاوبة التجاوب توسيط أوسط اوسط
version: 1.0.0
category: coding
---
Use this for CSS layout, responsive pages and styling problems.
1. Choose by dimension: Flexbox for one direction (a row of buttons, a nav bar), Grid for two (page layouts, card galleries). Space children with `gap` instead of margins.
2. Centering: `display: grid; place-items: center;` on the parent centers both ways; `margin-inline: auto` centers a block with a set width; `text-align: center` centers inline text.
3. Responsive by default: mobile-first styles, then `min-width` media queries at content breakpoints (around 640, 768, 1024, 1280 px). Fluid sizing with `clamp()`, `minmax()` and `repeat(auto-fit, minmax(16rem, 1fr))` removes many breakpoints; container queries size components by their own width.
4. Units: rem for type and spacing, % or fr for widths, `dvh` instead of `vh` for full-height mobile sections, a max width of about 60 to 75 characters for reading text.
5. Box model: `box-sizing: border-box` everywhere. Horizontal overflow usually comes from fixed widths, long words (`overflow-wrap: anywhere`) or images without `max-width: 100%`.
6. Stacking: z-index works only inside a stacking context; transform, opacity below 1 and positioning create new ones.
7. Logical properties (margin-inline-start, padding-inline, inset-inline) let one stylesheet serve RTL Arabic and LTR.
8. Low specificity: classes over IDs, no !important outside utilities, CSS variables for colors and spacing.
9. Motion: animate transform and opacity only, and respect prefers-reduced-motion.
Answer shape: the CSS with the HTML it needs, plus one line on browser support when relevant.
