---
name: واجهات RTL من اليمين لليسار
description: دعم العربي واتجاه RTL في المواقع والتطبيقات: عكس الواجهة، الأرقام، الأيقونات، النصوص المختلطة، التواريخ الهجرية، CSS المنطقي، التعريب. rtl ltr bidi right left dir mirroring mirrored i18n hijri numerals عربي العربي اليمين اليسار يمين يسار معكوسة معكوس مقلوبة التعريب تعريب
version: 1.0.0
category: design
---
Use this for Arabic and other right-to-left interfaces.
1. Set direction at the root: `<html lang="ar" dir="rtl">`, and `dir="auto"` on blocks of user-written text. Right alignment alone is not RTL.
2. Use logical CSS (margin-inline-start, padding-inline-end, inset-inline, text-align: start) with flex and grid, which mirror automatically; remove hard-coded left and right.
3. Mirror what shows direction: navigation order, back and forward arrows, step indicators, sliders, chevrons, drawer and close-button positions. Keep universal symbols unmirrored: media controls, clocks, check marks, logos, and usually the time axis of charts and number keypads.
4. Mixed text (Arabic with English names, numbers, emails, code): isolate Latin or numeric runs with `dir="ltr"` or the bdi element so order and punctuation stay right. Phone numbers, codes and prices often need explicit LTR isolation.
5. Digits: choose Western (0123) or Arabic-Indic (٠١٢٣) per audience and apply them everywhere; format with Intl.NumberFormat and Intl.DateTimeFormat for the locale, including the Hijri calendar where users expect it.
6. Typography: an Arabic font with correct shaping, taller line height, no letter-spacing, truncation at word boundaries.
7. Mobile: iOS and Android mirror layouts once RTL is supported (Android needs supportsRtl and start/end instead of left/right); test with the device language set to Arabic.
8. Translation is not enough: dates, currency (SAR, AED, EGP), address formats, names and tone must fit the market.
Answer shape: the concrete fixes (code or settings), then a short RTL test checklist.
