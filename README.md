# Mohassan skills library

100 instruction-only skills for Mohassan's GitHub skills source. Each skill is guidance text. When a request matches a skill, the chat adds it to the model's prompt. When no model is running, the chat shows the skill's steps to the person who asked instead. A skill grants no tools, runs no code and has no side effects.

## Layout

```
skills/<slug>/SKILL.md
```

The folder name is the skill id: lowercase letters, digits and hyphens. Each `SKILL.md` has this shape:

```
---
name: Arabic display name (3 to 100 characters)
description: Arabic summary followed by Arabic and English search words (10 to 1000 characters)
version: 1.1.0
category: one of reasoning, coding, browser, computer, design, creativity, documents, languages, business, marketing, research, security, analytics, media
---
One opening sentence in Arabic: what the skill helps with.

## الخطوات
1. ...

## شكل الجواب
...

## أخطاء شائعة
- ... (optional)

## ما أحتاجه منك
- ...
```

The body is written in Arabic, because the chat shows it to Arabic-speaking people as it is. The chat's skill reader shows the opening sentence, then the steps, the answer shape, «تحقق قبل التسليم», «أخطاء شائعة» and any other section. «ما أحتاجه منك» comes last, as the question to the person. A section titled «متى تُستخدم» is never shown, so say when the skill applies in the opening sentence. Keep code, commands and product names in Latin script inside backticks.

## Rules for adding or editing a skill

- Instructions only: no scripts, no `skill.contract.json`, no links, no HTML comments and no hidden or direction-control characters.
- Keep the body under 1800 characters. The chat gives all skill text at most 4000 characters, so two skills must fit together.
- The router matches words in the folder name, the name and the description. Put the words people actually type there, in Arabic (with common spellings) and in English. Leave out everyday words such as ما، كيف، أفضل، اليوم، what, how or best, which make a skill fire on small talk.
- The safety inspector holds back phrases that look like instructions to the model or like requests for secrets, even when they appear in a warning:
  - «you are now», or «تجاهل» followed closely by التعليمات, القواعد or الأوامر;
  - the verbs أرسل، اكشف، اطبع، انشر (or reveal, print, show, send, post) near words for passwords, keys or codes, such as كلمة المرور، المفتاح، الرمز. «الكلمات المفتاحية» counts as المفتاح;
  - file names of credential stores;
  - telling the model to act without telling or asking the user.

  A skill with any finding is not activated automatically.
- Raise `version` when you change a skill. Every new version counts toward the per-owner limit of imported versions.
- This repository is public. Never put customer data, credentials or private business details in it.

## Connecting it

On the server:

1. Set `SKILL_ENGINE_ENABLED=true`.
2. Set `SKILL_REMOTE_REPO=<owner>/<repo>`, `SKILL_REMOTE_REF=main` and `SKILL_REMOTE_PATH=skills`.
3. For automatic activation of skills that pass inspection with no findings, also set `SKILL_REMOTE_AUTO_ACTIVATE=true`.
