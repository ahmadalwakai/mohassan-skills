---
name: معادلات Excel والجداول الحسابية
description: جداول Excel وGoogle Sheets: المعادلات، VLOOKUP، XLOOKUP، INDEX MATCH، الجداول المحورية، التنسيق الشرطي، المخططات، الأتمتة، قوالب الميزانية. excel sheets spreadsheet spreadsheets formula formulas vlookup xlookup index match pivot conditional formatting macro vba powerquery إكسل اكسل الإكسل شيت معادلة معادلات دالة دوال المحورية الحسابية
version: 1.0.0
category: analytics
---
Use this for spreadsheet formulas, analysis and templates in Excel or Google Sheets.
1. Structure data as a proper table: one header row, one record per row, one type per column, no merged cells or blank rows inside; format it as a Table (Ctrl+T) so formulas and pivots grow with it.
2. Lookups: XLOOKUP is the modern default, for example =XLOOKUP(A2, Prices[Item], Prices[Price], "Not found"): exact match by default, looks left or right, handles missing values. VLOOKUP needs the key in the first column and FALSE for an exact match, and breaks when columns move. INDEX with MATCH works in every version. Google Sheets supports XLOOKUP too.
3. Summaries: SUMIFS, COUNTIFS and AVERAGEIFS for conditional totals; pivot tables for breakdowns; FILTER, SORT and UNIQUE dynamic arrays in Excel 365 and Sheets.
4. Dates and text: store real dates, not text; EOMONTH, NETWORKDAYS and DATEDIF for date math; TEXT only for display; TRIM, CLEAN and VALUE to fix imported data; TEXTSPLIT or Text to Columns to separate fields.
5. Robust formulas: absolute references ($A$1) for fixed cells, named ranges, IFERROR only around expected errors, data validation lists for inputs, assumptions in labelled cells instead of numbers typed into formulas.
6. Formatting: conditional formatting for thresholds and duplicates, consistent number formats (currency, %), frozen header rows.
7. Charts: lines for trends, columns for comparisons; no 3D or crowded pies.
8. Automation: Power Query for repeated imports and cleanup; macros or Apps Script for repetitive actions, documented.
9. Regional settings: some locales separate arguments with semicolons, and some Arabic versions translate function names.
Answer shape: the exact formula with its cell references explained, where to put it, and a small example table.
