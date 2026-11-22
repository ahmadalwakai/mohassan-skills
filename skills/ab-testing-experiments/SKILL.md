---
name: تجارب A/B ومقارنة النسخ
description: تجارب واختبار A/B: مقارنة نسختين من إعلان أو عنوان، حجم العينة، مدة الاختبار، الدلالة الإحصائية، فرضية التجربة، قراءة النتائج. ab split experiment experiments variant variants hypothesis sample duration uplift lift optimizely تجربة تجارب التجربة أجرب اجرب نسختين نسخة عنوانين علمياً فرضية
version: 1.0.0
category: analytics
---
Use this to design, run and read A/B tests and other experiments.
1. Hypothesis first: "Changing X for audience Y will improve metric Z because of reason R." Choose one primary metric before the test (conversion rate, click-through rate, revenue per visitor) plus guardrail metrics (refunds, complaints, page speed).
2. Test one meaningful change at a time, or use a proper multivariate design with enough traffic.
3. Sample size before starting depends on the baseline rate and the smallest lift worth detecting. With a 5% conversion rate and a 20% relative lift (to 6%), each variant needs roughly 8,000 visitors at 95% confidence and 80% power. Small sites should test big changes.
4. Duration: whole weeks, at least one and usually two to four, to cover weekday patterns. Stopping the moment a result looks significant inflates false positives unless the method is built for sequential reading.
5. Randomize by user, not by page view, keep each user's assignment stable, and check that the split matches the plan (a mismatch signals a bug).
6. Read results as a lift with a confidence interval, not just a winner; treat segment differences as ideas for the next test, not proof.
7. Ads: use the platform's experiment or ad-variation tools so traffic splits fairly; two ads that ran at different times are not a test.
8. Keep a test log: hypothesis, dates, traffic, result, decision, lessons.
Answer shape: the test plan (hypothesis, metric, variants, sample size, duration), then how to read the outcome.
