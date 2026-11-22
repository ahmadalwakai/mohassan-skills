# Mohassan skills library

100 instruction-only skills for Mohassan's GitHub skills source. Each skill is guidance text that the chat adds to the model's prompt when a request matches it. A skill grants no tools, runs no code and has no side effects.

## Layout

```
skills/<slug>/SKILL.md
```

The folder name is the skill id (lowercase letters, digits and hyphens). Each `SKILL.md` starts with this front matter:

```
---
name: Arabic display name (3 to 100 characters)
description: Arabic summary followed by Arabic and English search words (10 to 1000 characters)
version: 1.0.0
category: one of reasoning, coding, browser, computer, design, creativity, documents, languages, business, marketing, research, security, analytics, media
---
English instructions (at most 1800 characters)
```

## Rules for adding or editing a skill

- Instructions only: no scripts, no `skill.contract.json`, no links, no HTML comments, no hidden characters.
- Keep the body under 1800 characters. The chat gives all skill text at most 4000 characters, so two skills must fit together.
- The router matches words in the folder name, the name and the description. Put the words people actually type there, in Arabic (with common spellings) and English. Leave out everyday words such as ما، كيف، أفضل، اليوم، what, how or best, which make a skill fire on small talk.
- The safety inspector holds back phrases that look like instructions to the model or requests for secrets ("you are now", "ignore previous instructions", file names of credential stores, asking to print or send passwords or tokens, telling the model to hide actions from the user). A skill with any finding is not activated automatically.
- Raise `version` when you change a skill. Every new version counts toward the per-owner limit of imported versions.
- This repository is public. Never put customer data, credentials or private business details in it.

## Connecting it

On the server, set `SKILL_ENGINE_ENABLED=true`, `SKILL_REMOTE_REPO=<owner>/<repo>`, `SKILL_REMOTE_REF=main`, `SKILL_REMOTE_PATH=skills` and, for automatic activation of skills that pass inspection with no findings, `SKILL_REMOTE_AUTO_ACTIVATE=true`.
