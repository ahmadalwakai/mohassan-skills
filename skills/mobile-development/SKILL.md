---
name: تطوير تطبيقات الجوال
description: برمجة تطبيقات الجوال للآيفون والأندرويد: Flutter، React Native، Swift، Kotlin، الأذونات، الإشعارات، الأداء، النشر على App Store وGoogle Play. mobile apps ios android iphone flutter dart react native expo swift swiftui kotlin compose store play testflight apk جوال الجوال موبايل آيفون ايفون أندرويد اندرويد تطبيقات
version: 1.0.0
category: coding
---
Use this for building, testing and publishing mobile apps.
1. Choose the stack from constraints: native (Swift/SwiftUI, Kotlin/Jetpack Compose) for the best platform fit, heavy device features or top performance; Flutter or React Native with Expo for one codebase and a small team. Existing web skills favour React Native; pixel-identical custom UI favours Flutter.
2. Architecture: separate UI, state (one predictable store or view models) and data (a repository over the API and a local cache). Design for offline and slow networks with caching, retries, and clear loading and error states.
3. Platform rules: Human Interface Guidelines and Material Design, touch targets of at least 44 pt on iOS and 48 dp on Android, safe areas, dynamic type, dark mode, RTL mirroring for Arabic.
4. Permissions: request at the moment of need with a reason, and keep the app usable in a reduced way when refused.
5. Security: tokens in Keychain or Keystore, never in plain storage; HTTPS only; no server-side keys embedded in the app binary.
6. Performance: keep the main thread free, virtualize long lists, size images for the screen, measure startup time and memory.
7. Release: TestFlight and Play internal testing first; store listing, screenshots, privacy answers (App Privacy, Data safety) and age rating; on Android an App Bundle signed with an upload key you keep safe. Expect review delays and fix rejections against the cited guideline.
8. Crash reporting and analytics from the first build, with consent where required.
Answer shape: a recommendation with reasons, then the code or step list for the chosen platform.
