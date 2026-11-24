---
name: سي شارب CSharp و ASP.NET Core
description: يوجّه البرمجة بلغة C# ومنصة .NET: الأنواع والكائنات، وLINQ، وasync وawait، وASP.NET Core للواجهات الخلفية، وEntity Framework، وWinForms وWPF، واختبارات xUnit — سي شارب سيشارب csharp dotnet dot net aspnet asp.net core entity framework ef core linq blazor wpf winforms xunit nuget visual studio
version: 1.0.0
category: coding
---
كود C# حديث يستخدم async بشكل صحيح وLINQ بوضوح، ويتبع بنية ASP.NET Core القياسية.

## الخطوات
1. حدّد إصدار .NET (يفضّل LTS) ونوع المشروع: Web API، أو MVC، أو Blazor، أو سطح المكتب.
2. async وawait: لا تستخدم .Result أو .Wait() في كود غير متزامن، ومرّر CancellationToken.
3. LINQ: اكتب الاستعلام مقروءًا، وانتبه أن الاستعلام يُنفّذ عند التعداد، واستخدم ToList عند الحاجة فقط.
4. ASP.NET Core: حقن التبعيات في Program.cs، ومتحكمات رفيعة، وخدمات تحمل المنطق، والتحقق بالسمات أو FluentValidation.
5. Entity Framework Core: Migrations لكل تغيير، وInclude لتحميل العلاقات، وAsNoTracking للقراءة فقط.
6. الأخطاء: اقرأ Stack Trace من أول سطر في كودك، وفعّل Nullable reference types لتقليل NullReferenceException.
7. الإعدادات في appsettings وUser Secrets أثناء التطوير، لا في الكود.
8. اختبر بـ xUnit، وشغّل dotnet test قبل الدمج.

## شكل الجواب
الكود المقترح مع شرح، والأوامر (dotnet ...)، وطريقة التحقق.

## ما أحتاجه منك
- إصدار .NET ونوع المشروع.
- الكود أو رسالة الخطأ كاملة.
- ما تريد بناءه أو إصلاحه.
