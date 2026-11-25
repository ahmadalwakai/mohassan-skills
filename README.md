# Mohassan skills library

194 instruction-only skills for Mohassan's GitHub skills source. Each skill is guidance text. When a request matches a skill, the chat adds it to the model's prompt. When no model is running, the chat shows the skill's steps to the person who asked instead. A skill grants no tools, runs no code and has no side effects.

## Layout

```
skills/<slug>/SKILL.md
NOTICE.md      sources and licences of the adapted skills
LICENSES/      licence texts those sources require
```

The folder name is the skill id: lowercase letters, digits and hyphens. Each `SKILL.md` has this shape:

```
---
name: Arabic display name (3 to 100 characters)
description: Arabic summary — then Arabic and English search words (10 to 1000 characters)
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

Skills adapted from another project also carry `language`, `license`, `source`, `source-sha256` and `attribution` in the front matter, and are listed in `NOTICE.md`. An English variant names its Arabic skill in `variant-of`.

The body is written in Arabic, because the chat shows it to Arabic-speaking people as it is. The chat's skill reader shows the opening sentence, then the steps, the answer shape, «تحقق قبل التسليم», «أخطاء شائعة» and any other section. «ما أحتاجه منك» comes last, as the question to the person. A section titled «متى تُستخدم» is never shown, so say when the skill applies in the opening sentence. Keep code, commands and product names in Latin script inside backticks.

## Rules for adding or editing a skill

- Instructions only: no scripts, no `skill.contract.json`, no links, no HTML comments and no hidden or direction-control characters.
- Keep the body under 1800 characters. The chat gives all skill text at most 4000 characters, so two skills must fit together.
- The reader matches word stems in the folder name, the name and the description, and weighs each stem by how few skills hold it. A name word counts twice as much as a description word. So:
  - put the words people actually type in the name and the description, in Arabic (with dialect and common spellings, such as «عرس» and «انستقرام») and in English;
  - add the forms people use that the stemmer does not join: possessives of words ending in ة («سيارتي»، «قناتي»، «استقالتي») and verbs («أستورد»، «أغلف»، «أسوق»);
  - do not join an important name word to «و»: «وتحليل» is read as one word. Separate with «،» or «:»;
  - do not label the keyword list with «كلمات:»; the label is read as a search word. Separate the summary from the words with « — »;
  - leave out everyday words such as ما، كيف، أفضل، اليوم، what, how or best, and avoid a common word that is not the skill's subject. Every new skill that shares a word lowers that word's weight for the skills that rely on it.
- Before publishing a change, measure it from the main repository: `npx tsx scripts/skills-library/measure-reader.ts --out after.json --compare before.json`, and read every changed choice. A skill that takes a request another skill owns is fixed before it is published.
- The reader refuses some wording before it reads any skill: a question that opens with «متى» or «كم», "what is" or "is it", and live words such as "score" or a price with «اليوم». No skill text changes that.
- The safety inspector holds back phrases that look like instructions to the model or like requests for secrets, even when they appear in a warning:
  - «you are now», or «تجاهل» followed closely by التعليمات, القواعد or الأوامر;
  - the verbs أرسل، اكشف، اطبع، انشر (or reveal, print, show, send, post) near words for passwords, keys or codes, such as كلمة المرور، المفتاح، الرمز. «الكلمات المفتاحية» counts as المفتاح;
  - file names of credential stores;
  - telling the model to act without telling or asking the user.

  A skill with any finding is not activated automatically.
- Raise `version` when you change a skill. Every new version counts toward the per-owner limit of 4,000 GitHub versions, and nothing is deleted.
- At most 1,000 skill folders: above that the whole sync stops; it does not skip the extra folders.
- This repository is public. Never put customer data, credentials or private business details in it.

## Connecting it

On the server:

1. Set `SKILL_ENGINE_ENABLED=true`.
2. Set `SKILL_REMOTE_REPO=<owner>/<repo>`, `SKILL_REMOTE_REF=main` and `SKILL_REMOTE_PATH=skills`.
3. For automatic activation of skills that pass inspection with no findings, also set `SKILL_REMOTE_AUTO_ACTIVATE=true`.
