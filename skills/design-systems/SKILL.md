---
name: أنظمة التصميم ومكتبات المكونات
description: بناء نظام تصميم ومكتبة مكونات: design tokens، متغيرات الألوان والمسافات والخطوط، المكونات الموحدة، التوثيق، Figma، Storybook، السمات. system systems tokens components library figma storybook variables theming variants guidelines نظام أنظمة مكونات المكونات موحدة موحد توحيد مكتبة
version: 1.0.0
category: design
---
Use this to create or improve a design system and its component library.
1. Start with an audit: capture the existing screens and list every color, font size, spacing value and component variant in use, then merge duplicates. Most products need far fewer values than they have.
2. Design tokens in layers: primitive values (blue-600, space-4); semantic tokens (color-text-primary, color-bg-danger, space-inline-md) that themes remap; component tokens only where a component needs its own setting. Keep one source (JSON or Figma variables) and generate CSS variables and platform files from it.
3. Foundations: color roles, type scale, spacing scale on a 4 or 8 px base, radii, elevation, motion durations, breakpoints, icon set, grid.
4. Components in order of use: button, input, select, checkbox, radio, switch, card, modal, toast, table, tabs, navigation. Document each one's purpose, anatomy, variants, sizes, every state (hover, focus, disabled, loading, error), content rules, accessibility notes and do and don't examples.
5. Code components with the same names as in Figma; one responsibility per component; composition rather than endless props; keyboard, focus and ARIA built in.
6. Theming: light, dark and brand themes swap semantic tokens only; RTL handled with logical properties.
7. Governance: an owner, a contribution process, semantic versioning with a changelog, deprecation before removal, visual regression tests (Storybook with snapshot tests).
8. Measure adoption: share of screens built from system components and time to build a new screen.
Answer shape: the token structure (table or JSON), the prioritized component list, and the rollout steps.
