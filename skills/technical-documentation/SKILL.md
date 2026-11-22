---
name: التوثيق التقني
description: التوثيق التقني للمشاريع البرمجية: ملف README، توثيق API، أدلة الاستخدام والتثبيت، التعليقات في الكود، سجل التغييرات، وثائق المطورين. documentation docs readme guide manual tutorial changelog comments wiki onboarding توثيق التوثيق وثائق الوثائق دليل الاستخدام المستخدم التثبيت ريدمي
version: 1.0.0
category: documents
---
Use this for READMEs, API docs, user guides and other technical writing.
1. Write for a named reader and goal: a new developer setting up, an API consumer integrating, or an end user doing a task. Put what they need first.
2. README order: one-paragraph description (what it is, who it is for) → a quick start that works when copied (prerequisites with versions, install, configure, run) → usage examples → configuration reference (each environment variable with meaning, default and example) → tests → deployment → troubleshooting → contributing and license.
3. Every command and code sample is complete and tested, shows its expected output, and names the operating system when commands differ.
4. API reference per endpoint: method and path, purpose, authentication, parameters (name, type, required, description), a request example, response examples for success and each error, rate limits. Generate it from OpenAPI where possible and keep it in sync with the code.
5. Guides follow the task: numbered steps, one action per step, screenshots only where they help, and the result the user should see after key steps.
6. Explain why for important decisions (architecture notes, ADRs), not only what.
7. Style: short sentences, active voice, consistent terms, headings that match what people search for, jargon explained.
8. Changelog: version, date, and sections for added, changed, fixed and removed, with migration notes for breaking changes.
9. Use clearly fake example values, never real credentials.
Answer shape: the document in Markdown with headings, ready to commit.
