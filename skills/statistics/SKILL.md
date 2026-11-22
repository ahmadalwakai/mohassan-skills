---
name: الإحصاء والتنبؤ
description: الإحصاء والتنبؤ: المتوسط والوسيط والانحراف المعياري، الاحتمالات، العينات، الدلالة الإحصائية، قيمة p، فترات الثقة، الانحدار، السلاسل الزمنية والتنبؤ بالمبيعات. statistical mean median mode variance deviation probability sample significance significant pvalue confidence interval regression correlation forecast forecasting timeseries إحصاء الإحصاء احصاء إحصائية الإحصائية المتوسط الوسيط الانحراف الاحتمالات الانحدار التنبؤ
version: 1.0.0
category: analytics
---
Use this for statistical reasoning, statistical tests and forecasts.
1. Describe before inferring: for skewed data (incomes, delivery times, house prices) report the median and quartiles, not only the mean, which suits roughly symmetric data. Always give the spread (standard deviation or interquartile range) and the sample size.
2. Samples: say how the sample was drawn; convenience samples and self-selected surveys can be biased whatever their size.
3. Significance: a p-value is the probability of data at least this extreme if there were no real effect. p < 0.05 is a convention, not proof. Report the effect size and a 95% confidence interval, which show how large and how certain the effect is.
4. Choose the test by data type: two group means (t-test, or Mann-Whitney for skewed data), proportions (chi-square or a two-proportion z-test), several groups (ANOVA or Kruskal-Wallis), relationships (correlation, regression). Check the assumptions.
5. Many comparisons inflate false positives: correct for them, or fix the main metric in advance.
6. Correlation is not causation: randomized experiments establish causes; observational data need careful control of confounders.
7. Regression: interpret coefficients in real units ("each extra day of delivery time goes with 3% fewer repeat orders"), check residuals, never extrapolate far beyond the data.
8. Forecasting: begin with simple baselines (last value, same period last year, moving average), then seasonal methods (exponential smoothing, ARIMA, Prophet) when there is enough history, ideally two or more seasonal cycles; validate on a held-out recent period; always give a range, not a single number.
Answer shape: the result in plain words, the numbers with their uncertainty, the method, and its main limitation.
